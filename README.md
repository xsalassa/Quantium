# Quantium retail analytics

Two Python notebook exercises covering retail customer behavior and store-trial evaluation. The first prepares transaction/customer data and compares customer segments; the second selects control stores and examines changes during a trial period. This is educational analysis, not a production experiment or a claim of commercial impact.

## Start with the notebooks

| Notebook | Questions and methods |
| --- | --- |
| [Data preparation and customer analytics](Data_preparation_and_customer_analytics%20%281%29.ipynb) | Clean and join transaction/customer records; inspect missing dates, outliers, product brands and pack sizes; compare sales, customer counts and purchasing patterns across segments; examine group differences with a t-test. |
| [Experimentation and uplift testing](Experimentation_and_uplift_testing%20%281%29.ipynb) | Aggregate store/month metrics, compare candidate controls, scale control performance against trial stores, and inspect sales/customer changes with plots and statistical comparisons. |

The notebooks contain code, explanatory notes and stored outputs. Stored output is a historical artifact and was not regenerated for this README.

## Data and supporting files

- [QVI_transaction_data.xlsx](QVI_transaction_data.xlsx): transaction workbook included in the repository.
- `QVI_purchase_behaviour.csv`: referenced by the customer-analysis notebook but absent from this checkout.
- `QVI_data.csv`: referenced by the trial-analysis notebook but absent from this checkout.
- [Presentation PDF](Task%203%20-%20presentation%20guide_BRAND.pdf) and [editable slides](Task%203%20-%20presentation%20guide_BRAND.pptx): supporting presentation artifacts.

The notebooks currently read from hardcoded Google Colab Drive paths. The included workbook alone is insufficient to reproduce both analyses. Obtain the missing inputs through the original exercise materials and review their permitted use; do not substitute or publish private customer records.

## Reproduction steps

1. Open the notebooks in Jupyter or Google Colab and inspect their data-loading cells.
2. Provide the expected transaction/customer inputs and replace the Colab-specific file paths with your local paths. In local Jupyter, also replace or skip the Colab-only Drive import/mount cells.
3. Install the packages imported by the notebooks, including pandas, NumPy, Matplotlib, SciPy, Seaborn and missingno. No dependency lock or tested environment is provided here.
4. Run cells from the beginning in a clean kernel. Check joins, date coverage, missing values and outlier decisions before interpreting charts or test results.
5. Recheck control-store selection, scaling, time periods and statistical assumptions before drawing conclusions about the trial.

## Interpretation limits

The customer notebook uses segment comparisons; the trial notebook uses selected control stores and pre-trial scaling. A nonsignificant test result does not prove groups are equivalent, and observed differences do not by themselves establish a causal effect. Control selection and repeated comparisons also affect interpretation.

No notebook execution, data refresh, numerical result verification or independent evaluation was performed for this documentation update. The README summarizes the implemented workflow without promoting stored accuracy, significance or uplift statements into newly verified findings.
