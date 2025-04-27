**Project Proposal: Analyzing Structural Characteristics of Science Articles on Wikipedia**

**1. High-Level Goal:**
To collect and analyze metadata from a sample of English Wikipedia articles within the 'Science' category and its immediate subcategories to characterize their structure, scope, and engagement metrics.

**2. Goals, Motivation, and Research Question:**

*   **Goals:** This project aims to programmatically collect data on a diverse set of ~100 Wikipedia articles related to the broad category of "Science". Using the provided Python script leveraging `requests` and `BeautifulSoup`, we will scrape key metadata points including article size (Word Count, Section Count), sourcing (References), interconnectedness (Internal Links, External Links), visual elements (Image Count), timeliness (Last Edited Date), and historical depth (First Edit Year). The primary goal following data collection is to perform an exploratory data analysis (EDA) to identify typical characteristics and potential patterns within this sample of science-related articles.
*   **Motivation & Interest:** Wikipedia serves as a primary source of scientific information for a vast global audience. Understanding the structural properties of these articles—how long they are, how well-sourced they appear, how they connect to other information, and how actively they are maintained—is crucial for gauging the nature of publicly accessible scientific knowledge. This project is interesting because it applies computational methods to quantify aspects of science communication and knowledge curation on this influential platform. It can potentially highlight differences in how various scientific topics are presented or identify articles that might warrant further qualitative review based on their metadata (e.g., high importance topic with few references).
*   **Data Collection & Rationale:** The data will be collected using the provided Python script. It starts from the English Wikipedia "Category:Science", retrieves articles directly within it, and explores one level deeper into its subcategories (`DEPTH=1`), capping the total number of articles at `MAX_ROWS=100`. This approach provides a manageable yet diverse sample across different facets of science. The specific metadata fields (Title, Summary, Categories, References, Links, Last_Edited, Word_Count, Image_Count, Section_Count, External_Links, First_Edit_Year) are chosen because they offer quantitative insights into article size, depth, connectivity, visual richness, and editorial history.
*   **Research Question:** How do quantitative characteristics (such as word count, reference count, link density, image count, and edit history indicators) vary among articles within the 'Science' category and its immediate subcategories on English Wikipedia, and are there discernible patterns related to article scope or topic revealed through their assigned categories?

**3. Weekly Plan:**

*(Assuming a 4-week timeline and a single team member, adjust as necessary)*

*   **Week 1: Setup, Code Refinement & Data Collection**
    *   Set up the Python environment with necessary libraries (`requests`, `beautifulsoup4`).
    *   Review and potentially refine the scraping script (e.g., enhance error handling, adjust delays, confirm CSS selectors are current).
    *   Execute the script to collect data for the "Science" category (Depth 1, Max 100 rows).
    *   Perform initial validation of the output CSV file (`wikipedia_science_expanded.csv`) to ensure data integrity.
    *   Set up the GitHub repository. Push initial code and dataset.

*   **Week 2: Data Cleaning & Exploratory Data Analysis (EDA)**
    *   Load the dataset into a data analysis environment (e.g., Pandas in a Jupyter Notebook).
    *   Clean the data: Handle any missing values ('Unknown'), convert data types (e.g., counts to numeric, dates to datetime objects).
    *   Calculate basic descriptive statistics for all quantitative features (mean, median, min, max, standard deviation).
    *   Create initial visualizations: Histograms for distributions (Word Count, References, etc.), bar charts for categorical counts (if applicable from 'Categories' field after potential processing).
    *   Explore basic correlations between variables (e.g., Word Count vs. References, Links vs. Word Count).
    *   Commit analysis notebook and updated data (if cleaned) to GitHub.

*   **Week 3: Focused Analysis & Visualization**
    *   Attempt to group articles based on their 'Categories' field (this might require some text processing or manual categorization of the 100 articles based on their primary theme).
    *   Analyze the research question: Compare characteristics (e.g., average word count, reference density) across different identified groups/sub-categories. Use box plots or similar visualizations.
    *   Investigate potential outliers identified during EDA.
    *   Develop key visualizations that effectively communicate the main findings regarding the structure and characteristics of science articles in the sample.
    *   Refine analysis and visualizations based on initial findings. Commit progress to GitHub.

*   **Week 4: Interpretation, Reporting & Finalization**
    *   Interpret the results of the analysis in the context of the research question and motivation. What do the patterns (or lack thereof) suggest about science articles on Wikipedia?
    *   Write a final report or presentation summarizing the project goals, methodology, findings, limitations, and potential future work.
    *   Ensure the GitHub repository is well-organized, contains the final code, dataset, analysis notebooks, and the final report/presentation. Add a comprehensive README file.
    *   Prepare for project submission/presentation.