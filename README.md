# pali sanksrit keyboard for linux

a linux keyboard for typing pāli and sanskrit diactrics using the shift key ā ī ū ē ō ñ ṭ ḍ ṇ ḷ ḥ ś ṣ ṛ ṝ ṃ ŋ ṁ √

instructions
1. open a terminal and copy the file `pi` into into `/usr/share/X11/xkb/symbols` for example\
`sudo cp /home/*your user name*/pi /usr/share/X11/xkb/symbols/`
2. open system settings> keyboard > layouts 
3. click + to add a langauge
4. type pali and add it
5. navigate to `/usr/share/X11/xkb/rules`
6. open a terminal and type
  `sudo gedit evdev.xml`
7. search for `<layoutList>`
8. add the following lines of code beneath that
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
9. repeat steps 5-8 for `base.xml`
10. use your keboard to type pāli āṇḍ śāṇśkṛīṭ ḍīācṛīṭīcś ūśīṇg ṭḥe śḥīfṭ key. 

you can use the `us` keybaord to overwrite your existing us keybaord and type diacritics with the `alt` key 
