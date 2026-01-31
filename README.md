# Group 6 Prediction Model

## Setup Virtual Environment
```
python -m venv venv
source venv/bin/activate        # Linux/Mac
venv\Scripts\activate           # Windows
```

## Install Requirements
```
pip install pm4py pandas numpy torch scikit-learn seaborn matplotlib tqdm
```

## Data

**Source:** `BPI_Challenge_2017.xes` from Canvas

**Included CSV files:**
- `train_data.csv` - Training set (cases ending before 2016-11-01)
- `test_data.csv` - Test set (cases starting after 2016-11-01)

**Temporal Split:**
- Cutoff date: **2016-11-01**
- Train: cases that ended before cutoff
- Test: cases that started after cutoff
- Excluded: cases spanning the cutoff (to prevent data leakage)

**Features in CSV:**
| Column | Description |
|--------|-------------|
| CaseID | Application ID |
| CreditScore | Last known credit score before decision point |
| OfferCount | Number of offers created |
| ProcessingTime | Days from start to A_Complete |
| Amount | Requested loan amount |
| Label | 0 = Accepted, 1 = Cancelled/Refused |
| + Activity columns | Bag-of-words count per activity |

## Run
Open `prediction_model.ipynb` and run all cells in order.
