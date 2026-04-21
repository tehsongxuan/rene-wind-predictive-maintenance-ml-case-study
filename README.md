TehSongXuan_INN_ReneWind_Project_FullCode.html
# ReneWind Predictive Maintenance ML Case Study

Failure prediction for wind turbine generators using sensor data, neural network modelling, and recall-focused optimisation.

## Project Overview
This project analyses a predictive maintenance use case for ReneWind, a wind energy company seeking to identify generator failures before breakdown. Using transformed sensor-based turbine data, I developed and evaluated multiple neural network models to support earlier failure detection and reduce maintenance-related costs.

This case study focuses not only on model performance, but also on how machine learning can be translated into operational decision-making through clear business framing, model comparison, and actionable recommendations.

## Business Problem
ReneWind aims to reduce generator downtime and maintenance costs by predicting failures in advance.

In this problem:
- True Positives (TP): failures correctly predicted, leading to repair costs
- False Negatives (FN): actual failures missed by the model, leading to replacement costs
- False Positives (FP): normal cases incorrectly flagged, leading to inspection costs

Because missed failures are more costly than false alarms, **Recall** is treated as the most important evaluation metric.

## Objective
Build and compare classification models that can identify likely turbine generator failures early enough to support preventive maintenance and reduce operational risk.

## Dataset
- 40 predictor variables
- 20,000 training observations
- 5,000 test observations
- Target variable:
  - `1` = failure
  - `0` = no failure

The dataset is a transformed / ciphered version of confidential sensor data.

## Approach
The project followed a structured machine learning workflow:
1. Business understanding and problem framing
2. Exploratory data analysis
3. Data preprocessing
4. Baseline neural network modelling
5. Model improvement through experimentation
6. Performance comparison using recall, precision, F1-score, and confusion matrices
7. Business recommendations

## Model Development
I developed and compared multiple neural network variants, including:
- Baseline model
- Dropout-based regularisation
- Class-weighted model for imbalanced data
- Adam vs SGD optimisation
- Deeper architectures with additional hidden layers
- Combined enhancements to improve recall and generalisation

## Key Results
The project showed that optimising only for overall accuracy can be misleading in an imbalanced predictive maintenance problem.

Among the models tested:
- Model 3 delivered the strongest recall generalisation performance and was selected as the final model in the project write-up.
- The analysis highlighted the trade-off between higher recall and lower precision, which is acceptable in predictive maintenance where missed failures are more costly than additional inspections.
- The project demonstrates how model selection should be driven by business risk, not just technical metrics in isolation.

## Business Insights
This project demonstrates how AI can support operational decision-making by:
- identifying likely failures earlier
- reducing costly unplanned downtime
- prioritising maintenance actions
- improving asset reliability
- supporting a more proactive maintenance strategy

It also shows the importance of aligning model evaluation with business cost logic, especially in high-stakes operational environments.

## Files in this Repository
- `README.md` — project overview and business summary
- `TehSongXuan_INN_ReneWind_Project_FullCode.html` — full notebook exported as HTML
- `images/` — selected charts, confusion matrices, model comparison visuals
- `docs/` — optional GitHub Pages version for browser viewing

## View the Full Project
- [Open the full HTML notebook](./TehSongXuan_INN_ReneWind_Project_FullCode.html)

## Tools Used
- Python
- Pandas
- NumPy
- Matplotlib / Seaborn
- Scikit-learn
- TensorFlow / Keras
- Jupyter Notebook

## Why This Project Matters
This case study reflects my interest in using AI and analytics to translate technical work into clear, decision-ready outcomes. Beyond model building, I focused on communicating trade-offs, explaining business impact, and structuring insights in a way that supports stakeholder understanding and operational adoption.

## Future Enhancements
- compare neural network results with tree-based ensemble models
- introduce cost-sensitive threshold tuning
- test deployment-ready alert prioritisation logic
- package outputs into stakeholder dashboards or executive briefings

## Author
Song Xuan
