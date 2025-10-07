# United Airlines Flight Difficulty Score

**Project for the United Airlines SkyHack 3.0 Hackathon**

---

### 1. Problem Statement

Frontline teams at United Airlines are responsible for ensuring every flight departs on time. However, identifying high-complexity flights currently relies on manual, inconsistent methods. This project addresses the need for a systematic, data-driven approach to quantify the relative operational difficulty of each flight departing from Chicago O’Hare (ORD).

### 2. Our Solution: The Flight Difficulty Score

We developed a data-driven framework that calculates a daily **Flight Difficulty Score** for every flight. This score synthesizes multiple operational factors into a single, interpretable metric.

The system performs two key functions:
* **Daily Ranking:** Ranks all flights for a given day from most to least difficult.
* **Classification:** Automatically groups flights into three actionable categories: **Difficult, Medium, or Easy**.

This allows for proactive resource planning and helps frontline teams focus their attention on the flights that need it most.

### 3. Key Features & Drivers

Our final score is a weighted sum of five standardized (Z-score) features that our Exploratory Data Analysis (EDA) identified as key drivers of complexity:

| Feature | Weight | Rationale |
| :--- | :--- | :--- |
| **Ground Time Buffer** | 40% | The most critical structural constraint. |
| **Total SSRs** | 25% | A direct measure of passenger assistance workload. |
| **Total Transfer Bags**| 15% | A primary driver of ground handling complexity. |
| **Load Factor** | 10% | Amplifies all other operational challenges. |
| **Total Child Pax** | 10% | Influences boarding and in-flight service needs. |

### 4. Key Insights & Recommendations

Our analysis of the final scores revealed several actionable insights:

* **Most Difficult Destinations:** International long-haul flights to destinations like **GRU (São Paulo), BRU (Brussels), and HND (Tokyo)** consistently ranked as the most difficult.
* **Primary Drivers:** The difficulty for these top destinations was primarily driven by a combination of **low ground time buffers** and a **high number of transfer bags**.
* **Key Recommendation:** We recommend that United implement **proactive resource allocation** for flights classified as 'Difficult'. This includes pre-assigning dedicated teams for transfer baggage and special passenger assistance (SSRs) to these specific flights to mitigate the high risk of delays.

### 6. Repository Structure

```
├── extensive_eda.ipynb   # Jupyter Notebook with EDA on each dataset
├── EDA_RESULTS.ipynb     # The Jupyter Notebook with answers to EDA questions in the hackathon
├── final_ua_p3.ipynb     # The main Jupyter Notebook with all the analysis
├── presentation/         # Contains the final presentation file
└── README.md             # This file
```
