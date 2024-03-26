# @@@ ABORTED @@@
(why: see last section)


# Intro
Modern Hard Disk Drives is facinating due to their extremely precise hardware yet low cost.

By spending $20 on 7200RPM WD Blue HDD you can buy the most advanced mechanical devise you can get at retail at all. And this device will include:
- high-quality CNC'ed aluminum casing;
- [MU-metal](https://en.wikipedia.org/wiki/Mu-metal) plates, pins and washers;
- ultra-flat and high reflective aluminum discs;
- [fluid dynamic bearing](https://en.wikipedia.org/wiki/Fluid_bearing) from the main spindle combined with brushless motor that with high accuracy mount;
- ball bearing in HDD's arm axis;
- micro- and nano- piezoelectric actuators in the sliders;

I'm sure that this hardware could substitute expensive parts for DIY projects. And it already is:
- https://hackaday.com/2023/05/12/laser-projector-built-from-an-old-hard-drive/

I'm really interested in exploring all other possible ways to use all this hardware.

In this project I'm focused on studying the piezos in general, the HDD's piezos, the ways to control them, the ways to measure them.

# Harware intro
Used HDD -- WD10EZEX. 
- [WD10EZEX teardown](https://www.ifixit.com/Teardown/WD+Blue+Hard+Drive+Teardown/159818)
- [WD piezo actuators intro from WD](https://documents.westerndigital.com/content/dam/doc-library/en_us/assets/public/western-digital/collateral/tech-brief/tech-brief-hgst-micro-actuator.pdf)
# Theory

- [Piezoelectric actuator theory #1](https://fab.cba.mit.edu/classes/865.18/motion/piezoelectric/index.html)
- [Piezoelectric actuator theory #2](https://xeryon.com/technology/how-do-piezo-motors-work/)

Selected topics:
1. Resonanse frequency.
-- [link1](https://www.pi-usa.us/en/products/piezo-flexure-nanopositioners/piezo-motion-control-tutorial/tutorial-4-25)

# Extras
- Electrorestriction is similar to piezoeffect.

High voltage generation:
- [Example of micro piezo driver](https://www.piezodrive.com/modules/pdu100-micro-piezo-driver/), looks sweet, but expensive. I believe that similar driver could be build using $10 components.
- High voltage integrated switch boost regulator probably could be used to generate high voltage to control the piezos.
- Ways to generate high voltage for piezos: [1](https://ww1.microchip.com/downloads/en/AppNotes/91053b.pdf), [2](https://www.instructables.com/High-Voltage-Switch-Mode-Power-Supply-SMPSBoost/), [3](https://www.instructables.com/High-Voltage-Power-Supply-for-Nixie-and-Valve-Tube/)

- [LIGO: Build Your Own Michelson Interferometer](https://dcc.ligo.org/public/0117/T1400762/001/interferometer_2014.pdf)
- [SMD X7R capasitors as piezoelectric actuators](https://dberard.com/2015/08/16/mlcc-piezo-actuators/) with 300-800nm deformation

- Vaporizer piezos are much stiffer than buzzer piezos


# (?_?) why aborted
**in the upper section actual progress should be added
After opening an actual HDD with piezos inside I encountered three substential problems why this couldn't be done in the planned way.

1. Size of used piezos.

They are too small to be useful. See also Table 1 on https://doi.org/10.1007/s00542-023-05460-7.
Size of the single piezo is less than 1mm * 1mm * 0.2mm. This is not enough to create any kind of useful actuation force (!a research need tbd here!).

2. Resonant frequency.
? as a consequence from previous item: ? resonance frequency of actuator system based on the piezos from HDD is too small to achieve ultrasonic working mode resultin in slow actuation speed and really unfancy high-pitch noise.

> The way to overcome problems 1 and 2: use more suitable piezocrystals. So no HDD :(

>But it seems that these crystals is pretty cheap (~ tens of $) if bought on Aliexpress. Custom crystals means custom design of the actuator not fixed to HDD arm design.

>Along with that more mundane source of piezocrystals could be considered; and only two ideas comes to my mind: buzzers and evaporizers.

3. Michelson interferometer.
No success in attempt to build it on the table because of the environment vibrations with amplitude large than lambda/2.


>I see two possible ways to move further in this direction:
>- find stable platform: close to optical table or optical table
>- create interferometer with rigid body so relative vibrations will be negligible

# TBD
- post all existing progress
- reformat current notebook so new versions of file is on top
- do physics review
