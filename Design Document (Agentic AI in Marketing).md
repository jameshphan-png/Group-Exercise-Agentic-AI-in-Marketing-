**Ad Optimization Agent Overview**

1. Agent Role

The goal of this agent is to improve digital advertising performance by evaluating datasets and allocating budgets across digital channels. 3 channels will be evaluated: Search (Google), Social (Facebook), and Display (Sprouts Market). These 3 channels will span over the course of \~14 days, during which the agent will identify and recommend what may optimize for conversions (Click-through rate). It will continuously monitor and refine data to produce more optimal results, and create a comparison based on the agent’s approach vs. an equal-split baseline (where all 3 channels get a 33% budget split each overall).

2. Inputs & Outputs

Inputs will be primarily focused on the data columns from all 3 channels: Date, channel, spend (budget spending), impressions, clicks, and conversions. In addition to this, we will also use the following columns and several tools to help analyze metrics for results, which are performance metrics, bid adjustments, pause ad groups, and request new creatives. 

Outputs, on the other hand, will produce decision previews, based on daily budgets allocated for the day, reasoning for adjusting channel budgets, and a brief status report of conversion results. It’s important to consider the comparisons between agent conversions and baseline performance, as it represents the difference between how much the AI agent optimized overall. Furthermore, there will also be a brief paragraph describing the results in detail, as well as the conditions used (guardrails, heuristics), and overall evaluation as final results.

3. Rules/Guardrails   
* The capacity for budget allocation for channel(s) cannot go above/below 20% per-day  
  * Prevent fluctuations in data to evaluate overall consistency in metrics  
  * Evaluates CTR,CVR, and CPA, to gather data and identify patterns  
* Exploration begins with a 33/33/33 split towards Search, Social, & Display channels  
* Explanation should always be followed up when budget allocation changes for channel(s)  
  * Enable transparency to identify why this is “optimal.” 

4. Evaluation Metric

Upon the results, the optimization agent will evaluate the output based on certain parameters

* Primarily, total spend, impressions, clicks, and conversions will be evaluated as a measure to indicate the frequency of the CTR/Conversion Rate overall (when comparing the Agent’s optimization to a baseline approach)  
* Followed along, it will also include secondary parameters, such as average CTR (conversion), cost per acquisition, etc  
  * Further producing more insights, i.e. is this agent more effective at optimizing an advertisement for a daily channel?