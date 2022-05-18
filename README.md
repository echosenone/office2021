# Office 2021 is Here!


![office](Microsoft_Office_365_Logo_white_text-700x425.png)
![classic](Microsoft_Office_365_Logo_black_text-700x172.png)
# Office 2021 Pro Plus
Download Office 2021 on GitHub, yes it's legal.
This installs and activates Office!

## Activation
I recommend running activation after 180 days or if says it is not valid.

# Q: How do I install?
A: So the original config *configuration-office* has project and visio removed. If you want those features, use the name from the configuration-office file and overwrite the file.
A: Assuming you have the files, you can run the bat file.


Run the bat when you are ready.

---


# Q: Can I activate on my own?
Yeah, for sure you can. That is why I did not make activation automatic. You may skip that and activate on your own.

Q: The KMS Servers are down, what servers can I use?

A: Haha, I made KMS servers a while ago.
A: Here it is: k1.4kash.org k2.codelazy.org k3.linux4kash.com

---

# Q: How do I activate? It keeps saying Office activation off.
So it might be a bug, im fixing it but for now

Put this text below in a notepad and save as a .bat

---
@echo off
title Activate Office 365 ProPlus for FREE - codelazy.org.com&cls&echo =====================================================================================&echo #Project: office 2021 on github activator &echo =====================================================================================&echo.&echo #Supported products: Office 365 ProPlus (x86-x64)&echo.&echo.&(if exist "%ProgramFiles%\Microsoft Office\Office16\ospp.vbs" cd /d "%ProgramFiles%\Microsoft Office\Office16")&(if exist "%ProgramFiles(x86)%\Microsoft Office\Office16\ospp.vbs" cd /d "%ProgramFiles(x86)%\Microsoft Office\Office16")&(for /f %%x in ('dir /b ..\root\Licenses16\proplusvl_kms*.xrm-ms') do cscript ospp.vbs /inslic:"..\root\Licenses16\%%x" >nul)&(for /f %%x in ('dir /b ..\root\Licenses16\proplusvl_mak*.xrm-ms') do cscript ospp.vbs /inslic:"..\root\Licenses16\%%x" >nul)&echo.&echo ============================================================================&echo Activating your Office...&cscript //nologo slmgr.vbs /ckms >nul&cscript //nologo ospp.vbs /setprt:1688 >nul&cscript //nologo ospp.vbs /unpkey:WFG99 >nul&cscript //nologo ospp.vbs /unpkey:DRTFM >nul&cscript //nologo ospp.vbs /unpkey:BTDRB >nul&set i=1&cscript //nologo ospp.vbs /inpkey:XQNVK-8JYDB-WJ9W3-YJ8YR-WFG99 >nul||cscript //nologo ospp.vbs /inpkey:NMMKJ-6RK4F-KMJVX-8D9MJ-6MWKP >nul||goto notsupported
:skms
if %i% GTR 10 goto busy
if %i% EQU 1 set KMS=kms7.MSGuides.com
if %i% EQU 2 set KMS=s8.uk.to
if %i% EQU 3 set KMS=s9.us.to
if %i% GTR 3 goto ato
cscript //nologo ospp.vbs /sethst:%KMS% >nul
:ato
echo ============================================================================&echo.&echo.&cscript //nologo ospp.vbs /act | find /i "successful" && (echo.&echo ============================================================================&echo.&echo #My official blog: MSGuides.com&echo.&echo #How it works: bit.ly/kms-server&echo.&echo #Please feel free to contact me at msguides.com@gmail.com if you have any questions or concerns.&echo.&echo #Please consider supporting this project: donate.msguides.com&echo #Your support is helping me keep my servers running 24/7!&echo.&echo ============================================================================&choice /n /c YN /m "Would you like to visit my website [Y,N]?" & if errorlevel 2 exit) || (echo The connection to my KMS server failed! Trying to connect to another one... & echo Please wait... & echo. & echo. & set /a i+=1 & goto skms)
explorer "http://codelazy.org"&goto halt
:notsupported
echo ============================================================================&echo.&echo Sorry, your version is not supported.&echo.&goto halt
:busy
echo ============================================================================&echo.&echo Sorry, the server is busy and can't respond to your request. Please try again.&echo.
:halt
pause >nul

---
