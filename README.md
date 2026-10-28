# Google Trends: AI Tools Comparison

An analysis of worldwide Google Trends search interest for ChatGPT, Gemini, and Microsoft Copilot, completed as a DataCamp guided project (Understanding Search Interest with Google Trends).

## Question

Imagine working as a data analyst at a tech company that monitors the AI tools market. Which tool is gaining the most traction, and how do the three compare over time?

## Data

Weekly Google Trends interest scores (0 to 100) for the three tools, from late August 2023 to September 2024. The file `ai_tools_comparison.csv` is provided inside DataCamp's lab and is not included in this repo.

Columns: `week`, `chatgpt`, `gemini`, `microsoft_copilot`

## Approach

1. Load the data, parse `week` as a datetime, and use it as the index.
2. Check for missing values (none found).
3. Plot all three series over time.
4. Measure consistency as the standard deviation of week over week percent change. The lowest value marks the steadiest tool.
5. Find ChatGPT's largest single week drop in interest, ignoring the final partial week of the data.
6. Average all three tools together, group by calendar month, and find the month with the highest average.

## Results

| Question | Answer |
| --- | --- |
| Most consistent tool | ChatGPT (week over week change std of about 0.09, versus 0.36 for Gemini and 0.25 for Copilot) |
| Largest ChatGPT decline | December 2023 |
| Month with highest average interest | May |

ChatGPT dominates search interest throughout, while Gemini and Copilot stay far lower. Gemini starts to climb in early 2024.

## Files

* `analysis.ipynb`: the full analysis code

## Tools

Python, pandas, NumPy, matplotlib
