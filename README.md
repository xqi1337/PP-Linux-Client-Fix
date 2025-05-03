# PP-Linux-Client-Fix

Habt ihr euch auch gefragt was mit dem Perfect Privacy Client für Linux nicht stimmt?

 

Ich hab es für euch rausgefunden!

 

 

 

 

 

Als erstes gir1.2 installieren

wget http://ftp.ru.debian.org/debian/pool/main/liba/libappindicator/gir1.2-appindicator3-0.1_0.4.92-7_amd64.deb
sudo dpkg -i gir1.2-appindicator3-0.1_0.4.92-7_amd64.deb
 

 

Dann öffnet ihr folgende Datei (in dem Beispiel mit nano):

nano "/opt/perfect_privacy/perfect-privacy-vpn/perfect_privacy_vpn_lib/Builder.py"
 

Dann änder sucht ihr:

ele_widgets = tree.getiterator("object")
und ändert es zu

ele_widgets = tree.iter("object")
 

Weils so schön war sucht ihr jetzt nochmal folgendes:

 

ele_signals = tree.getiterator("signal")
und ändert es in:

ele_signals = tree.iter("signal")
 
