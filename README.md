# Premier League 2024/2025: Player & Squad Performance Tracker

An interactive Excel dashboard exploring player productivity, playing time, age groups, penalty contributions, and nationality composition.
- **Tools**: Microsoft Excel, Power Query, Power Pivot, DAX, PivotTables, and PivotCharts
- **Project**: Data Modelling group project, BINUS University
- **My role**: Team Leader and contributor to data modelling, DAX, dashboard design, and final deliverable review

## Project Overview
This project transforms football player statistics into an interactive dashboard for exploring player and squad performance. The intended users are team managers, club analysts, scouts, and recruitment teams.
The analysis examines attacking contributions alongside playing time, age distribution, and penalty dependence. It provides descriptive evidence for squad discussions and identifies areas that need further investigation.

## Dataset & Data Model
Source: Premier League 2024-2025 Data by furkanark on Kaggle.
The project report describes an initial dataset of 574 rows and 25 columns. The supplied workbook contains 573 player-club records, 20 squads, and 4 retained position categories. Player_ID combines the player's name and squad, so the row count should not be interpreted as a count of distinct individuals.

| Table | Purpose | Loaded records |
| --- | --- | ---: |
| `Fact_PlayerStats` | Playing-time, attacking, penalty, and disciplinary statistics | 573 |
| `Dim_Player` | Player-club identifiers, names, nationality, age, birth year, and age group | 573 |
| `Dim_Squad` | Squad identifiers and names | 20 |
| `Dim_Position` | Position identifiers and categories: DF, MF, GK, FW | 4 |

The loaded dimension keys are unique, and all loaded fact-table keys have matching dimension records.

## Dashboard Features
### KPI Summary
- **Top Attacker**: Player or tied players with the highest combined goals and assists.
- **Most Minutes Played**: Player or tied players with the most recorded minutes.
- **Average Age**: Mean player age in the selected context.
- **Total Goals**: Total recorded player goals in the selected context.
### Visualisations
- Goals and assists by player.
- Playing time compared with age.
- Total playing time by age group.
- Penalty and non-penalty goal contributions.
- Nationality composition for the ten displayed country groups.
- - A disciplinary-ratio chart; its per-90 values require correction before interpretation.
### Interactive Controls
Squad, Position, and Age Group slicers control the charts. A separate Squad dropdown controls the KPI cards through CUBEVALUE worksheet formulas referencing Power Pivot measures.
Select both sets of controls consistently when comparing a squad's KPI cards with its charts. The saved workbook has Crystal Palace selected for the KPI cards.

## Key Findings

| Finding | Interpretation |
| --- | --- |
| Mohamed Salah recorded **29 goals and 18 assists**, totalling **47 goal contributions**. | Goals and assists together provide a broader view of attacking contribution. |
| The loaded statistics total **1,082 player goals**. | The dashboard summarises attacking output across the recorded squads. |
| The **22–28 age group** accounts for **483,469 minutes (64.4%)**.<br>The **21-and-under group** accounts for **94,986 minutes (12.6%)**, and the **over-28 group** for **172,473 minutes (23.0%)**. | Playing time is concentrated among players aged 22–28, providing context for rotation and youth-development discussions. |
| Nathan Collins recorded **3,420 minutes** as an outfield player. | High playing time indicates substantial team usage, although it does not establish fatigue or injury risk. |
| Justin Kluivert recorded **12 goals, including 6 penalties**.<br>Matheus Cunha recorded **15 goals with no penalty goals**. | Players with similar attacking roles can have different penalty and non-penalty scoring profiles. |
| England accounts for **194 of 573 player-club records (33.9%)**.<br>Brazil accounts for **34 records**, the largest overseas country group. | England is the largest nationality group in the loaded dataset. |

## My Contributions
As the leader of a six-member team, I:
- Assigned tasks to individual team members.
- Helped develop the data model and DAX measures.
- Designed dashboard visual elements, including colour choices and chart selection, particularly the nationality pie chart.
- Analysed project errors and helped the team identify issues requiring correction.
- Assisted with the report and PowerPoint presentation and performed their final review.

## Contributors
- Nacito Florisen Astari
- Aditya Maulana
- Aditya Naufal Erlangga
- Gideon Manggaprouw
- Mohamad Arya Fadlullah
- Thio Michael Yulianto


