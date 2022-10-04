
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
    