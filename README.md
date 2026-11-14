# Used Car Price Prediction

A machine-learning regression project for estimating used-car selling prices using the Vehicle Dataset from CarDekho.

## Submission files

- `README.md` — project description and setup instructions.
- `LICENSE` — MIT license for this repository's original code and documentation only.
- `used_car_price_prediction.ipynb` — notebook entry point.
- `src/` — separate EDA, preprocessing and model-training Python files.
- `Used_Car_Price_Prediction_Project_Report.docx` — project report.
- `data/` — place the downloaded dataset here; the dataset itself is not bundled.
- `outputs/` — generated model metrics, plots and saved model after training.

## Dataset

Download the Vehicle Dataset from CarDekho:
https://www.kaggle.com/datasets/nehalbirla/vehicle-dataset-from-cardekho

Save the CSV as `data/car_data.csv`. The scripts adapt to available supported columns and require `selling_price` as the target. Dataset versions may differ in row and column counts.

The dataset is not included in this repository. Check its license and Kaggle terms before redistributing it or committing it to a public repository.

## Install and run

```bash
pip install -r requirements.txt
python src/eda.py
python src/train.py
```

Or open `used_car_price_prediction.ipynb` in Jupyter and run its cells in order.

The training script compares Linear Regression, Decision Tree, Random Forest, AdaBoost and Gradient Boosting. It reports MAE, MSE, RMSE and R², saves `outputs/model_comparison.csv`, charts and the best trained model.

**Evaluation note:** This is a regression task, so classification accuracy is not appropriate. Report R² together with MAE, MSE and RMSE. Do not invent scores; use the values produced by running the code.

## GitHub upload

Create a new empty GitHub repository, then from this folder run:

```bash
git init
git add .
git commit -m "Add used car price prediction project"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```

Replace the remote URL with your own repository URL.

## Create a DOI with Zenodo

1. Push the finished project to GitHub.
2. Sign in to Zenodo and connect/authorize your GitHub account.
3. In Zenodo's GitHub integration, enable the repository you want to archive.
4. Create a GitHub release in your repository (for example `v1.0.0`) and publish it.
5. In Zenodo, open the record created for that release, review its metadata and publish the record.
6. Copy the version-specific DOI shown by Zenodo and use that DOI link when sharing the archived project.

Zenodo's interface and integration steps may change. A DOI is created only after the release is archived and the Zenodo record is published. Do not claim a DOI before Zenodo provides one.

## Prediction CSV

`outputs/model_comparison.csv` is generated when training runs. A separate predictions CSV can only be created after the dataset and model have been run; no fabricated prediction values are included in this repository.
