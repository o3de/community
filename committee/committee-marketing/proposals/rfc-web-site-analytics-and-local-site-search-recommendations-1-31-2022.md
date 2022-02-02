# Request for Comment: Proposal to fund improved site analytics and local site search

Submitted by: Doug Erickson

Revision History:

* First draft for review, 1/31/2022, Doug Erickson

## Summary:

As of 1/5/2021, we have 2 major improvements we'd like to make to the O3DE.org website: support for advanced web analytics; and support for server-based local site search.
Currently, for basic analytics, we rely on the basic features provided by our Netlify service instance's "Analytics" pane. This provides the bare minimum for web metrics: page views, visitors, referrals, visitor regions, top accessed pages. It provides for a 30-day rolling window of metrics and does not retain historical data. This is insufficient for the deeper opportunity analysis and reporting needed by the Marketing committee and O3DE partners, like AWS.

For local site search, O3DE.org currently uses the Lunr local search package, which does not require a separate search service but also inhibits site build and access performance, and returns static results based on simple heuristics. Adding local site search based on a modern indexing approach will improve the quality of results for customers and improve performance of the site (especially for documentation searches) as the site continues to grow.
Since we cannot instrument and collect in-product analytics, analytics from both global search and local site search&mdash;provided by both tools&mdash;can be used to gain more customer insight for development strategies, as well.

We would like to request funding from the O3D Foundation to purchase subscriptions to 2 services, respectively, to improve the overall site experience for our customers and to gather the analytics we need to make targeted improvements and understand O3DE contributor and customer experiences.


### Analytics

**DataDog**: DataDog is a cloud monitoring and analytics platform that has relatively straightforward, out-of-the-box integration support for Netlify. It is frequently used as the analytics solution for Linux FOundation Netlify-based sites.

**Why DataDog**: https://www.datadoghq.com/blog/monitor-netlify-with-datadog/ 
Integration Overview: [DataDog Analytics for Netlify Static Site Services](https://docs.datadoghq.com/integrations/netlify/?_gl=1*1nilt0s*_ga*MTI3NTE0MzM4OS4xNjQxNDA0NDcy*_ga_KN80RDFSQK*MTY0MTQwNDQ3Mi4xLjEuMTY0MTQwNDUyMi4w&_ga=2.214270935.1342909212.1641404473-1275143389.1641404472)

* Log Drain docs: https://docs.netlify.com/monitor-sites/log-drains/ 
* There are out-of-the-box Netlify-specific dashboards for ingested web log data.

**Cost**: [DataDog Log Analytics Pricing Page](https://www.datadoghq.com/pricing/?_gl=1*le1t40*_ga*MTI3NTE0MzM4OS4xNjQxNDA0NDcy*_ga_KN80RDFSQK*MTY0MTQwNDQ3Mi4xLjEuMTY0MTQwNDUzOC4w&product=real-user-monitoring#real-user-monitoring)

* Ingestion only ($0.10 per GB/month)
* 30-Day retention ($2.50 per million log events/month)
* Estimated monthly spend:
  * For 10 GB log volume + 1M monthly events: $1.00 + $2.50 = $3.50/mo
  * For 1TB log volume + 100M monthly events $100.00 + $250.00 = $250/mo

### Local Site Search

**Algolia**: "With Algolia Search, developers can rely on a simple and robust API to build the experiences at the core of their companies' applications. It democratizes the power of API building blocks with management UIs necessary to optimize user experiences and drive business results. From eCommerce sites to virtual reality productivity tools, Algolia Search powers search and discovery experiences anywhere."

**Why Algolia**: Algolia is a cloud-based local site search service that has a well-documented plug-in for use with Netlify-based sites. Besides an improved search experience for users, Algolia provides solid analytics that can be used to better tailor the docs to support local search experiences.

**Integration Overview**: https://www.algolia.com/doc/tools/crawler/netlify-plugin/quick-start/ 

* Local site search analytics: https://www.algolia.com/doc/guides/getting-analytics/search-analytics/out-of-the-box-analytics/ 

**Cost**: https://www.algolia.com/pricing/ 

* Search support: $1.00 per 1000 requests/mo + 1000 records
* (optional) Recommendations support: $0.60 per 1000 requests/mo
* Estimated cost (based on current Lunr data): $20.00/mo



## What are the advantages of the suggestions?

DataDog: We lack good analytics to better understand our contributors and customers as they view O3DE.org and our marketing/documentation. With DataDog, we get deep, datalake-based analytics that we can customize and deep dive on, using a platform used across many other Linux FOundation sites.

Our current Lunr-based local site search adds a large processing overhead that slows publishing times and browse experiences, and customer feedback signals that readers are dissatosfied with the results it returns. With Algolia, we get a cloud-based service that produces much better local site search results with minimum overhead on web server (Netlify) performance.

## What are the disadvantages of the suggestions?

* They both cost money for subscriptions, roughly estimated to be around $250/month.

## How will this work within the O3DE project?

* Both platforms (DataDog and Algolia) are used across Linux Foundation, Netlify-based sites. They are both easy to configure and allow easy customizations, and both have API support for further use cases.

## What is the strategy for adoption?

1. Get approval to purchase subscriptions to these two services from the TSC.

2. LF/O3DE purchases and owns those subscriptions.

3. O3DE sig-infra develops basic use cases for manual testing to confirm successful integration.

4. LF/O3DE integrates these services transparently and managed as a project.

5. O3DE community tests these features based on the defined use cases.

6. Roll it out! Follow-up surveys with community should be considered.