# A/B Test for New Customer Engagement for SaaS Collaboration Platform

### Executive Summary

We identified an important opportunity in improving platform engagement for new customers through changes to the onboarding process. After creating and running an A/B test of the new onboarding experience, we were able to produce a 21% increase in Time to First Collaboration for new customers, and recommend using the variant experience for all new organizations moving forward.
</br>
</br>
### Business Problem

Early engagement for new customers of our platform is one of the key drivers of long-term retention. Many new organizations have shown significant delays in engaging with core product features and inviting their teammates. Where can we make improvements to the new user experience to drive early engagement and collaboration?
</br>
</br>
### Methodology

1. Generate synthetic datasets for this project using ChatGPT.
2. Conduct an Exploratory Data Analysis using SQL to identify areas of opportunity.
3. Based on findings from EDA, recommend an A/B test likely to improve early engagement.
4. Compare test results against control group and baseline metrics to determine the winner.
</br>

### Skills

SQL: Analysis composed of basic queries, CTEs, table joins, aggregates functions, and case expressions.

AI: Used to generate synthetic datasets and create template python code for visualizations (pandas, matplotlib, numpy).
</br>
</br>
### Results & Business Recommendations

Our Exploratory Data Analysis indicated the Onboarding experience was an effective driver of early engagement, but had high friction.

Of our new organizations, 78% engaged with onboarding. Organizations that started onboarding had up to 17% faster Time to First Collaboration Event than the median, and 71% of new organizations only send their first invite after starting onboarding. Unfortunately, only 38% of all new organizations completed onboarding and many new organizations took over an hour to complete onboarding.

Important Note: Starting onboarding is the driver of Time to First Collaboration, while Onboarding Completion has less impact. Once new organizations reach value through onboarding, they tend to abandon onboarding as it is no longer seen as valuable.
</br>
</br>
</br>
<img width="1389" height="490" alt="chart1v2" src="https://github.com/user-attachments/assets/6b7e18d0-c235-4ce8-b66b-9e1298a1746b" />
</br>
</br>
</br>
To improve the onboarding experience, we introduced the following changes in an A/B test with a 50/50 split for February:
- Questionnaire moved to immediately after signup
- Questionnaire reduced to 3 questions, all as dropdowns: Country, Industry, and Company Size
- Questionnaire required for new accounts
- Skippable Invite Your Team screen added to Onboarding, following Questionnaire
- Repository Creation and Management added to New User Tour

After conducting the test, here are the results of the Variant group against the Control group:
</br>
</br>
</br>
<img width="1389" height="590" alt="chart3" src="https://github.com/user-attachments/assets/e83eb06e-72e7-44ed-82d6-e2b1c071a995" />
</br>
</br>
</br>
Primary Metric:
- Median Time to First Collaboration (Hours): 21% improvement
- Control: 345.85
- Variant: 272.67

Secondary Metrics:
- p75 Onboarding Length (Hours): -5% decline
- Control: 0.22
- Variant: 0.23

- p75 Time to First Invite (Hours): 98% improvement
- Control: 95.40
- Variant: 1.57

- % Onboarding Completion: 58% improvement
- Control: 40.00%
- Variant: 63.33%

Guardrail Metric:
- % Onboarding Abandon: 42.86%
- Control: 23.33%
- Variant: 13.33%

Based on the results of our test, we strongly recommend going live with the new Onboarding Experience used in the Variant group immediately with a 1 month monitoring period before further testing.
