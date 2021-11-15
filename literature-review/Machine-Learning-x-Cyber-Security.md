# Machine-Learning-x-Cyber-Security

## Machine Learning Based Cyber Attacks Targeting on Controlled Information: A Survey
keywords: leak, information, train, attack

### Intro
ML-based stealing attack: Attacker utilizes an ML algorithm to build up a computational model to disclose the controlled information, while the raw data set is collected in legitimate ways.

Out of scope: disrupt, disable, destroy, or maliciously control a computing environment, and destroy the integrity of the data. Example DDoS attack leaking customer data [14]

Three common vulnerabilities subject to the controlled information stealing attacks:
1. User activity information [26], extracting user's foreground app Android [97]
2. Exploitation in ML and training data, particularly those host Machine-Learning-as-a-Service (MLaaS) [125] [9,51,81,120]
3. Authentication information

ML applied in :
- Cyber attack prediction [123] 
- Insider threat detection [77]
- Network traffic classification [78, 146-148]
- Spam detection [17]
- Software vulnerability detection [73]

![](attachments/Pasted%20image%2020211116005325.png)

Methodology of ML-based stealing attack (MLBSA):
- reconnaissance
- data collection (weaponization in cyberkill chain)
- feature engineering (delivering the weapon to the victim, exploiting the vuln, installing malware, cnc)
- attacking the objective
- evaluation

ML services allow access from users, only training data is considered as confidential. Stealing attack against a model [125, 131] or training samples [34, 49, 116]

Using ML to infer the password from user's keystrokes [79, 122]

Interacting with the operating system [79, 122,42, 152]




> ML reconstruction attack[34], GAN Attack, Analyzing big data and build predictive models [125, 131] using Google Prediction API or Amazon SageMaker,
> Other survey: [3, 7, 31, 145]