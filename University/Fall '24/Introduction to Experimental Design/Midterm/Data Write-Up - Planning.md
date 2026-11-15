**Objective**

To import, manipulate, analyze, and interpret a dataset using descriptive statistics in R, focusing on both categorical and continuous data, and to communicate your findings in a clear and concise manner.

**Format**

- 12-point font
- Double-spaced
- Normal margin (1’’ all around)
- Approximately 4 pages for introduction, methods, results excluding references, tables & figures, or R code appendix
- At least 1 table & 3 figures
- APA style throughout


**Deadline & Planning**

Data write-up will be due Monday October 28, 2024 5 PM EST. Please consult the syllabus for late submission policies. Additionally, you have the option to submit the data write-up early on Monday October 14, 2024 5 PM EST. By doing so, you will receive 0.5 points of extra credit. 


You are encouraged to follow the schedule below to plan your writing:

By 10/7: 
- confirm variables of interest
- start preliminary literature search
- import data into R
- manipulate/clean data and fill out the demographic table

By 10/14: 

- complete literature review
- write the introduction section
- fill out the demographic table
- make Figure 1-3

By 10/21:

- write the method and result sections 
- format the write-up based on APA format
- comment and clean up the R code for the appendix

By 10/28:

- consult writing tutors for revisions
- polish the writing
- check the formatting/content related to the grading rubric/organization guide below
- compile and submit the data write-up by 5 PM EST

**Organization**

The data write up should consist of five sections: Introduction, Methods, Results, Tables & Figures, Reference, and R Code Appendix. Expectations and instructions for each section is outlined below:

**Introduction** should consist of roughly three to five paragraphs. 

- **_Introductory Paragraph_**: to introduce your research subject that would quickly capture readers’ attention. This paragraph should describe the significant gap in knowledge that directly relates to a critical scientific need. It should include the following information:
	- _First Sentence/Hook_: Explain what your research topic is and why it is critical that you conduct the research.
	- _What is Known_: Summarize what is currently known in the specific field (1-3 sentences). Provide the reader with only the necessary details to understand why you are proposing the work. Remember to be concise and focus on only the key points.
	- _Significance_: Clearly state how your research will fill a gap in knowledge or create positive impact. 
	- _The Critical Need_: Emphasize the significance of the problem you are trying to address. Additionally, it should be clear in this paragraph that your research proposes the next logical step to what is known.

- **_Paragraph 2-4_**: 

	- _Start with a topical sentence in each paragraph_ that summarizes what the paragraph is about.
	- _Variable A Introduction/Definition_**:** Introduce the first variable (Variable A) and briefly explain its significance in psychological research.
	- _Previous Findings on Variable A_**:** Summarize key findings from existing literature about Variable A, highlighting any patterns or trends.
	- _Variable B Introduction/Definition_**:** Introduce the second variable (Variable B) and briefly explain its significance in psychological research.
	- _Previous Findings on Variable B_**:** Summarize key findings from existing literature about Variable B, emphasizing any notable patterns or trends.
	- _Relationship between Variable A and B_**_:_** Introduce any existing literature that specifically addresses the relationship between Variable A and Variable B. 
- **_Concluding paragraph_**: 
	- _The current study_: briefly state the goal for the current study.
	- _Consistencies in the Literature_**:** Highlight any consistent findings or conclusions across studies regarding the relationship between the two variables.
	- _Knowledge Gaps_**:** Point out any gaps, contradictions, or gaps in the literature regarding the relationship between Variable A and Variable B. Alternatively or additionally, sfate why it is important to study Variable A and B based on literature review.
	- _Relevance to Current Study_**:** Explain how the existing literature on these two variables informs and relates to your current data write-up. 
	- _Summarize_ how the dataset/proposed study will address the gaps in the literature.

  

**Methods**

- **_Data Source and Collection_**

	- Dataset Description: Briefly describe the original dataset, including the primary objective of the data collection, the institution or researchers responsible, and the time frame of data collection.
		- _Example:_ The data utilized in this study was sourced from the XYZ Longitudinal Study conducted by ABC University between 2015 and 2020.

