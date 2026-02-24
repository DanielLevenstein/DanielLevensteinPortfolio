# SuperCart Store Revenue Prediction

## Project Summary

- Ingests categorical and numerical data from a csv file.
- Cleans up categorical columns and converts them to enumerations.
- Trains product sales prediction model using gradiant boost.
- Serializes model using pickle and deploys it to Huggingface using Flask for the backend and streamlit for the frontend.

**Frontend URL:** https://huggingface.co/spaces/DanielLevenstein/SuperCartFrontend

## Data Cleaning

- Categorical columns like ["Product_Sugar_Content", "Product_Type", "Store_Size", and "Store_Location_City_Type"] were converted to enumerations before training the model.
- Some columns like [Product_Sugar_Content] had multiple values which mapped to the same enumerations. For these columns one single value was listed in dropdown for the UI.
- A helper function was used in the Streamlit API to convert the selected categorical values to integer values prior to sending them to the backend.

## Features Used


| Field                        | Input Type | Options                                   |
| ---------------------------- | ---------: | ----------------------------------------- |
| Product\_Weight              |      Float | weight in units (e.g., grams or kg)       |
| Product\_Allocated\_Area     |      Float | percentage of total display area (0–100) |
| Product\_MRP                 |      Float | price (currency)                          |
| Product\_Store\_Sales\_Total |      Float | total sales amount (currency)             |

![Numerical Columns](../charts/numerical_columns_used.png)



| Field                       | Input Type | Options                                                                                                                                                                                                     |
| --------------------------- | ---------: | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Product\_Sugar\_Content     |   Dropdown | No Sugar, Low Sugar, Regular                                                                                                                                                                                |
| Product\_Type               |   Dropdown | Frozen Foods, Dairy, Canned, Baking Goods, Health and Hygiene, Snack Foods, <br />Meat, Household, Hard Drinks, Fruits and Vegetables, Breads, Soft Drinks, <br />Breakfast, Others, Starchy Foods, Seafood |
| Store\_Size                 |   Dropdown | Small, Medium, High                                                                                                                                                                                         |
| Store\_Location\_City\_Type |   Dropdown | Tier 1, Tier 2, Tier 3                                                                                                                                                                                      |

![Categorical Columns](../charts/categorical_columns_used.png)

## Conclusion

This project shows how to deploy a model on HuggingFace in a form that allows other developers to test your model using their own input data.

### Project

- Class: AI Model Deployment
- Name: Daniel Levenstein
- Submission Date: 2/15/2026
