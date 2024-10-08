---
layout: default
title: Saving Your Value
nav_order: 5
parent: Pressure Advance / Linear Advance
grand_parent: Tuning
---

{% comment %}

# This page has moved! Please visit [the new location](https://ellis3dp.com/Print-Tuning-Guide/articles/pressure_linear_advance/saving.html).

{% endcomment %}

# Saving Your Value

---

{: .compat}
:dizzy: This page is compatible with Klipper, Marlin, and RepRapFirmware.

{: .prereqs}
> - ![]({{ "/assets/img/marlin_small.png" | absolute_url }}) **Marlin**: Linear advance must be [:page_facing_up: enabled in firmware](https://marlinfw.org/docs/configuration/configuration.html#linear-advance). Not all printers have it enabled by default. 

---

![]({{ "/assets/img/klipper.png" | absolute_url }})

- In the `[extruder]` section of your config, update `pressure_advance` to the new value and issue a `RESTART`.

  - Alternatively:

  - In **PS/SS**, you can manage this per-filament by putting `SET_PRESSURE_ADVANCE ADVANCE=`\<value> in your custom filament g-code.
    - You can also set different values for different nozzle sizes using [:page_facing_up: this](https://github.com/AndrewEllis93/Ellis-SuperSlicer-Profiles#changing-pa-based-on-nozzle-size).
  - In **Cura**, you can set it during slicing using [:page_facing_up: this plugin.](https://github.com/ollyfg/cura_pressure_advance_setting)

---

![]({{ "/assets/img/marlin.png" | absolute_url }})

- Place `M900 K`\<value\> in your filament g-code (same as above). This must be set each time.

- You can save a permanent default to the firmware by modifying Configuration_adv.h and reflashing the firmware. Instructions in the "Saving the K-Factor in the Firmware" section [:page_facing_up: here](https://marlinfw.org/docs/features/lin_advance.html).

- In **Cura**, you can set it during slicing using [:page_facing_up: this plugin.](https://github.com/fieldOfView/Cura-LinearAdvanceSettingPlugin)

---


![]({{ "/assets/img/duet.png" | absolute_url }})

- Place `M572 S`\<value\> in your filament g-code (same as above) or in your start macro. This must be set each time.
