# Assignment: Questionnaire Design and Sample Evaluation

## Requirements

The goal of this assignment is to practice developing and evaluating sampling materials.

### Part A - Survey Design:

Select one of the scenarios below and design a survey to meet the need(s) outlined in the prompt.

1.	In two to three sentences, describe the purpose of your survey
2.	Describe your target population, sampling frame, sampling units, and overall sampling strategy.
3.	Write a 5-10 question survey to address your chosen scenario below.

##### Scenarios
1.	You work in the Human Resources Department at a large tech company. Over the past few months, the company has been experiencing a high turnover rate across many of its departments, specifically within the entry- and lower-level positions. The company wishes to understand why this turnover is happening, and what changes need to occur to improve employee satisfaction.
2.	You work for a Canadian national political party during a federal election. Throughout the campaign period, your party has seen relatively high approval ratings, but an opposing party is also polling favorably and may still have a chance to win the election. You are one month away from the election and you want to understand what voters want from your party and its leader in order to maintain your lead and eventually win the election.
3.	You are a student researcher in the sociology department at the University of Toronto. You are working on a research project that concerns the relationship between music taste and age. This involves both comparisons between different people of different ages and comparisons of the same individual at different ages during their lifetime. You wish to understand to what extent age influences music taste, specifically as it relates to perceptions of popular music. Your results will be written into an academic paper that you hope to publish.

### Part B - Survey Evaluation:

For the **Canadian General Social Survey on Giving, Volunteering, and Participating, 2018 (cycle 33)**, conducted by Statistics Canada find any and all available documentation for the data gathered and identify and describe the survey features indicated below.

1. Sample type
2. Sample size
3. Target population
4. Sampling frame
5. Survey mode(s) 
6. Timeline
7. Response rate
8. Weights
9. Data processing
10. Cleaning, imputation, etc
11. Sources of error
12. Limitations, known biases, etc
13. Link to documentation and any additional sources used


# Your Changes

## Part A - Survey Design: 

The number of your chosen topic: `#`

Describe the purpose of your survey:
```
The purpose of the survey below is to gather insights from eligible Canadian voters about their political opinions and policy priorities on key social, economic, and environmental issues. The survey intends to analyze voter interest and concern with policies which the Crimson Dawn Party (CDP) is campaigning on. The findings aim to help the party with better messaging and targeted strategic campaigning to win the support of progressive Canadians. 
```

Describe your target population, sampling frame, sampling units, and observational units:
```
The target population is all eligible voters (18 years and older) residing in Canada. The sampling frame can be a voter registration list maintained by the Election Commission of Canada. Sampling units would be individuals chosen randomly from the sampling frame (say 10,000 distributed across different provinces). Alternatively, one can also use telephone directories as the sampling frame with households as the sampling unit.

A stratified random sampling strategy can be adopted for this political survey. The target population should be stratified by factors like province and age. This would allow for collection of more specific voter interests which would in turn allow for more targeted strategies based on provinces or campaign locations like universities for young demographic and so on. Randomly selected individuals should be contacted either through a phone call or email about the survey. Lastly, the statistical analysis should weight the results post collection to account for sampling biases.
```

Your 5-10 question survey:
```
1. Which province or territory do you live in? 
    Optional : Dropdown list of all provinces and territories
2. How would you describe your political leaning?
    Optional : From Very Left to Very Right on a scale of 1-5
3. How important is it to you that Canada increases funding for public services like healthcare and education?
    Answer : Scale of 1-5
4. Do you support stronger government regulation of large corporations to ensure fair wages and working conditions?
    Answer : Scale of 1-5
5. Should Canada implement a universal basic income (UBI) to reduce poverty and income inequality?
    Answer : Scale of 1-5
6. How concerned are you about climate change and its impact on future generations?
    Answer : Scale of 1-5
7. Do you support transitioning to a green economy, even if it means reducing dependence on fossil fuels?
    Answer : Scale of 1-5
8. Should Canada implement more progressive taxation (e.g., higher taxes on the wealthy) to fund social programs?
    Answer : Scale of 1-5
9. What is the most important issue to you when choosing a political party?
    Answer (Select upto 3) : Healthcare, Climate Policy, Housing affordability, Jobs and wages, Education, Better Taxations, Social and indegenous rights.
10. How likely are you to vote for the CDP (Crimson Dawn Party) in the upcoming federal election?
    Answer : Scale of 1-5
```

## Part B - Survey Evaluation:

Identify and describe survey features:

```
The 2018 General Social Survey (GSS) on Giving, Volunteering and Participating, conducted by Statistics Canada, gathered data on how Canadians contribute to their communities through time and money. It used a probability sampling method, along with a technique called rejective sampling, which screened out a portion of non-volunteers early on to better focus on capturing volunteer responses. The final sample included 16,149 completed surveys, excluding about 3,700 rejected non-volunteer cases, while the intended sample size was 20,000. The survey targeted individuals aged 15 and older living in the 10 provinces, excluding those residing in Yukon, Northwest territories, and Nunavut, as well as people living full-time in institutions.

The sample was cross-sectional drawn using a combination of landline and mobile phone numbers (from telephone companies and population census data), along with Statistics Canada’s Address Register, which helped ensure broad coverage of Canadian households. The survey was conducted from early September to late December 2018 and offered two response modes: a self-administered online questionnaire (rEQ) and telephone interviews with trained staff (iEQ). The overall response rate was 41.9%.

To ensure the data reflected the national population, each respondent was assigned a weight that adjusted for design factors like stratification, non-response, and demographic differences. These weights were calibrated to match known population totals by age, sex, province, and income. After collection, the data underwent extensive processing, including editing, coding of open responses, and imputation to address missing or inconsistent answers. Donation amounts in the public dataset were rounded or perturbed slightly to maintain confidentiality without affecting data quality.

As with any survey, the results are subject to sampling error and non-sampling error, such as inaccurate reporting or misunderstanding of questions. Notably, the 2018 cycle is not directly comparable to earlier versions of the survey due to changes in how data was collected and processed, including the introduction of online responses and updates to question wording and definitions. There’s also potential underrepresentation of certain harder-to-reach groups, such as mobile-only households or younger adults.

References
1. <https://www23.statcan.gc.ca/imdb/p2SV.pl?Function=getSurvey&Id=796234#a2>
2. <https://www150.statcan.gc.ca/n1/pub/45-25-0001/cat5/c33_2018.zip>

```

## Rubric

-	All required components are present and complete **Complete / Incomplete**
-	Choice of sampling strategy for Part A is justified and related to survey purpose **Complete / Incomplete**
-	Information for Part B is complete and correct **Complete / Incomplete**

## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `23:59 - 18/04/2025`
* The branch name for your repo should be: `assignment-2`
* What to submit for this assignment:
    * This markdown file (a2_survey_design_and_evaluation.md) should be populated and should be the only change in your pull request.
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sampling/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-2`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via the help channel in Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
