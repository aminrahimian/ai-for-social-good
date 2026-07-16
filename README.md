# IE 1171: AI for Social Good — Claude Tutorial Series

## Human–AI collaboration, statistical learning, and responsible analysis

> **Repository status:** This tutorial series is still in development. Tutorials 0–9 are currently included. Additional tutorials, data files, and final course guidance will be added as the series is completed.

Claude can help clarify a problem, navigate documentation, draft code, explain results, and challenge assumptions. It cannot decide what matters, guarantee correctness, or take responsibility for the consequences of an analysis.

> **Central idea:** The strongest workflow combines human purpose and judgment with AI speed and breadth.

## Repository Overview

This repository contains guided Jupyter notebook tutorials for IE 1171. The tutorials introduce human–AI problem solving, data understanding, statistical learning, machine learning, and responsible model evaluation.

Each tutorial contains:

- three main learning objectives;
- assigned reading and theory connections;
- a required Level 1 foundation;
- an optional Level 2 challenge;
- manual pauses before Claude is used;
- focused Claude collaboration or coding tasks;
- workspace cells for generated code;
- reference solutions for comparison;
- human checks, interpretation, and reflection;
- AI for social good connections.

The notebooks are not designed to make Claude complete an analysis automatically. They are designed to show how Claude can support a careful analytical process while the human remains responsible for the problem, data, verification, interpretation, and consequences.

## Tutorial Sequence

Complete the tutorials in numerical order when possible. Tutorials 2 and 3 directly use the output created in Tutorial 1.

| Tutorial | Main focus | Required file or files |
|---|---|---|
| **Tutorial 0: Human–AI Problem Solving with Claude** | Use Pólya’s problem-solving cycle to make Claude a collaborator rather than an answer machine. | No data required |
| **Tutorial 1: Data Understanding and Exploration** | Begin with the research problem, codebook, feature engineering, and exploratory data analysis. | `PublicData.csv` and `codebook.xlsx` |
| **Tutorial 2: Linear Regression Concepts and Modeling** | Use Claude to draft the programming while examining simple and multiple linear regression. | `tutorial_1_output.csv` created by Tutorial 1 |
| **Tutorial 3: Forward and Backward Model Selection** | Compare predictor sets without allowing the test set to choose the model. | `tutorial_1_output.csv` created by Tutorial 1 |
| **Tutorial 4: Logistic Regression** | Move from continuous predictions to probabilities and outcome groups. | `SocialNetworkAdClicks.csv` and `iris.csv` |
| **Tutorial 5: Naive Bayes** | Combine prior probabilities and feature evidence while questioning the naive assumptions. | `processed.cleveland.csv` |
| **Tutorial 6: K-Nearest Neighbors and Movie Recommendation** | Find similar movies while examining distance, sparsity, popularity, and privacy. | `data/movies.csv` and `data/ratings.csv` |
| **Tutorial 7: Decision Trees and Boosting** | Build an interpretable tree, control its complexity, and compare it with boosting. | `mushrooms.csv` |
| **Tutorial 8: Support Vector Machines** | Connect representation, margins, support vectors, and kernels to classification. | `Ad_click_prediction_train.csv` and `Ad_Click_prediciton_test.csv` |
| **Tutorial 9: Deep Learning** | Build a multilayer neural network while examining optimization, learned representations, and unequal error. | `smoking.csv` |

## Recommended Folder Structure

Keep each notebook and its required data together. File names and capitalization must remain exactly as shown because the notebooks check these paths before loading the data.

