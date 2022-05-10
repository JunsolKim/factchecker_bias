# factchecker_bias

## Goal
  - Analyzing whether partisan bias exists among fact-checkers

## Organization-based fact-check label data
  - Data: `factcheck_organization_data_20220508_party.csv`, Code: `collect_organization_claimreview_data.ipynb`, Variable description: `factcheck_organization_data_codebook.txt`
  - Features
    - Google and Duke Reporters' Lab created tagging system for organization-based fact-checks, called [ClaimReview](https://www.claimreviewproject.com/). This system allows us to collect entire fact-checks generated by entire US-based fact-checking organizations (including independent fact-checking organizations and news media).
    - Fact-checks on 31,107 claims done by 794 fact-checkers in 9 organizations between 2007 and 2022 are collected. [Google Fact Check Markup Tool feed](https://datacommons.org/factcheck) and web crawling method are used.
      - Independent organizations
        - Politifact (N=20,872)
        - Lead Stories (N=4,530)
        - CheckYourFact (N=3,194)
        - FactCheck.org (N=1,084)
      - News media
        - The Washington Post (N=348)
        - Newsweek (N=258)
        - Dispatch (N=140)
        - USA Today (N=100)
        - New York Times (N=65) 
      - Excluded organizations
        - Snopes.com: Data not standardized
        - Health Feedback, Science Feedback: Focused solely on health and science
        - Polygraph (Voice of America): Targeting international audience
        - CBS News: Few data
    - For some claims, we have URLs where the claims first appeared.
    - We have 225 claims that are cross-factchecked by multiple factcheckers/organization (matched by URLs where the claims appeared).
    - Speaker's party information was appended on the data based on PolitiFact data (https://www.politifact.com/personalities/).

## Community-based fact-check labels
  - Twitter BirdWatch data
