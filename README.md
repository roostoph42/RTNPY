# RTNPY
## Remote Telescope Nong Pok Yai

![](assets/RTNPY_Observatory.png)  
Image AI generated

---

## A Window to the Southeast Asian Sky

Deep in rural Thailand, far from European light pollution, a remotely operated observatory is taking shape — dedicated to the observation of dynamic events in our Solar System. While Europe sleeps, RTNPY gazes into the clear tropical sky. And you? You sit comfortably at home with a cup of coffee, watching the data come in.

### Why Thailand?

- **Time offset of +5/+6 hours:** Astronomical events that occur in European daylight take place at convenient observing hours over Nong Pok Yai.
- **Geographic complementarity:** Occultation paths that miss Europe frequently sweep across Southeast Asia.
- **Climate:** The dry season from November through February offers a surprising number of clear nights with calm seeing.
- **Low geographic latitude:** Objects of the southern celestial hemisphere and the ecliptic rise much higher above the horizon than they ever do from Central Europe.

### Scientific Objectives

The observatory is designed for **time-critical, high-precision photometry**:

- **Stellar occultations by minor planets (asteroids):** Millisecond-accurate light curve measurements to determine size, shape and possible companions.
- **Mutual events of the Galilean moons:** Eclipses and occultations among Io, Europa, Ganymede and Callisto.
- **Lunar occultations of stars:** Especially grazing occultations and occultations of bright stars.
- **Exoplanet transits** as well as variable and eclipsing binary stars.
- **Comets and Near-Earth Objects (NEOs):** Astrometry and photometry.

---

## Proposed Equipment

The following list outlines a setup that meets the scientific objectives while satisfying the demands of a fully remote-controlled robotic observatory.

### Optics — the Eye of the Observatory

| Component | Recommendation | Rationale |
|---|---|---|
| Main telescope | Ritchey-Chrétien 14" (356 mm), f/8 | Large aperture, flat field, coma- and chromatic-aberration-free imaging for photometry |
| Guide scope / finder | APO refractor 80/480 mm | Alternative to off-axis guiding; wide-field search and astrometry |
| Reducer/flattener | 0.67× reducer (f/5.4) | Wider field of view and shorter exposures for occultation work |

### Mount — the Backbone

- **Direct-drive mount** (e.g. ASA DDM85, 10Micron GM2000 HPS or Planewave L-500): absolute encoders, no periodic error, payload capacity ≥ 50 kg, pointing model suitable for unattended operation.
- **Massive pier** thermally decoupled from the building floor.

### Sensors — the Retina

| Purpose | Camera |
|---|---|
| Science camera (photometry/astrometry) | Cooled CMOS, e.g. ZWO ASI6200MM Pro or QHY600M (full frame, 16 bit, low read noise) |
| High-speed occultation camera | QHY174M-GPS or ASI174MM with GPS module for absolute time stamps below 1 ms |
| Autoguider | ZWO ASI220MM Mini or equivalent |
| All-sky camera | ZWO ASI224MC + fisheye lens for cloud monitoring |

### Filter Wheel and Filters

- **Filter wheel** with 7 positions, motorized.
- **Photometric filters:** Johnson-Cousins B, V, R, I and Sloan g', r', i'.
- **Narrowband filters** Hα, OIII, SII for supplementary imaging sessions.
- **Luminance / IR-cut filter** for occultation observing with maximum SNR.

### Time — the Most Important Measurement

- **GPS-disciplined time server** (e.g. Meinberg LANTIME) with PPS output.
- **Camera with hardware GPS trigger** — mandatory for asteroidal stellar occultations.
- NTP synchronization of all control computers against the local GPS server.

### The Dome — Built on Site

Rather than a conventional roll-off roof, RTNPY will be housed under a **classical observatory dome** — exactly as depicted in the rendering above. The dome offers superior protection against tropical wind, driving monsoon rain and the intense daytime sun, while a narrow shutter slit shields the optics from local stray light and dewfall.

A particular strength of this project: **the dome will be designed and built by local Thai craftsmen.** Thailand has a long tradition of skilled metalwork, fiberglass fabrication and precision carpentry. Building on site means:

- **Lower cost** than shipping a commercial dome halfway around the world.
- **Local know-how** for ongoing maintenance and repairs.
- **Community involvement** — the observatory becomes a local landmark, not a foreign installation.
- **Custom adaptation** to the climate, the pier geometry and the specific telescope.

The dome will feature a motorized rotation drive, motorized shutter, safety limit switches and full ASCOM/Alpaca integration for remote control.

### Infrastructure — Around the Dome

- **Weather station:** cloud sensor (Boltwood Cloud Sensor III), rain sensor, anemometer, hygrometer, temperature, sky brightness (SQM).
- **UPS** providing at least 30 minutes of backup — graceful shutdown on power loss.
- **Climate-controlled electronics room** separated from the optics (tropical climate!).
- **Redundant internet connection:** fiber as primary, 4G/5G as backup.
- **Remote-controlled power distribution** (PDU) — every component individually switchable.
- **Surveillance cameras** with infrared illumination for visual checks from afar.

### Software Stack

- **Acquisition / control:** N.I.N.A., Voyager or ACP Expert
- **Plate solving:** ASTAP or PlateSolve2
- **Photometry / analysis:** Tangra (occultations), AstroImageJ (transits), Muniwin
- **Weather / safety logic:** custom automation with hard-abort on clouds or rain
- **Remote access:** VPN plus remote desktop, redundantly secured

---

## What You Can Expect

Picture this: It is 7 p.m. in Central Europe. In Thailand, it is one in the morning. The sky stands clear and steady at the zenith. A 14-inch mirror gathers the light of a 12th-magnitude star — and in exactly 47 seconds, an 80-kilometer asteroid beyond Mars will extinguish its light for 4.2 seconds. You watch the star on your screen. The GPS-clocked camera counts the frames. And your measurement helps give shape, for the very first time, to a rock drifting through the outer Solar System.

**That is RTNPY.**

---

*Location: Nong Pok Yai, Thailand · Operated remotely from Europe*
