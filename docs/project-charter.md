## Background
As organisations grow, customer information is often created and maintained across multiple operational systems, including CRM, ERP, service-management and master-data platforms. Over time, the same customer may be represented by several records containing differences in name format(legal name, business or 'doing-business-as' (DBA)), address lines and abbreviations, spelling, field completeness or data-entry conventions.

These inconsistencies make it difficult to determine whether two records refer to the same customer, business, individual/person or to different individuals. Traditional rule-based matching can address some of these problems, but fixed rules may become difficult to maintain as data volumes, source systems and variation patterns increase.

This project uses the synthetic FEBRL record-linkage dataset to examine how rule-based and machine-learning approaches can support duplicate customer record detection. FEBRL contains fictitious person records with controlled spelling variations, abbreviations, missing values, transpositions and other inconsistencies commonly encountered in enterprise customer master data. Its synthetic nature allows the project to demonstrate record-linkage methods without using employer, customer or personally identifiable information. :contentReference[oaicite:0]{index=0} :contentReference[oaicite:1]{index=1}

## Business Problem
Duplicate customer records create fragmented and unreliable views of customers across enterprise systems. When duplicates remain unresolved, customer analytics may be distorted, communication, service delivery, and servicing costs may increase, operational teams and field service representatives may act on incomplete information, and downstream analytical models may produce unreliable results.

In a Master Data Management environment, duplicate detection is often performed through fixed matching rules or manual review. These approaches can be transparent and effective, but they may require extensive maintenance and may not adapt well to complex variations in names, addresses and other identifying fields.

The business challenge is therefore to determine whether supervised machine-learning models can identify duplicate customer records more effectively than a well-designed rule-based baseline, while remaining sufficiently explainable and practical for use within an enterprise MDM and Data Governance programme. The organisation must also decide whether any improvement in predictive performance justifies the additional complexity, monitoring and governance requirements associated with machine learning. :contentReference[oaicite:2]{index=2} :contentReference[oaicite:3]{index=3}

## Project Objective
The objective of this project is to design and evaluate a reproducible entity-resolution process for identifying probable duplicate customer records and supporting the creation of a trusted customer view.

The project will:
1. Profile the FEBRL customer data to identify missing values, field inconsistencies and common variation patterns.
2. Engineer field-level similarity features using techniques such as Jaro-Winkler similarity, Levenshtein distance, token-based cosine similarity and exact-match indicators.
3. Develop a transparent rule-based duplicate-detection baseline.
4. Train and compare supervised classification models, including Logistic Regression, Decision Tree, Random Forest and XGBoost.
5. Evaluate model performance using precision, recall, F1-score and ROC-AUC rather than relying on accuracy alone.
6. Examine which fields and similarity features contribute most strongly to duplicate identification.
7. Establish thresholds for confirmed matches, confirmed non-matches and records requiring manual steward review.
8. Design survivorship and golden-record rules for resolving conflicting customer attributes.
9. Document the governance controls, limitations and implementation considerations required for applying the approach in an enterprise MDM environment.

The wider objective is not merely to identify the model with the highest score. It is to determine whether machine learning provides sufficient operational and governance value to justify its additional complexity when compared with established rule-based matching methods. :contentReference[oaicite:4]{index=4} :contentReference[oaicite:5]{index=5}

## Success Criteria
The project will be considered successful when it produces a complete, reproducible and professionally documented entity-resolution solution that satisfies the following criteria:

1. **Data understanding:** The source dataset is profiled and documented, including field completeness, variation patterns and class imbalance.
2. **Transparent baseline:** A clearly defined rule-based matching approach is implemented so that machine-learning results can be compared against an understandable benchmark.
3. **Model comparison:** Logistic Regression, Decision Tree, Random Forest and XGBoost models are trained and evaluated using a consistent validation approach.
4. **Appropriate evaluation:** Performance is assessed using precision, recall, F1-score and ROC-AUC, with particular attention to the business consequences of false-positive and false-negative matches.
5. **Explainability:** The project identifies which similarity features and customer attributes contribute most strongly to matching decisions.
6. **Operational decision framework:** Matching thresholds are translated into practical categories for automatic match, automatic non-match and manual steward review.
7. **Golden-record design:** The project defines defensible survivorship rules for resolving conflicting attributes and creating a trusted customer record.
8. **Governance relevance:** The findings are translated into recommendations for data stewardship, manual review, model oversight, exception handling and ongoing data-quality monitoring.
9. **Reproducibility:** The code, methodology, data dictionary, assumptions and limitations are clearly documented so that another analyst can understand and reproduce the analysis.
10. **Responsible interpretation:** Any improvement from machine learning is assessed against the additional implementation and governance complexity it introduces. The project will not claim that a more complex model is preferable unless the evidence demonstrates a meaningful practical benefit.

Because FEBRL is synthetic, the project will also acknowledge that results may not transfer directly to production customer data with more complex, multilingual or organisation-specific naming conventions. :contentReference[oaicite:6]{index=6} :contentReference[oaicite:7]{index=7}
