# Pali sanksrit keyboard for linux

A linux keyboard for typing pāli and sanskrit diactrics ( i.e ā ī ū ē ō ñ ṭ ḍ ṇ ḷ ḥ ś ṣ ṛ ṝ ṃ ŋ ṁ √ ) .

## Instructions
1. Copy the file `pi` into `/usr/share/X11/xkb/symbols` .
2. Navigate to `/usr/share/X11/xkb/rules` .
3. Add the following lines of code above `</layoutList>` in `evdev.xml` and `base.xml` .
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
4. Reboot .
5. Open system settings > keyboard > layouts . 
3. Click '+' to add a langauge .
4. Search `Pali` and add it .
11. Type pāli āṇḍ śāṇśkṛīṭ diactrics with shift key . 

#### You can use the `us` keybaord to overwrite your existing us keybaord in `/usr/share/X11/xkb/symbols` , and type diacritics with the `right alt` key . 
