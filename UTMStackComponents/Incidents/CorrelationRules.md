The Importance of Being Well-Written
How well is your UTMStack deployment running?
It really comes down to your correlation rules.
Without well-written rules, your UTMStack mutates into a simple security event logger. 
If your correlation rules are misconfigured, UTMStack could well miss an attack or experience performance issues.
So, in addition to the False Positive rules we outlined yesterday, today we'll take an in-depth look at Correlation Rules.
Well-written Rules
UTMStack
Correlation rules are the cogs and gears that output actual positive alerts while avoiding false negatives.

Correlation Rules and You
Cybersecurity correlation rules are a powerful tool for you as a security analyst to identify and respond to threats quickly and effectively.
As an analyst, you need to ensure that your cybersecurity correlation rules are both effective and durable. To achieve this, you should take a few key steps, as follows.
First, it is important to have an understanding of the environment in which the correlation rule will be deployed.
This includes reviewing the UTMStack log activity for which the rule will be written, including the previous alerts and incidents already generated. A good understanding of the threat results in a good correlation rule written.
Know the Environment
Second, when writing a correlation rule, keep an eye out for precision so you can effectively identify malicious activity without generating false positives (bad) or false negatives (very bad).
Code with Precision
Most correlation rules, with practice, will be fairly straightforward for you. More complex correlations may require that you employ a combination of techniques (e.g., fuzzy logic or Bayesian probability models).

Third, it is important to test your correlation rules prior to deployment in order to verify their accuracy and effectiveness.
Test your rules
You should also consider testing different scenarios using various test data sets so that you can gain confidence in your results before deploying them into your UTMStack production environment.
Finally, once deployed into your UTMStack deployment, you should monitor your correlation rules on an ongoing basis.
With time, threat changes or anomalies will inevitably surface, indicating new threats or malicious activity.
Monitor your Rules
By monitoring these rules on an ongoing basis, you can ensure they remain effective and durable over time as new threats emerge and evolve.

These are your deployment's rules, and supplement the UTMStack base correlation rules

As our base correlation rules develop, we update them on GitHub, at https://github.com/AtlasInsideCorp/UTMStackCorrelationRules