```text
data-for-good/
├── README.md
├── LICENSE
├── Tutorials/
│   ├── Tutorial 0 - Human-AI Problem Solving with Claude/
│   │   └── Tutorial 0 - Human-AI Problem Solving with Claude.ipynb
│   ├── Tutorial 1 - Claude Data Understanding and Exploration/
│   │   ├── Tutorial 1 - Claude Data Understanding and Exploration.ipynb
│   │   ├── PublicData.csv
│   │   └── codebook.xlsx
│   ├── Tutorial 2 - Claude Linear Regression Concepts and Modeling/
│   │   ├── Tutorial 2 - Claude Linear Regression Concepts and Modeling.ipynb
│   │   └── tutorial_1_output.csv
│   ├── Tutorial 3 - Claude Forward and Backward Model Selection/
│   │   ├── Tutorial 3 - Claude Forward and Backward Model Selection.ipynb
│   │   └── tutorial_1_output.csv
│   ├── Tutorial 4 - Claude Logistic Regression/
│   │   ├── Tutorial 4 - Claude Logistic Regression.ipynb
│   │   ├── SocialNetworkAdClicks.csv
│   │   └── iris.csv
│   ├── Tutorial 5 - Claude Naive Bayes/
│   │   ├── Tutorial 5 - Claude Naive Bayes.ipynb
│   │   └── processed.cleveland.csv
│   ├── Tutorial 6 - Claude K-Nearest Neighbors Movie Recommender/
│   │   ├── Tutorial 6 - Claude K-Nearest Neighbors Movie Recommender.ipynb
│   │   └── data/
│   │       ├── movies.csv
│   │       └── ratings.csv
│   ├── Tutorial 7 - Claude Decision Trees and Boosting/
│   │   ├── Tutorial 7 - Claude Decision Trees and Boosting.ipynb
│   │   └── mushrooms.csv
│   ├── Tutorial 8 - Claude Support Vector Machines/
│   │   ├── Tutorial 8 - Claude Support Vector Machines.ipynb
│   │   ├── Ad_click_prediction_train.csv
│   │   └── Ad_Click_prediciton_test.csv
│   └── Tutorial 9 - Claude Deep Learning/
│       ├── Tutorial 9 - Claude Deep Learning.ipynb
│       └── smoking.csv
└── extras/
    └── Previous repository files and course materials
```

## Before Beginning a Tutorial

1. Read the tutorial overview and learning objectives.
2. Complete the assigned reading before or alongside the notebook.
3. Download the complete tutorial folder, including its data files.
4. Keep the file names and folder locations unchanged.
5. Open the notebook in Google Colab or Jupyter Notebook.
6. Run the notebook from the first cell downward rather than skipping directly to the model.
7. Keep Claude open in a separate browser tab for the collaboration tasks.

GitHub can display a notebook, but the GitHub preview cannot run its code. Use Google Colab or Jupyter Notebook when completing the tutorial.

## Option 1: Use Google Colab

Google Colab is the easiest option if Python and Jupyter are not installed on your computer.

1. Download the tutorial notebook and its required data files from this repository.
2. Go to [Google Colab](https://colab.research.google.com/).
3. Select **File → Upload notebook**.
4. Choose the `.ipynb` file from the tutorial folder.
5. Select the folder icon on the left side of Colab.
6. Use **Upload to session storage** to upload the required data files.
7. For Tutorial 6, create a folder named `data` in the Colab file area and place `movies.csv` and `ratings.csv` inside it.
8. Run one cell at a time with the play button or `Shift + Enter`.

Colab session files are temporary. Download any output that must be used later before closing the session.

## Option 2: Use Jupyter Notebook Locally

Download the complete tutorial folder and open the notebook from that folder. A common local installation uses the following packages:

```bash
pip install jupyter pandas numpy matplotlib scipy scikit-learn openpyxl xgboost
```

After installation:

1. Open a terminal or Anaconda Prompt in the tutorial folder.
2. Run `jupyter notebook`.
3. Select the tutorial’s `.ipynb` file in the browser window.
4. Run the cells from top to bottom.

## How to Work With Claude

The Claude tasks are intentionally divided into focused steps. Use the following process:

1. Complete the **Manual Pause** before asking Claude.
2. Copy only the current Claude prompt from the notebook.
3. Provide the named data file or context when the task requests it.
4. Read Claude’s explanation and generated code before running anything.
5. Paste the code into the matching **Your Workspace** cell.
6. Run the cell and inspect every warning, table, measure, and plot.
7. Compare your result with the **Reference Solution** only after making your own attempt.
8. Complete the **Human Check** and **Look Back** sections yourself.

Do not judge a response only by whether it sounds confident or whether the code runs. Check whether:

- the problem was represented correctly;
- the correct file and variables were used;
- the assumptions are visible;
- the data were split and prepared appropriately;
- the output supports the interpretation;
- the consequences of incorrect predictions were considered.

## Level 1 and Level 2

**Level 1** is the required foundation. Complete it first and follow the parts in order.

**Level 2** is an optional challenge using the same reading and data foundation. It adds a harder application, audit, comparison, or extension without replacing the Level 1 work.

## Responsible Use

These tutorials are instructional. A model that performs well in a notebook is not automatically appropriate for medical, educational, financial, employment, safety, or other high-consequence decisions.

Model performance must be interpreted through the consequence of the error, not separated from it. Human judgment, domain knowledge, documentation, independent verification, and careful attention to affected groups remain necessary throughout the tutorial series.

## Development Notes

- Tutorials 0–9 are currently available.
- Additional tutorials are planned.
- Existing notebooks and data placement may receive small revisions.
- Final course-wide setup, instructor guidance, and supporting material will be added after the tutorial sequence is complete.

