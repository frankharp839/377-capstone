# Capstone Template UPDATE

This is a template repository for setting up your capstone project: it includes a simple folder structure and placeholder files for the most important assets you will be creating.

## Usage

1. Start a new GitHub repo using this template.
2. Update your `LICENSE` file with date and owner.
3. Update your `README.md` file to reflect the project - see a sample structure below and please refer to Synapse on what needs to be included here. 
4. Set up and activate your conda environment:
    - Create a new `conda` environment for your capstone project.
    - Activate the environment and export:
        ```bash
        conda env export > conda.yml
        ```
    - Make sure re-export every time after you update the environment.
    - You can reset your conda environment by running:
        ```bash
        conda env create -f conda.yml
        conda activate <your-env-name>
        ```
5. Add your own notebooks in `./notebooks/` and remove placeholders.
6. Add your own data in `./data/` and remove placeholder. Note: `.gitignore` will ignore the data folder when you push to github, save a copy of your raw and processed data, pickled models in a Google Drive folder and add the link in the `data_links.md` file.
7. Add your project documents, figures, reports, presentation pdf's in the `./docs` and remove placeholders.
8. Add your references (tutorials, papers, books etc.) in `./references`. 
9. Add your own scripts in `./src/` and remove unnecessary folders.

Feel free to rename the folder and customize the project structure to best fit your work - this template is just the starting point.

------------------------------------------------------------------------------

## Diabetes Risk Prediction using Machine Learning
=========================

### Problem Area

The goal of the project is reducing the risk of diabetes by identifying factors that lead to the disease and use that information to formulate prevention methods. The project seeks to address the relationship between a patient’s biomarkers (e.g. blood pressure and glucose levels) and lifestyle habits that are considered unhealthy.

### Impact

The potential impact of this project includes:

1. Supporting and growing a heathier community.
2. Better health education to any affected communities.

### Dataset Description

Our analysis utilizes a dataset of females from the Gila River Indian community in Arizona. The dataset includes:

1.	Age, Pregnancies, and Outcomes of getting diabetes or not.
2.	Biomarkers (blood pressure, glucose, insulin, body mass index)

### Data Dictionary 

1. Pregnancies (int64): number of pregnancies a female has
2. Glucose (float64): sugar levels in blood in milligrams per deciliter (mg/dl)
3. Blood pressure (float64): blood circulation throughout the body in millimeters of mercury (mmHg)
4. Skin thickness (float64): hard and swollen looking skin in millimeters (mm)
5. Insulin (float64): transfers glucose from bloodstream into cells measured in units.
6. Body Mass Index (float64): body fat in weight per height (kg/m^2).
7. Diabetes Pedigree Function (float64): likelihood on developing diabetes based on family history.
8. Outcome (int64): outcomes of getting diabetes or not, 0 for no diabetes and 1 for diabetes.
9. Age (int64)

### Demo

... Show your work:
...     Data visualizations
...     Interactive demo (e.g., `streamlit` app)
...     Short video of users trying out the solution


### Methodology

... High-level diagrams of entire process:
...     various data processing steps
...     various modelling directions
...     various prototyping directions


### Organization

#### Repository 

* `data` 
    - contains link to copy of the dataset (stored in a publicly accessible cloud storage)
    - saved copy of aggregated / processed data as long as those are not too large (> 10 MB)

* `model`
    - `joblib` dump of final model(s)

* `notebooks`
    - contains all final notebooks involved in the project

* `docs`
    - contains final report, presentations which summarize the project

* `references`
    - contains papers / tutorials used in the project

* `src`
    - Contains the project source code (refactored from the notebooks)

* `.gitignore`
    - Part of Git, includes files and folders to be ignored by Git version control

* `conda.yml`
    - Conda environment specification

* `README.md`
    - Project landing page (this page)

* `LICENSE`
    - Project license

#### Dataset

... Google Drive links to datasets and pickled models

### Credits & References

... Include any personal learning
