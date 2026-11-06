# Mini-Courier Planner Capstone

A complete, executable B.Tech capstone prototype for parcel prioritization, capacity constrained packing, shortest-path routing, and delivery-tour planning. The complete implementation is in `mini_courier_planner.ipynb`.

## What it does

- Loads fictional parcel and road data from `datasets/` with Pandas.
- Ranks parcels using an implemented merge sort (priority descending, deadline ascending).
- Selects the maximum declared-value parcel set that fits an 18.0 kg limit using 0/1 knapsack dynamic programming.
- Builds an undirected weighted graph and runs heap-based Dijkstra shortest paths.
- Plans a depot-to-depot visit order with nearest-neighbor TSP over shortest-path distances.
- Runs correctness assertions, timed benchmarks, and produces charts and PNG evidence.

All dataset names, addresses, and road distances are fictional. The TSP routine is an approximation and is not guaranteed to find the optimal tour.

## Open and run in VS Code

1. Extract the ZIP and open the `mini-courier-planner` folder in VS Code.
2. Install Python 3.10 or later and the VS Code **Python** and **Jupyter** extensions.
3. In the VS Code terminal, run `python -m pip install -r requirements.txt`.
4. Open `mini_courier_planner.ipynb`, select the installed Python kernel, and choose **Run All**. Run it with the project folder as the notebook working directory so `datasets/` and `images/` resolve correctly.
5. The notebook prints the current output and regenerates `images/runtime_measurements.csv`, `images/runtime_comparison.png`, and the evidence PNGs in `images/screenshots/`.

The saved notebook includes output from the execution completed for this submission. Benchmark times vary across computers and runs.

## Project structure

```text
mini-courier-planner/
├── README.md
├── PROJECT_REPORT.md
├── mini_courier_planner.ipynb
├── datasets/
│   ├── parcels.csv
│   └── routes.csv
├── images/
│   ├── runtime_comparison.png
│   ├── runtime_measurements.csv
│   └── screenshots/
├── requirements.txt
└── .gitignore
```

## Publish with GitHub Desktop

1. Extract the ZIP and open GitHub Desktop.
2. Choose **File > Add Local Repository**, select the extracted `mini-courier-planner` folder, and initialize it as a repository if prompted.
3. Review the changed files, enter a summary such as `Complete Mini-Courier Planner capstone`, and click **Commit to main**.
4. Choose **Publish repository**. Select private/public visibility as directed by your college and publish.
5. To create the required tag, open **Repository > Create Tag**, enter `v1.0-final-submission`, choose the final commit, and confirm. Push the tag using **Push origin** (or **Repository > Push** and ensure tags are included).
6. Submit the GitHub repository URL through your LMS/ZOSIMA portal. Account sign-in, repository visibility, publishing, and LMS submission require your own account access.

## Evidence

`images/screenshots/` contains program-generated parcel ranking, packing, graph, route, correctness-check, and performance images. These are generated from executed program results, not screenshots from a user's computer.
