# From Nothing to Mind

**→ [weopki1232.github.io/neuron-to-brain](https://weopki1232.github.io/neuron-to-brain/)**

A scroll-driven biology explainer. One point cloud morphs across 43 stations: scattered
dust becomes a neuron, the neuron becomes a network, the network becomes a brain — then the
skull closes over it, the spine descends, the arm is built, and a tendon tap travels back up
to fire the muscle. The last station hands you the model to drag and turn yourself.

Scroll is the only control until the end. No build step, no framework, no server needed.

## What's in here

| File | What it is |
|---|---|
| `index.html` | the whole thing — 7.1 MB, all geometry inlined as typed-array literals |
| `three.min.js` | three.js, the single dependency |
| `ATTRIBUTION.txt` | where the anatomy came from |

GitHub won't preview `index.html` in the file browser (it refuses HTML over ~5 MB) — use the
live link above. Over the wire it's about 3.5 MB gzipped.

## Running it locally

Clone and open `index.html` in a browser. It's a `file://`-safe page: the only relative
reference is `./three.min.js`. The three webfonts come from Google Fonts, so offline the type
falls back to the system sans/mono — everything still works, it just looks plainer.

Needs WebGL and a discrete-ish GPU to stay smooth — the scene is a single
`THREE.Points` cloud in the hundreds of thousands of points, and the floor it was tuned
against is **30 fps at ordinary scroll speed** on the development laptop.

## Where the anatomy is real

The brain, brainstem, cerebellum, vertebrae and spinal canal are **not modelled by hand** —
they are real mesh data resampled into the point cloud. See `ATTRIBUTION.txt`:

- **BodyParts3D** © The Database Center for Life Science (DBCLS), CC BY-SA 2.1 Japan
- **Neuron morphology** (`cnic_001`) from NeuroMorpho.org, Wearne_Hof archive — a real
  light-microscopy reconstruction, not a drawn approximation
- **Myelinated axon** built to a labelled textbook cross-section, not downloaded

The nerve paths, the brachial plexus braid, the neuromuscular junction and the reflex arc
were specified against anatomy references rather than eyeballed.

## Licence

- **Code** (the page, the shaders, the morph engine): MIT — see `LICENSE`.
- **three.js**: MIT, © three.js authors.
- **Anatomy point data derived from BodyParts3D**: CC BY-SA 2.1 Japan. That's a share-alike
  licence, so if you reuse the geometry, carry the attribution and the same terms with it.
