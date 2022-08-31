# Fbx Motion Sampling Settings

The motion sampling modifier allows control over the the quality and memory and disk size of our motion assets. This modifier is automatically created for every motion in the Fbx.

### Some technical background information

Before we go over the settings, let's first discuss a few things to make it easier to understand what each setting does.

Motion data can be seen as a set of curves. For example the rotation over the x axis of a given joint can be such a curve. To be more precise, we capture the position (x, y, z), rotation (x, y, z, w) and scale (x, y, z) of each joint. The rotation has a w, because we use quaternions, but if you are not familiar with that you can just ignore that.

These curves can be stored in different ways. While in Maya you might animate using actual real curves, where you adjust tangents and control points, in game engines we typically have to sample these curves instead. With sampling we mean that we measure the value at that curve at specific time values. By interpolating between those points we approximate the original curve.

As you can imagine, the more sample points we store, the more accurate our approximation will be, so the closer it will look like it will look in your DCC app like Maya. The downside is, the more samples we store, the more memory we will use as well. The rate at which we store samples is called the **sample rate**. A sample rate of 30 would store 30 keyframes for every second of motion data. So every 1/30th of a second we store a sample.

If we uniformly space those samples, so at fixed distances, like 1/30th of a second, we can very quickly sample the motion data, as we can easily find the two samples to interpolate between at runtime. In EMotion FX we call this "**Uniform Motion Data**". Inside the Fbx settings we call it "**Evenly spaced keyframes (faster, mostly larger)**".

![image](/Images/Image1.png)

When the position, rotation, or scale of a given joint does not change, we of course do not store samples for that, but store just one value instead. So this is optimized.

However, now imagine the case where our rotation does not change for a long period during the motion, but then suddenly makes a change near the end. Using the uniformly sampled method we would be storing a lot of samples that will have the same value for a large part of the motion. What if we could just store the first key frame, and another keyframe just before the values start to change? This would reduce the amount of samples quite significantly. This is the method that we call "**Non-Uniform Motion Data**", or "**Reduced keyframes (slower, mostly smaller)**".

Now this generally uses less memory as we can reduce more of those samples. However, it comes at a cost in performance, because now we have to actually do a search to find the samples to interpolate between. Also we store a time value for each sample, which adds some overhead. But most of the times this overhead gets compensated by the reduced number of samples required. This is not always the case though. If you have motions where everything is constantly animating we can't reduce the amount of samples a lot and we still pay for this time value overhead. So there are cases where the high performance uniformly spaced method is faster and uses less memory.

This is the exact reason why we added an "Automatic" mode, so that we pick the high performance method if it also uses less memory. Sometimes the difference in memory usage can be pretty small, in which case you likely still want to go for higher performance. So we also added a "Allowed memory overhead" option that allows you to control how much extra memory you are willing to pay for in trade for performance. Please keep in mind that a value of say 15% doesn't mean you always use 15% more memory. This could as well be 2% as well. It just means it will stay within 15% maximum. Basically the automatic setting will try to create a motion for both motion data types, and see if the difference in memory and file size is within the specified limits. If so, it will choose the high runtime performance data type, otherwise the one the more memory efficient one.

Here is an image that shows the difference between uniform and non uniform sampling:

| Uniform (Evenly Spaced) | ![image](/Images/Image2.png) |
| Non-Uniform(Reduced Keyframes) | ![image](/Images/Image3.png) |

The "**quality**" settings basically tell how aggressively the non-uniform reduced keyframe method should remove samples. It will measure the error introduced when removing a given sample. If it is within limits it will remove that sample, otherwise it will keep it. The quality sliders basically allow you to set the values within a given range. This is easier than entering some values like 0.004 or so, which is the reason why we used a quality percentage. If you want smaller files and less memory usage you can try reducing the quality. Most memory is typically used by rotations, so the rotation quality is likely what you will be mostly interested in.

