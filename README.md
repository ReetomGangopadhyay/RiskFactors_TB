# infectious_disease_SIBS

## Data Cleaning Key

# Key for Data

**person**  
**case_id**  
**eTB.Manager.ID**  
**Outcome**  
**Sex**  
**Age**  
- Fixed two entries showing ">100" by taking modulo 100, i.e., 134 → 34.

**Region**  
**Urban.Rural**  
**Treatment.start.date**  
- Renamed to **start_date** and converted to date/time format.

**Treatment.end.date**  
- Renamed to **end_date** and converted to date/time format.

**Localization**  
- Changed to 1 for Pulmonary, 2 for Extra-pulmonary, and 0 for Both. No missing values.

**Cavitation**  
- Changed to 1 for Yes, 0 for No.

**hiv_def**  
- 0 for negative, 1 for positive.

**HIV.testing**  
- Renamed to **hiv_testing** and changed to date/time format.

**Has.started.to.take.ART.**  
- Renamed to **takes_art**. Set start date for ART to m/d/y format. Consider adding missing values as the epoch (commented out for now).

**Cotrimoxazole.treatment**  
- Changed to m/d/y format and consider adding epoch.

**Alcohol.abuse**  
- Set to 0 if ‘-’ or NA, otherwise set to 1 for yes.

**Injecting.drug.user**  
- Set to 0 if ‘-’ or NA, otherwise set to 1 for yes.

**Homeless**  
- Set to 0 for No and 1 for Yes. Consider ‘-’ to be No.

**Unemployed**  
- Set to 0 for No and 1 for Yes. Consider ‘-’ to be No.

**Healthcare.worker**  
- Renamed to **healthcare_worker** and set to 0 for No and 1 for Yes. Consider ‘-’ to be No.

**Prisoner**  
- Set to 0 for No and 1 for Yes. Consider ‘-’ to be No.

**Sample.collection.date**  
- Renamed to **sample_date** and changed to date/time format.

**Weight**  
- **NEW VARIABLE:** **imputed_weights**

#### Method:

1. Convert weights from pounds to kilograms if they are between 140 and 240.
2. Add a decimal point for weights between 240 and 1000.
3. Set values > 1000 to NA and impute.

Multiple imputation based on Age, Sex, Weight using the MICE package in R. The distribution looks correct.

**Smear.result**  
**Culture.result.Bactec**  
- Renamed to **Bactec** and changed NA values to negative.

**Culture.result.LowensteinJensen**  
- Renamed to **LJ** and changed NA values to negative.

**GeneXpert**  
- Set to 0 for Negative and 1 for Positive. Consider NA as Negative.

### DST Vars
**DST.result.E**  
**DST.result.Z**  
**DST.result.R**  
**DST.result.S**  
**DST.result.H**  
**DST.result.Am**  
**DST.result.Cm**  
**DST.result.Lfx**  
**DST.result.Mfx**  
**DST.result.PAS**  
**DST.result.Km**  
**DST.result.Ofx**  
**DST.result.Et**  
**DST.result.Gfx**  
**DST.result.Lzd**  
**DST.result.Cs**  
**DST.result.Cfx**  
**DST.result.Sfx**  
**DST.result.Pa**

- For all DST results: 
  - Make missing values 0, "Resistant" 1, "Sensitive" 2, and "Contaminated" 3.
  - Apply naming convention **DST_XYZ**, e.g., **DST.results.R** → **DST_R**. Adjust names for multiple letters as needed.

**migrant_refugee**  
- Set to 0 for No and 1 for Positive.

**new_prev**  
**case.start**  
- Changed to date/time format.

**case.end**  
- Changed to date/time format.

**fake.failure**  
**final_outcome**  
**final_outcome_group**

---

There are three new variables; note this before analysis. Some variables are not clean on purpose.
