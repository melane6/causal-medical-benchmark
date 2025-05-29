# causal-medical-benchmark
Main idea is to have trusted causal graph for a collection of disease/condition in centralised platform, where it has combined effort of the state of the art causal discovery algorthims outputs instead of one.

- [ ] 1. Start of with developing this for a group of three conditions -> Diabetes, Breast Cancer and Stroke 
- [ ] 2. Develop an API to store and get causal graphs for each condition 
  - [ ] GET - This would simply return the causal graph in some format(Need to research what the common way is to give this -> I think a CSV maybe) 
  - [ ] UPDATE - This could be done in a different ways. 
    - A user can simply contribute to the benchmark by providing both a script and data to reproduce their new causal graph for the condition.
    - Or, Add/Remove/Modify an edge to throught the review process outline below.
- [ ] 3. Create a process to retrieve a bundle of evidence for each edge in the causal graph for any condition:
  - [ ] Data provence in support of the edge produced by the causal discovery algorthim; this could be the dataset used or clinical trial with the date/timestamp
  - [ ] Literature Support of the edge; Nature/PubMed publications that reports the causal link
  - [ ] Confidence Score of the actual causal link and the weighted value of the causal link?
    - This could be an accumulation of scores:
      - How many times this causal link appears across different causal discovery methods for the same dataset
      - How many times this causal link appears across different datasets
      - How many times this causal link appears subpopulations so like specific age group etc. -> USEFUL to explore this further when looking at Fairness/Bias
      - A summation of the acceptence rate/rejection rate of the edge among experts(In Validation Stage; see below)
- [ ] 4. Create a validation process that involves experts in the field of the condition:
  - [ ] Simple UI that allows clinicians to see the causal graph graphically and in a simple sentences and review the causal graph
  - [ ] To review the causal graph: the expert requires to have had meaning full contruibution to the field of the condition or have medical experience (Probably relax this restriction when starting out)
  - [ ] Review Process:
    - Low confidence edges or edges with conflicting evidence have more urgance/requirement of the review process
    - Reviewers can reject/accept or modify with evidence/comments an edge. The comments can include mistakes that were made or any data issues that may have occured
    - Audit trail of all the changes to each edge with details of the Expert(researcher/clinician) related to change to credit contribution to the causal graph and provide crediability to the causal graph
- [ ] 5. Nightly jobs to check for new papers that could be related to certain condition and flag a review in certain cases with the reason of a new paper in the field



