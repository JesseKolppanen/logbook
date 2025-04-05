
ZAP by Checkmarx Scanning Report

Generated with The ZAP logoZAP on Sat 5 Apr 2025, at 20:30:10

ZAP Version: 2.16.0

ZAP by Checkmarx
Contents

    About this report
        Report parameters
    Summaries
        Alert counts by risk and confidence
        Alert counts by site and risk
        Alert counts by alert type
    Alerts
        Risk=Informational, Confidence=High (1)
    Appendix
        Alert types

About this report
Report parameters
Contexts

No contexts were selected, so all contexts were included by default.
Sites

The following sites were included:

    http://localhost:8000

(If no sites were selected, all sites were included by default.)

An included site must also be within one of the included contexts for its data to be included in the report.
Risk levels

Included: High, Medium, Low, Informational

Excluded: None
Confidence levels

Included: User Confirmed, High, Medium, Low

Excluded: User Confirmed, High, Medium, Low, False Positive
Summaries
Alert counts by risk and confidence

This table shows the number of alerts for each level of risk and confidence included in the report.

(The percentages in brackets represent the count as a percentage of the total number of alerts included in the report, rounded to one decimal place.)
	Confidence
User Confirmed 	High 	Medium 	Low 	Total
Risk 	High 	0
(0.0%) 	0
(0.0%) 	0
(0.0%) 	0
(0.0%) 	0
(0.0%)
Medium 	0
(0.0%) 	0
(0.0%) 	0
(0.0%) 	0
(0.0%) 	0
(0.0%)
Low 	0
(0.0%) 	0
(0.0%) 	0
(0.0%) 	0
(0.0%) 	0
(0.0%)
Informational 	0
(0.0%) 	1
(100.0%) 	0
(0.0%) 	0
(0.0%) 	1
(100.0%)
Total 	0
(0.0%) 	1
(100.0%) 	0
(0.0%) 	0
(0.0%) 	1
(100%)
Alert counts by site and risk

This table shows, for each site for which one or more alerts were raised, the number of alerts raised at each risk level.

Alerts with a confidence level of "False Positive" have been excluded from these counts.

(The numbers in brackets are the number of alerts raised for the site at or above that risk level.)
	Risk
High
(= High) 	Medium
(>= Medium) 	Low
(>= Low) 	Informational
(>= Informational)
Site 	http://localhost:8000 	0
(0) 	0
(0) 	0
(0) 	1
(1)
Alert counts by alert type

This table shows the number of alerts of each alert type, together with the alert type's risk level.

(The percentages in brackets represent each count as a percentage, rounded to one decimal place, of the total number of alerts included in this report.)
Alert type 	Risk 	Count
Authentication Request Identified 	Informational 	1
(100.0%)
Total 		1
Alerts

    Risk=Informational, Confidence=High (1)
        http://localhost:8000 (1)
            Authentication Request Identified (1)
                POST http://localhost:8000/login

Appendix
Alert types

This section contains additional information on the types of alerts in the report.

    Authentication Request Identified
    Source 	raised by a passive scanner (Authentication Request Identified)
    Reference 	
        https://www.zaproxy.org/docs/desktop/addons/authentication-helper/auth-req-id/

