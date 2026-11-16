# Murmuration

**Try it:** https://sarahfoxall.github.io/murmuration/

Two tools on one page. Switch between them with the bar at the top:

- **Animated** ([#animated](https://sarahfoxall.github.io/murmuration/#animated)): a flock that flies across the frame, for video.
- **Still** ([#still](https://sarahfoxall.github.io/murmuration/#still)): static murmuration images. See [Murmuration still](#murmuration-still).

Each tool keeps its settings while you switch.

A starling murmuration you can shape and export. The flock swoops in from the left on long, broad arcs, morphing gradually as it crosses the frame, and leaves on the right. The motion is built on field research into real starling flocks.

## Use it

Open the link above, or open `animated.html` directly, in Chrome, Edge or Firefox. Safari works for viewing; video recording depends on browser support. It's a single file, with no install, no server and no external assets.

- **Timeline:** play, pause and restart, and drag the scrubber to any point in the flight.
- **Record video (WebM):** records the whole flight at full resolution. It starts and ends on an empty frame, so it also loops cleanly. Keep the tab visible while it records.
- **Save frame (PNG):** saves the current frame at full resolution.

## Controls

| Section | Controls |
|---|---|
| Colours | Background, Dots |
| Flock | Dots, Dot size, Flock size, Twist and fold (how much the shape changes), Morph speed (how fast it changes), New flock (new birds and a new route) |
| Motion | Length (6–12 s), Turning (how much the route swoops up and down), Turn spread (how slowly each turn passes through the flock) |
| Output | Size (Slide 16:9, Social 4:5, Story 9:16, Square), Record video (WebM), Save frame (PNG) |

## How it moves

Each rule below comes from studies of real starling flocks:

- **A thin sheet.** Flocks are much thinner than they are wide or long, with proportions of roughly 1 : 3 : 6, and birds pack more tightly at the border than in the middle (Ballerini et al., 2008). The flock here is a 3D sheet with those proportions, seen in perspective from the ground. Much of its apparent change in shape and density comes from the sheet tilting towards and away from us. Edge-on, it collapses into a dense band.
- **Constant speed, equal-radius turns.** Starlings barely change speed, and each bird turns on a path parallel to its neighbours' rather than around a shared centre. So the flock keeps its orientation in the sky while its direction of travel swings: a wide, flat flock becomes long and narrow after a 90° turn (Hemelrijk & Hildenbrandt, 2011; Attanasi et al., 2015).
- **Turns travel through the flock.** A turn starts at one tip of the flock and sweeps through it like a wave, undamped and two to four times faster than the birds fly (Attanasi et al., 2014). Birds the wave hasn't reached yet carry straight on, which bends and stretches the flock mid-turn. **Turn spread** controls how slowly the wave travels.
- **Banking.** The flock banks into its turns.
- **Left out on purpose.** Real flocks also flash and shimmer as wings catch the light, including the dark bands that run through a flock when a falcon attacks (Hemelrijk et al., 2015). That proved too distracting here, so the brightness comes only from how densely the dots overlap.
- **Following the leaders.** Most of the flock's length trails along the route, with the birds behind following the leaders' path, so the flock bends into a ribbon through each swoop.
- **Constant change.** Moving currents inside the flock keep pushing parts of it out, stretching them, pouring birds from one side to the other and pulling them back in, so the outline never settles. Meanwhile the whole sheet tilts, folds and bends into crescents. **Twist and fold** sets how strong this is and **Morph speed** how fast.
- **Inertia.** Each dot follows its place with its own slight springy lag, so the movement stays soft rather than mechanical.

## Editing the code

The animation lives in `animated.html`: styles and the control panel at the top, the animation in the `<script>` at the bottom.

- `buildScene`: the route (a few slow waves, flown at constant speed), banking, and the slow timing of each shape change.
- `buildParticles`: where each bird sits in the sheet.
- `computeTargets`: the sheet's orientation and shape at a given moment, the turn delay for each bird, and perspective.
- `state` at the top of the script: the default settings.

## Murmuration still

**Try it:** https://sarahfoxall.github.io/murmuration/#still

A companion tool for static murmuration images for slides, social and web, at 1920 × 1080. It lives in `still/index.html` and is also a single file. `index.html` is the page with the switch at the top.

- **Shape:** five starting forms (Crescent, Sail, Ribbon, Ring, Cloud), then Width, Height, Bend, Twist, Fold, Viewing angle, Density balance and Edge softness.
- **Dots:** Flock size, Dot size and Depth shading (dots further back fade).
- **Placement:** position, rotation and horizontal flip.
- **Colour:** dot and background colours, two presets, or a transparent background.
- **Variation:** New variation reshuffles the birds. Save preset and Load preset store a look as a .json file.
- **Export:** PNG at 1× or 2×, or SVG, optionally without the background and cropped to the flock.

## References

- Ballerini, M. et al. (2008). Empirical investigation of starling flocks: a benchmark study in collective animal behaviour. *Animal Behaviour* 76, 201–215.
- Hemelrijk, C. K. & Hildenbrandt, H. (2011). Some causes of the variable shape of flocks of birds. *PLoS ONE* 6(8), e22479.
- Attanasi, A. et al. (2014). Information transfer and behavioural inertia in starling flocks. *Nature Physics* 10, 691–696.
- Attanasi, A. et al. (2015). Emergence of collective changes in travel direction of starling flocks from individual birds' fluctuations. *J. R. Soc. Interface* 12.
- Hemelrijk, C. K., van Zuidam, L. & Hildenbrandt, H. (2015). What underlies waves of agitation in starling flocks. *Behavioral Ecology and Sociobiology* 69, 755–764.

## Licence

Add a licence of your choice (MIT is a common pick for small tools) if you want others to reuse the code.
