# Reef Analytics

**Reef Analytics** is an interactive research prototype for exploring coral colony architecture, structural complexity, and synthetic 3D morphometrics.

Current release: **v0.7.0-alpha**

## Features

- Synthetic 3D coral colony generator
- Interactive 3D rotation
- Species presets for *Acropora palmata* and *Pocillopora damicornis*
- Adjustable branching, compactness, elongation, stress, and scale parameters
- Df3D approximation by 3D box-counting
- Surface area
- Colony volume
- Projected area
- Colony height
- Shelter volume
- T0 vs T1 comparison
- CSV, PNG, and PLY export
- Responsive PWA interface

## Scientific scope

Reef Analytics is currently a **synthetic geometric model**. It does not replace photogrammetry, structured-light scanning, or empirical measurements of coral colonies.

The current Df3D is estimated from sampled points on the synthetic branch surface. Surface area and volume are analytical approximations derived from tapered branch segments.

Shelter volume is currently calculated as:

```text
shelter volume = projected area × colony height − colony volume
```

The structural-stress control is conceptual and is not yet calibrated against DHW, temperature, bleaching severity, mortality, or hydrodynamic forcing.

## Run locally

No build system is required.

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Deploy

This repository can be deployed directly to Netlify, GitHub Pages, Vercel, or another static host.

## Current limitations

- Branch intersections are not yet boolean-unioned.
- Geometry is not yet a watertight triangular mesh.
- Surface area and volume may be biased upward where branches overlap.
- Df3D is based on sampled synthetic surface points.
- No real mesh import yet.
- No OBJ/STL export yet.
- Packing, sphericity, convexity, and rugosity are not yet implemented.
- Environmental stress is not empirically calibrated.

## Development

See [ROADMAP.md](ROADMAP.md).

## Authors and contributions

Reef Analytics is jointly developed by Eduardo Juventino Ramírez Chávez, Sergio David Guendulain García, and Andrés Ramón López Pérez.

See [AUTHORS.md](AUTHORS.md) for detailed scientific and technical contributions.

## Citation

See [CITATION.cff](CITATION.cff).

## License

MIT License by default. Change this before publication if you prefer another licensing model.

## Disclaimer

This is an alpha research prototype. Outputs should not be interpreted as validated ecological predictions unless independently calibrated and validated.
