# NEXUS — Autonomous ML Experiment Planner
React + TypeScript + Tailwind CSS v4 dashboard for static GitHub Pages hosting.

## Local setup
1. Copy your three actual CSV result files into `public/data/`:
   - `experiment_leaderboard.csv`
   - `feature_importance.csv`
   - `final_evaluation_summary.csv`
2. Run `npm install`, then `npm run dev`.
3. Open the local Vite URL shown in the terminal.

## GitHub Pages
1. Create a GitHub repository, e.g. `autonomous-ml-experiment-planner`.
2. In `vite.config.ts`, replace `YOUR_REPOSITORY` with that exact repository name.
3. In GitHub, open **Settings → Pages** and choose **GitHub Actions** as the source.
4. Commit and push the project to the `main` branch. The included workflow builds and deploys it.
5. Your URL will be `https://YOUR_GITHUB_USERNAME.github.io/YOUR_REPOSITORY/`.

If the repository is named `YOUR_GITHUB_USERNAME.github.io`, change `base` in `vite.config.ts` to `/`.

## Important
GitHub Pages hosts static files only. This UI reads saved CSV results in the browser; it does not run Python agents, train models, or start new experiments. Agent descriptions in `src/data/agents.ts` are based on the six-agent project outline currently available in the conversation. Compare them against `RaviTeja_MLPlannerV2.ipynb` before presenting; the notebook itself was not included with this generated source package. The CSV loader tries common header names, so if your files use different headers, adjust `src/lib/data.ts`.
