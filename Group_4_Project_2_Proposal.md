# Project Proposal: Analyzing Structural Characteristics of Science Articles on Wikipedia

## 1. High-Level Goal
Collect and analyze metadata from a sample of English Wikipedia articles within the 'Science' category and its immediate subcategories to characterize their structure, scope, and engagement metrics.

## 2. Goals, Motivation, and Research Question:

### Goals

This project aims to programmatically collect data on a diverse set of approximately 100 Wikipedia articles related to the broad "Science" category. Using a provided Python script (leveraging `requests` and `BeautifulSoup`), we will scrape key metadata points, including:

- **Article size**: Word Count, Section Count
- **Sourcing**: Number of References
- **Connectivity**: Internal Links, External Links
- **Visual elements**: Image Count
- **Timeliness**: Last Edited Date
- **Historical depth**: First Edit Year

Following data collection, we will conduct an exploratory data analysis (EDA) to identify structural characteristics and emerging patterns within this sample.

### Motivation and Interest

Wikipedia serves as a primary source of scientific information for a global audience. Understanding the structural properties of science-related articles—such as length, sourcing, interconnectedness, and maintenance activity—is crucial for assessing the quality and accessibility of public scientific knowledge.

This project is particularly interesting because it uses computational methods to quantify aspects of science communication on an influential platform. It may also highlight potential gaps, such as important topics lacking references, or reveal trends in article maintenance across scientific disciplines.

### Data Collection & Rationale

We will use a Python scraping script to:

- Start from the "Category:Science" on English Wikipedia
- Retrieve articles directly within it and one level deeper into subcategories (Depth = 1)
- Cap the total sample at **100 articles** (MAX_ROWS = 100)

The collected metadata fields are:

| Field | Description |
|:------|:------------|
| Title | Article title |
| Summary | Short description/summary |
| Categories | List of assigned Wikipedia categories |
| References | Count of references |
| Internal Links | Number of internal links |
| External Links | Number of external links |
| Word Count | Total number of words |
| Section Count | Number of sections in the article |
| Image Count | Number of images |
| Last Edited | Date of last edit |
| First Edit Year | Year of first edit |

These features offer quantitative insights into article size, sourcing, connectivity, visual richness, and editorial history.

### Research Question

> **How do quantitative characteristics (e.g., word count, reference count, link density, image count, and edit history) vary among Wikipedia science articles and their subcategories? Are there discernible patterns related to article scope or topic as reflected in their assigned categories?**

---

## 3. Weekly Plan

### Group Member Roles and Rotation

To ensure balanced learning, fair contribution, and comprehensive skill development, we propose rotating roles weekly as follows:

| Week | Member 1 | Member 2 |
|:----:|:--------:|:--------:|
| 1 | Data Collection and Script Maintenance | GitHub Setup and Initial Validation |
| 2 | Data Cleaning and Preprocessing | Exploratory Data Analysis (EDA) and Visualization |
| 3 | Statistical Analysis and Visualization | Advanced Categorization and Focused Analysis |
| 4 | Report Writing (Methodology, Results) | Report Writing (Introduction, Discussion, Conclusion) |

- **Member 1** and **Member 2** will both be responsible for regular peer review of each other's work during weekly check-ins.
- In Week 4, both members will collaborate fully to synthesize all results into the final report and presentation.

---

### Week 1: Setup, Code Refinement, and Data Collection

- Set up Python environment (install `requests`, `beautifulsoup4`, etc.)
- Review and refine scraping script (error handling, delays, selectors)
- Execute script to collect data (Depth = 1, Max = 100 articles)
- Validate collected dataset (`wikipedia_science_expanded.csv`)
- Create and initialize GitHub repository (push initial code and dataset)

### Week 2: Data Cleaning and Exploratory Data Analysis (EDA)

- Load dataset (Pandas in Jupyter Notebook)
- Clean data (handle missing values, convert data types)
- Calculate basic descriptive statistics (mean, median, min, max, std dev)
- Create initial visualizations:
  - Histograms (e.g., Word Count, References)
  - Bar charts (e.g., Top Categories)
- Explore basic correlations (e.g., Word Count vs. References)
- Push cleaned data and analysis notebook to GitHub

### Week 3: Focused Analysis and Visualization

- Group articles based on 'Categories' field (may require processing)
- Compare article characteristics across groups (e.g., Word Count, Reference Density)
- Use boxplots or similar visualizations
- Identify and explore outliers
- Develop main visualizations that summarize findings
- Refine analysis based on results and feedback

### Week 4: Interpretation, Reporting, and Finalization

- Interpret findings relative to research questions and project goals
- Discuss implications, limitations, and future directions
- Write a final report or prepare a final presentation
- Organize GitHub repository (code, cleaned dataset, notebooks, report)
- Add a clear and comprehensive README file
- Prepare for project submission or presentation

---
