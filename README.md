# HMDA-Analysis: Adventures in Modeling and Audit of Oregon HDMA Data

## Background:
The Home Mortgage Disclosure Act (HMDA) requires financial institutions to report and publicly disclose mortgage data. This project explores fairness and bias in machine learning models using the Oregon HMDA data from 2018 to 2021. The data helps identify potential discriminatory lending practices and allows public officials to make informed policy decisions.

HMDA was originally enacted by Congress in 1975 and is implemented by Regulation C. [Source](https://www.consumerfinance.gov/data-research/hmda/).

## Resources:
- [2021 HMDA Dataset](https://ffiec.cfpb.gov/data-browser/data/2021?category=states&items=OR)
- [2021 HMDA Guide](https://www.ffiec.gov/hmda/pdf/2021Guide.pdf)

## Project Overview:
This project analyzed the fairness of loan approval models by utilizing the Oregon HMDA dataset and applying bias mitigation techniques. The focus was on protected attributes such as sex, race, and ethnicity, ensuring equitable decision-making processes.

- **Dataset**: Oregon HMDA data from 2018–2021
- **Models**: Shallow two-layer neural network trained with TensorFlow/Keras
- **Bias Metrics**: Equal Parity, Proportional Parity, False Positive Rate Parity, and others
- **Bias Mitigation**: Class weighting was applied to mitigate bias.

## Key Findings:
- The machine learning model exhibited bias across multiple protected attributes, including sex, race, and ethnicity, despite efforts to mitigate bias.
- **Proportional Parity** was the only metric that passed the fairness checks, while others such as False Positive Rate and False Discovery Rate Parity failed, indicating the model’s difficulty in treating all demographic groups fairly.
- Bias mitigation efforts reduced some disparity, but five out of six fairness metrics still showed significant bias.
- Notably, the **derived sex** attribute passed four out of six bias metrics, making it fairer than race and ethnicity metrics.

## Conclusion:
Despite attempts at bias mitigation, the machine learning model revealed significant biases based on gender, race, and ethnicity, raising concerns about the model's suitability for fair decision-making. Bias was found to persist, even after efforts to adjust for class imbalances in the data, highlighting the need for more effective bias mitigation techniques. Future work should aim to refine these techniques and re-examine fairness metrics to ensure equitable outcomes in loan approval models.

