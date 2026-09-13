# Werkstatt Gottesdienst — a generative church identity

**One building, endless posters.** A dynamic identity generator pitched for a church startup in Berlin — every regeneration produces a poster that has never existed before, yet is unmistakably the same brand.

**[▶ Try it live](https://oratioandco.github.io/dynamic_identity_configurator/)**

![The configurator in action — regenerating the design, retuning the colors, downloading the result](/assets/img/configurator-demo.gif)

---

## The brief

The venue is St. Johannes Evangelist on Auguststraße in Berlin-Mitte — gallery row. A beautiful old building with a signature look and a lot of architectural detail.

But the congregation was not the church that owns the building. The client was a church startup — a young congregation renting the space for its services, gathered under the Evangelische Kulturwerkstatt, the Protestant church's culture program. The building itself had passed into art use: the Kulturwerkstatt showed contemporary art there, which is what put it on gallery row in the first place. A congregation meeting inside an artwork, in effect.

That layered setting shaped the brief. The startup's services would vary — teaching, worship, cultural evenings — and each needed a poster, an invitation, a flyer. A fixed logo could never carry that variety. The identity needed to be as plural as the room it was meeting in.

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

No design software. No designer in the loop. Every service gets its own original.

## Epilogue

The building was later sold and is today a full church again — home to an Assyrian congregation. The identity was made for a specific moment in the building's life: a young church renting an art space, on a street full of galleries. The posters are how that moment looked.

## Under the hood

Vanilla JavaScript with [d3.js](https://d3js.org) driving the SVG generation, [chroma.js](https://gka.github.io/chroma.js/) for the color ranges, [interact.js](https://interactjs.io) for the controls, and PDF export client-side. The source shapes live as SVGs in [`/sources`](./sources) — poster, letterhead, business card.

---

**[▶ Try it live](https://oratioandco.github.io/dynamic_identity_configurator/)** — no install, nothing to sign up for.
