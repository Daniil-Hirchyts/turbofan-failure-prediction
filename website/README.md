# FD001 website

A one-page visual summary of [the merged notebook](../nasa_fd001_predictive_maintenance.ipynb): the engine, the data, the models and the results.

```bash
npm install
npm run dev
```

Then open http://localhost:5173. `npm run build` writes a static site to `dist/`.

The charts read `src/data/fd001.json`. To rebuild it from the raw C-MAPSS files (about 4 minutes, needs pandas and scikit-learn):

```bash
npm run data
```

The script repeats the notebook's reference pipeline and stops if a checked number differs from the reference results.

Built with React, Tailwind, [EvilCharts](https://evilcharts.com) (Recharts) and the Turbofan figure from [Anatomy](https://github.com/wheresryan22/anatomy) (MIT).

Published at https://website-snowy-eight.vercel.app. Vercel deploys pushes to `main`
from the connected GitHub repository, using `website/` as the root directory,
`npm run build` as the build command, and `dist/` as the output directory.
