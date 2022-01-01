# pali sanksrit keyboard for linux

a linux keyboard for typing pāli and sanskrit diactrics using the shift key ā ī ū ē ō ñ ṭ ḍ ṇ ḷ ḥ ś ṣ ṛ ṝ ṃ ŋ ṁ √

instructions
2. open a terminal and copy the file "pi" into into `/usr/share/X11/xkb/symbols` for example
   `sudo cp /home/*your user name*/pi /usr/share/X11/xkb/symbols/`
4. open system settings> keyboard > layouts 
5. click + to add a langauge
6. type pali and add it
7. navigate to /usr/share/X11/xkb/rules
8. open a terminal and type
  `sudo gedit evdev.xml`
9. search for `<layoutList>`
10. add the following lines of code beneath that
````
<layout>
      <configItem>
        <name>pi</name>
        <shortDescription>pli</shortDescription>
        <description>Pali</description>
        <languageList>
          <iso639Id>pi</iso639Id>
        </languageList>
      </configItem>
      <variantList/>
</layout>
````
11. repeat steps 7-10 for `base.xml`
12. use your keboard to type pāli āṇḍ śāṇśkṛīṭ ḍīācṛīṭīcś ūśīṇg ṭḥe śḥīfṭ key. 