The quality settings are not doing anything when we do uniformly spaced sampling. This is why those settings will disappear if you choose to force to use that motion data type.

### The settings

If you go to the Fbx settings and go to the "Motions" tab, you should see the following modifier:
![image](/Images/Image4.png)

 <table>
  <tr>
    <th>Motion data type</th>
    <td>**Automatic: **Prefer runtime performance if the memory usage of the high performance method is smaller or within memory overhead limits. Otherwise prefer the slower but more memory efficient data type.

**Evenly spaced keyframes:** This data type results in the fastest runtime performance, often at the cost of increased memory usage. (UniformMotionData)

**Reduced keyframes:** This data type mostly results in the smallest memory footprint, at the cost of performance. (NonUniformMotionData).

**Custom data types:** There can be additional data types listed, which are implementations that are not provided by Lumberyard on default. This is not literally an option you will see, but you might just see a list of additional items.
</td>
  </tr>
  <tr>
    <th>Sample rate</th>
    <td>The rate at which we sample the motion data, in frames per second (aka samples per second).

**From Fbx:** We will use the same frame rate as the motion was created in. So if you set Maya to use 30 fps, we will sample the data at 30 fps as well.

**Custom sample rate:** This is the number of samples per second. For example if your Fbx file has a motion that was created at 30 fps, but you set this value to 15, we will sample the data at only 15 frames per second. This can reduce the quality of your motion as it will lose some high frequency details, but often it still looks good while it can significantly reduce the memory usage. If you provide a value that is higher than the original Fbx frame rate, for example 120, while the motion was created at 30 fps, then we will internally just sample at the rate provided by the Fbx file, so 30 in our example case.
</td>
  </tr>
  <tr>
    <th>Translation quality (%)</th>
    <td>The compression quality of the translation data. Higher values will match your DCC closer, but use more memory. In most cases only the root joint has translation data, so changing this setting won't have a massive impact.
</td>
  </tr>
    <tr>
    <th>Rotation quality (%)</th>
    <td>The compression quality of the rotation data. Higher values will match your DCC closer, but use more memory. Rotation data is the majority of the data, so changing this value will likely have most impact.
</td>
  </tr>
    <tr>
    <th>Scale quality (%)</th>
    <td>The compression quality of the scale data. Higher values will match your DCC closer, but use more memory. Only in very rare cases is scale animated, so changing this setting will likely have no impact on most motions.
</td>
  </tr>
    <tr>
    <th>Allowed memory overhead (%)</th>
    <td>Only used when "**Automatic**" mode is selected as the motion data type. This is the percentage of allowed memory usage overhead between the evenly spaced keyframes and reduced keyframes methods. If the additional memory usage of the high performance method (evenly spaced keyframes / UniformMotionData) is less or equal than this percentage compared to the slower but more memory efficient method (Reduced keyframes / NonUniformMotionData) then the automatic mode will prefer and pick the high performance method.
</td>
  </tr>
    <tr>
    <th>Keep duration</th>
    <td>When enabled this keep the duration the same as the Fbx motion duration, even if no joints are animated. When disabled and the motion doesn't animate any joints then the resulting motion will have a duration of zero seconds.
</td>
  </tr>
</table>

### Inside the animation editor

You can see what kind of motion data is used inside the Motion Set window. If you want to reduce memory, try forcing more motions to be saved as "Reduced Keyframes" (NonUniformMotionData) inside the Fbx settings. If you want higher performance, force more motions to use "Evenly Spaced" (UniformMotionData).

To increase performance in trade for memory you can also try increasing the "Allowed memory overhead" values inside the motion sampling modifier inside the Fbx settings.

To decrease memory usage and file size in trade for performance you can also decrease the quality for motions. Try decreasing the rotation quality percentage first, and make sure the motion data type saved is the "Reduced keyframes" one, to make sure the quality settings have any effect at all.

![image](/Images/Image5.png)

##### Updated Aug 2022