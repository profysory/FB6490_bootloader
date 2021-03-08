# FB6490_bootloader
bootloader (FRITZ.Box_6490_Cable) from eMMC (25L1606E)
Hardware:	CH341A - USB Programmer
Software:	AsProgrammer.exe
======================================================
Wenn bootloader Ihren FritzBox funktioniert nicht mehr:

1. auslöten Sie eMMC (25L1606E) von Ihre FritzBox;
2. probieren Sie Daten von eMMC (25L1606E) auszulesen und, wenn möglich ist, ihre Daten (tr069_passphrase, tr069_serial) zu speichern;
3. offnen "bootloader_6490.image" aus "bootloader_6490.zip" z.b. in Notepad++;

4. nachsuchen = CC:CE:1E:XX:XX:XX
======================================================
CC:CE:1E = das zeichnen Branding AVM
IR = Ihre Daten
======================================================
CM-MAC:         CC:CE:1E:XX:XX:XX = CC:CE:1E:IR:IR:IR

macdsl          CC:CE:1E:XX:XX:XX = CC:CE:1E:IR:IR:IR
usb_board_mac   CC:CE:1E:XX:XX:XX = CC:CE:1E:IR:IR:IR
usb_rndis_mac   CC:CE:1E:XX:XX:XX = CC:CE:1E:IR:IR:IR
maca            CC:CE:1E:XX:XX:XX = CC:CE:1E:IR:IR:IR
macb            CC:CE:1E:XX:XX:XX = CC:CE:1E:IR:IR:IR
macwlan         CC:CE:1E:XX:XX:XX = CC:CE:1E:IR:IR:IR
macwlan2        CC:CE:1E:XX:XX:XX = CC:CE:1E:IR:IR:IR
======================================================
muss man nachsuchen und überschreiben:
drei Block (21 nicht hintereinander) mac adress:

CC:CE:1E:XX:XX:XX
CC:CE:1E:XX:XX:XX
CC:CE:1E:XX:XX:XX
CC:CE:1E:XX:XX:XX
CC:CE:1E:XX:XX:XX
CC:CE:1E:XX:XX:XX
CC:CE:1E:XX:XX:XX

CC:CE:1E:XX:XX:XX
CC:CE:1E:XX:XX:XX
CC:CE:1E:XX:XX:XX
CC:CE:1E:XX:XX:XX
CC:CE:1E:XX:XX:XX
CC:CE:1E:XX:XX:XX
CC:CE:1E:XX:XX:XX

CC:CE:1E:XX:XX:XX
CC:CE:1E:XX:XX:XX
CC:CE:1E:XX:XX:XX
CC:CE:1E:XX:XX:XX
CC:CE:1E:XX:XX:XX
CC:CE:1E:XX:XX:XX
CC:CE:1E:XX:XX:XX

webgui_pass = toptop9999
webgui_pass = ihre-daten

wlan_key = 99999999999999999999
wlan_key = ihre-----------daten

tr069_passphrase = xxxxxxxxxxxx
tr069_passphrase = ihre---daten

tr069_serial = XXXXXX-XXXXXXXXXXXX
tr069_serial = ihreee-datennnnnnnn
================================================
5. speichern Sie Daten als ihre bootloader;
6. sreiben Sie Daten zu eMMC (25L1606E);
7. einlöten eMMC (25L1606E);
8. neustarten ihre FritzBox.
================================================
