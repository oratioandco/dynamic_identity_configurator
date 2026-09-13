# Werkstatt Gottesdienst — a generative church identity

**One building, endless posters.** A dynamic identity generator designed for a Berlin church — every regeneration produces a poster that has never existed before, yet is unmistakably the same brand.

**[▶ Try it live](https://oratioandco.github.io/dynamic_identity_configurator/)**

![The configurator in action — regenerating the design, retuning the colors, downloading the result](/assets/img/configurator-demo.gif)

---

## The brief

St. Johannes Evangelist sits on Auguststraße in Berlin-Mitte — gallery row. A beautiful old building with a signature look and a lot of architectural detail, and across the street, its own gallery. The church runs events of every kind, and each one needs a poster, an invitation, a flyer.

A fixed logo could never carry that variety. The identity needed to be as plural as the congregation itself.

## The idea

Express church as a mosaic: a diverse group of people with different walks of life, one common spirituality.

The building itself became the metaphor. Its facade — arched windows, the rose window, the portal — was drawn as a vector from photography, then broken apart into separate elements. No single element is the identity. The identity is the way the pieces come together, and the pieces come together differently every time.

The facade before the break-up:

![Vectorized church front](/assets/img/vectorshape.png)

## The system

Two dials drive everything:

- **Threshold** — each element rolls a random number. Below the threshold, it appears; above, it's gone. Low threshold: a sparse, quiet facade. High: the full building.
- **Color range** — every element draws its hue, saturation and lightness from a bounded field, so the palette can swing from restrained to exuberant without ever leaving the brand.

The result is a system that is random on purpose and bounded by design. Regenerate, and you get a poster nobody has seen before that nobody could mistake for anyone else's.

The identity applied across formats — poster, letterhead, business card — all generated from the same source shapes:

![Poster layout mockup](/assets/img/mockup.png)

## The tool

A generative system is only useful if the people who run the events can drive it. So the system became a configurator: set the threshold, tune the color range, edit logo and text, swap the background — and download the finished piece as a PDF, print-ready.

No design software. No designer in the loop. Every event gets its own original.

## Under the hood

Vanilla JavaScript with [d3.js](https://d3js.org) driving the SVG generation, [chroma.js](https://gka.github.io/chroma.js/) for the color ranges, [interact.js](https://interactjs.io) for the controls, and PDF export client-side. The source shapes live as SVGs in [`/sources`](./sources) — poster, letterhead, business card.

---

**[▶ Try it live](https://oratioandco.github.io/dynamic_identity_configurator/)** — no install, nothing to sign up for.