- Sampling Method**:** Describe the sampling method used in the original data collection, such as random sampling, stratified sampling, etc.
	- _Example:_ Participants were selected using a stratified random sampling technique, ensuring representation across various demographic groups.

- **_Participants_**

	- Sample Size: Indicate the number of participants in the original dataset and the number you included in your analysis, if different.
		- Example:_ The original dataset comprised 10,000 participants. After applying our inclusion criteria, our analysis focused on 8,500 participants.
	- Demographics**:** Provide a breakdown of the sample in terms of age, gender, ethnoracial identity, and any other relevant demographic variables. 
		- _Example:_ The sample consisted of 52% females and 48% males, with an age range of 18-65 years. The ethnic breakdown was as follows: 60% Caucasian, 25% African American, 10% Hispanic, and 5% other.
		- Additionally, create a demographic table by filling in information below:

  

**Results**
Results will consist of reporting of descriptive statistics for variables of interest. 

- For **_continuous variable_**, report and interpret the following:
	- Central Tendency: Report measures of central tendency (mean, median) for key continuous variables.
	- Dispersion: Report measures of dispersion (standard deviation, range, interquartile range) for key continuous variables.
	- Shape: skewness and kurtosis
	- Visualizations: Include appropriate plots (histograms, boxplots) to visualize distributions. Ensure all plots have clear titles, axis labels, and legends.

- For **_categorical variable,_** report and interpret the following:
	- Frequency and relative frequency: Report frequency counts and percentages for key categorical variables.
	- Visualizations: Include appropriate plots (bar charts, pie charts) to visualize category distributions. Ensure all plots have clear titles, axis labels, and legends.

- **_Visualization and description of two variables together_**
- If both variables are categorical variables: 
	- Compute conditional relative frequency based on your research question. For example, if I am interested in how poverty status differs between genders, I would compute the relative frequency of poverty for male and female separately in order to descriptively compare the poverty rates between male and female.
	- Create either stacked or grouped bar chart corresponding to conditional relative frequency. 

- If both variables are continuous variables: 

- Plot a bivariate scatterplot and describe what you observe.

- If one variable is continuous and the other variable is categorical,

- Compute the mean/variance for each categories of the categorical variable. For example, if I am interested in how ethnoracial identities impact adverse childhood events, I would compute mean/variance of adverse childhood events for each ethnoracial group.
- Plot a stacked/grouped bar chart, or histogram/scatterplot/boxplot of the continuous variable by categories in the categorical variable

- **_Interpretation_**:

- Patterns and comparisons: Discuss any noticeable patterns. 
- Summary: Summarize your main observations from the descriptive statistics.
- Hypotheses: Suggest potential hypotheses or research questions based on your observations.

  

**Tables and Figures:**

- **_Table_**: You should have at least 1 demographic table that are discussed in the Method section. The template is shown at the end of the instruction.
- **_Figures_**: You should have at least 3 figures

- Figure 1: visualization for Variable A
- Figure 2: visualization for Variable B
- Figure 3: Figure from Step 3 of Results section

  

**Reference**_:_ Please adhere closely to APA 7 style and include at least 10 citations.

  

**R Code Appendix:** Please Ensure your code is well-commented so that someone else could understand and replicate your analysis. Please explicitly and clearly use # to highlight the following sections:

- For demographic table
- For Figure 1-3
- For descriptive statistics of each variable
- Include all relevant R code used for data cleaning, manipulation, and visualization.

  

**Grading Rubric**

  

**1. Format** (2 points)

- Font, Spacing, and Margin (0.5 points)

- Adheres to 12-point font, double-spaced, and normal margin (0.5 points)
- Minor deviations from the format (0.25 points)
- Significant deviations or multiple errors in format (0 points)

- Length and Content (1.5 points)

