# ADSR

```
   /\D
 A/  \_____
 /      S  \R
/           \
```

An envelope generator with classic ADSR profile centered around the 555 timer, responsive to a gate input. Adjustable durations for attack, duration, and release; and adjustable voltage for the sustain portion.

The circuit here is based on the [Yusynth ADSR (newer version)](https://yusynth.net/Modular/EN/ADSR/index_latest.html) with minor tweaks to make it more Eurorack friendly. The changes I've made are thus:
* Selected resistors appropriate for +/-12V rails,
* Added polarity protection so that a backward power header doesn't fry anything (twin series schotty diodes: BAT54SL),
* Full surface mount design.

The Yusynth page is a treasure trove of information about this circuit that I am too amateur to claim as my own; please read that outstanding page before using this circuit. The page provides many details and other implementations of this circuit that you may find suitable.

The KiCAD project here uses the library/footprints [found in my companion repo](https://github.com/thismatters/EurorackKiCAD).


## Width

6hp on a standard 3U rack.

## Inputs

Accepts gate input via patch cable, has pushbutton for manual gating.
Four knobs set the shape of the envelope. A toggle switch sets the response of the envelope generator between fast and slow.

## Outputs

Envelope and inverted envelope outputs. LED visualizes the output signal.

## Vendors

There are part numbers in the [BOM](adsr.csv) for many of the parts (not for basic passives though) at the following vendors:

* [Mouser](https://www.mouser.com): Needs no introduction. Get your ICs from here (or [digikey](https://www.digikey.com)).
* [Tayda Electronics](https://www.taydaelectronics.com/): Good supplier for passive components; audio jacks, and potentiometers. Their audio jacks are slightly smaller than the thonkiconn from thonk.
* [Love My Switches](https://lovemyswitches.com/): Has [really good knobs](https://lovemyswitches.com/anodized-aluminum-knob-the-lo-fi-1-4-smooth-shaft-12-5mm-od/) to go on those potentiometers!
* [OSHPark](https://oshpark.com/): Fast and (relatively) cheap PCB manufacturer. I haven't done a prototype run yet... stay tuned.
