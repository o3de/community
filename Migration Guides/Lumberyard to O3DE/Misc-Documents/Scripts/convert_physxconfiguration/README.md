    @echo off
    REM Place this script above the <dev_root> directory
    REM This script is used to convert the physicsconfiguration and physconfiguration 
    
    SETLOCAL EnableDelayedExpansion
    set "ScriptDir=%~dp0"
    set "ScriptDir=%ScriptDir:~0,-1%"
    
    REM Parse command line arguments for directory of SerializeContextTools
    set "BIN_DIRECTORY="
    :CmdLineArgumentsParseLoop
    if "%1"=="" goto CmdLineArgumentsParsingDone
            REM Argument is path to directory containing SerializeContextTools.exe
            set "BIN_DIRECTORY=%1%"
            shift
            goto GotValidArgument
        )
    :InvalidCommandArgument
        echo "%1" is an invalid argument, a directory containing the SerializeContextTools.exe must be supplied
        exit /b 1
    :GotValidArgument
        shift
    goto CmdLineArgumentsParseLoop
    :CmdLineArgumentsParsingDone
    
    set "SCTOOL=SerializeContextTools.exe"
    if NOT "%BIN_DIRECTORY%"=="" (
        set "SCTOOL=%BIN_DIRECTORY%\%SCTOOL%"
    )
    
    set "LY_PROJECTS=AutomatedTesting;AtomTest;CMakeTestbed;Helios;LargeWorldsTest;MultiplayerSample;PhysicsSamples;SamplesProject;StarterGame"
    
    for %%a in (%LY_PROJECTS%) do (
        %SCTOOL% convert --files=%ScriptDir%/dev/%%a/project.physicsconfiguration --ext=physicsconfiguration.setreg --json-prefix=/Amazon/Gems/PhysX/PhysicsConfiguration --regset= "/Amazon/AzCore/Bootstrap/sys_game_folder=%%a"
        %SCTOOL% convert --files=%ScriptDir%/dev/%%a/project.physxconfiguration --ext=physxconfiguration.setreg --json-prefix=/Amazon/Gems/PhysX/PhysXConfiguration  --regset="/Amazon/AzCore/Bootstrap/sys_game_folder=%%a"
        move /Y "%ScriptDir%\dev\%%a\project.physicsconfiguration.setreg" "%ScriptDir%\dev\%%a\Registry\physicsconfiguration.setreg"
        move /Y "%ScriptDir%\dev\%%a\project.physxconfiguration.setreg" "%ScriptDir%\dev\%%a\Registry\physxconfiguration.setreg"
    )
    
    @echo off