- 4 pages covering introduction, methods, and results (1 point)
- Includes at least 1 table & 3 figures (0.5 points)
- Missing elements or over/under page limit 1 page or more (-0.25 points for each deviation)

2. **Introduction** (4 points)

- Introductory Paragraph (1 point)

- Comprehensive coverage of all elements (1 point)
- Missing 1-2 elements (0.5 points)
- Missing more than 2 elements (0 points)

- Paragraphs 2-4 (2 point)

- Comprehensive coverage of all elements (2 point)
- Missing 1-2 elements (1 points)
- Missing more than 2 elements (0 points)

- Concluding Paragraph (1 point)

- Comprehensive coverage of all elements (1 point)
- Missing 1-2 elements (0.5 points)
- Missing more than 2 elements (0 points)

3. **Methods** (2 points)

- Data Source and Collection (1 point)

- Comprehensive description and sampling method (1 point)
- Missing 1 element (0.5 points)
- Missing both elements (0 points)

- Participants (1 point)

- Comprehensive description of sample size and demographics (1 point)
- Missing 1 element (0.5 points)
- Missing both elements (0 points)

4. **Results** (4 points)

- Variable A Descriptive Statistics (1 points)

- Comprehensive coverage of all elements (1.5 points)
- Missing 1-2 elements (0.75 points)
- Missing more than 2 elements (0 points)

- Variable B Descriptive Statistics (1 points)

- Comprehensive coverage of all elements (1.5 points)
- Missing 1-2 elements (0.75 points)
- Missing more than 2 elements (0 points)

- Visualization and Description of Two Variables (2 points)

- Comprehensive coverage of all elements (2 points)
- Missing 1-2 elements (1 point)
- Missing more than 2 elements (0 points)

5. **Tables and Figures** (4 points)

- Demographic Table (1 points)

- Table is clear, comprehensive, and correctly formatted (2 points)
- Table is present but has minor errors (1 point)
- No table or significant errors in table (0 points)

- Figures (3 points)

- All 3 figures are clear, relevant, and correctly formatted (2 points)
- 1-2 figures are missing or have errors such as missing labels/legends/title/descriptions (1 point)
- More than 2 figures are missing or have significant errors (0 points)

6. **Reference** (2 points)

- Adheres closely to APA 7 style and includes at least 10 citations (2 points)
- Minor deviations from APA 7 style or less than 10 citations (1 point)
- Significant deviations from APA 7 style or significantly fewer citations (0 points)

7. **R Code Appendix** (2 points)

- Code is well-commented, organized by sections, and replicable (2 points)
- Code is present but lacks clarity or organization (1 point)
- No code or significant errors in code (0 points)

  

  

**Resources**

- APA style 7: https://apastyle.apa.org
- How to use BU library for literature search: https://www.bu.edu/library/help/bu-libraries-search/ 
- Writing help at BU: 

- CAS writing center: https://www.bu.edu/writingprogram/the-writing-center/writing-center-policies/
- Education resource center: https://www.bu.edu/erc/programs/writing/

  

  

Table 1

_Template for Table 1_

|   |   |   |   |   |   |   |   |
|---|---|---|---|---|---|---|---|
|N (%) unless otherwise noted||Total Sample|Cis Man|Cis Woman|Trans Man|Trans Woman|Trans GNB|
|Gender identity|(leave empty)|(leave empty)||||||
|Race|White|||||||
||Black|||||||
||Latino|||||||
||Multirace|||||||
||Other|||||||
|Sexual minority identity|Heterosexual|||||||
||Sexual minority|||||||
|Education|High school or less|||||||
||Some college|||||||
||More than college|||||||
|Age, mean (sd)|(leave empty)|||||||

Note. For all variables other than age and gender, total sample column should consist of marginal frequency (marginal relative frequency) whereas other columns should consist of joint frequency (conditional relative frequency conditioned on gender). For gender identity, nonempty cells should consist of frequency (relative frequency). For age, nonempty cells should consist of mean (standard deviation) or mean (standard deviation) of the group with specific gender identity.