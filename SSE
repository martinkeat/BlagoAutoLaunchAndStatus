@ECHO OFF
title Miner Auto Launch - Status Checker
:StatusMiner


:: Filename of Blago Miner Version Used

SET BlagoVersion=BlagoMiner_SSE.exe

ECHO -------------------------------------------
ECHO Blago Miner Auto Launch And Status Checker by Spontaneocus
ECHO -------------------------------------------
ECHO.
ECHO.


:: Initiation of Status Check for Blago Miner

ECHO Initiating Status Check of "%BlagoVersion%"

TASKLIST | FINDSTR /I "%BlagoVersion%" >NUL
ECHO.
IF ERRORLEVEL 1 (GOTO :InitiateMiner) ELSE (ECHO Details of Last check)


:: Report of current Status of Blago Miner

ECHO -------------------------------------------
ECHO Date            Time            Status
ECHO -------------------------------------------
ECHO %DATE%     %time%      Mining
ECHO -------------------------------------------
ECHO.


:: Countdown to next check

ECHO Next Status Check (Every 5 Minutes):
timeout /t 300 /NOBREAK 
::PING localhost -n 20 >NUL
CLS
GOTO :StatusMiner


:: Procedure for starting Blago Miner if not already started. 

:InitiateMiner
ECHO Status checker has confirmed that blago miner is not running. 
timeout /t 2 /NOBREAK
ECHO Please standby - Starting Blago Miner...
start %BlagoVersion%
PING localhost -n 6 >NUL
CLS
GOTO :StatusMiner
