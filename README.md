## Description
- A linux keyboard for typing pāli and sanskrit diactrics ( i.e ā ī ū ē ō ñ ṭ ḍ ṇ ḷ ḥ ś ṣ ṛ ṝ ṃ ŋ ṁ √ ) .
- Type diactrics with left alt key as modifier (ṅ = lefht alt + b, ñ = left alt + y, ŋ = left alt + <) . 

## Install on X11 (will be overwritten if you upgrade system)
  - Install as a alternative layout of us ( easiest ).
    > 1.`sudo mv /usr/share/X11/xkb/symbols/us /usr/share/X11/xkb/symbols/us.backup` .  
    > 2.`sudo mv us-pali /usr/share/X11/xkb/symbols/us` .  
    > 3. reboot .  

  - Install as a optional layout .
    > 1.`sudo mv us-pali /usr/share/X11/xkb/symbols/pi` .  
    > 2.under /usr/share/X11/xkb/rules, add layout item to evdev.xml and base.xml's <layoutList> tag.  
    ```
      <layout>
        <configItem>
          <name>pi</name>
          <shortDescription>us-pali</shortDescription>
          <description>us-pali</description>
          <languageList>
            <iso639Id>pi</iso639Id>
          </languageList>
        </configItem>
        <variantList/>
      </layout>
    </layoutList>
    ```
    > 3.reboot .  
    > 4.open system settings > keyboard > layouts .  
    > 5.click '+', search and active `us-pali` .

## Install on sway
  1. `mkdir -p ~/.xkb/symbols`
  2. `mv us-pali ~/.xkb/symbols` .
  3. add relevant snippet in the sway config file .
  ```
  input type:keyboard {
    xkb_layout us-pali
  }
  ```
  4. reboot .

## Config
  - Instead of left alt key, you can set right alt key as the modifier by replace `lalt_switch` with `ralt_switch` in us-pali .
