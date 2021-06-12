# Install on Linux

Put the following text block inside `/usr/share/X11/xkb/symbols/tr`

```
// github.com/salif/colemak-tr
partial alphanumeric_keys
xkb_symbols "colemak" {

  include "us(colemak)"

  name[Group1]= "Turkish (Colemak)";

  key <AD01> {[ odiaeresis,  Odiaeresis,  q, Q ]};
  key <AD02> {[ scedilla,    Scedilla,    w, W ]};
  key <AD10> {[ gbreve,      Gbreve            ]};
  key <AD11> {[ udiaeresis,  Udiaeresis        ]};
  key <AC09> {[ i,           Iabovedot         ]};
  key <AC11> {[ idotless,    I                 ]};
  key <AB02> {[ ccedilla,    Ccedilla,    x, X ]};

  include "level3(ralt_switch)"
};
```

Put the following text block inside `/usr/share/X11/xkb/rules/evdev.xml`

```
<variant>
  <configItem>
    <name>colemak</name>
    <description>Turkish (Colemak)</description>
  </configItem>
</variant>
```

Then add `Turkish (Colemak)` via your desktop environment's settings.

If it doesn't work then create an issue on this repository
