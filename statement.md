# Statement of Work: Personal Finance Tracker
## Overview
The Personal Finance Tracker is a command-line application designed to help users categorize their spending into "Needs" and "Wants," track the performance of their investment portfolio, and visualize their financial health through text-based summaries and charts.

## Core Modules and Logic
A. Data Classification (classify_want_need)
The program uses a keyword-based heuristic to automate the categorization of expenses.

Needs: Identified by essential keywords like rent, electricity, medicine, and education.

Wants: Identified by lifestyle keywords like netflix, shopping, zomato, and travel.

Fallback: Transactions that do not match these keywords are tagged as UNCATEGORIZED.

## Transaction & Investment Management
add_transaction(): Captures user input for amount, category, description, and type (Income vs. Expense). It automatically timestamps the entry.

add_investment(): Captures the "Asset Name," "Invested Amount," and "Current Market Value" to calculate unrealized gains or losses.

## Financial Analysis Tools
Summary Module: Calculates the total income, total expenses, net balance, and overall Net Worth (Balance + Current Investment Value).

Wants vs. Needs Analysis: Provides a percentage breakdown of essential vs. discretionary spending to help users follow budgeting rules (like the 50/30/20 rule).

Visual Representation: Uses a simple ASCII bar chart (using * symbols) to provide a quick visual ratio of spending categories.

## Predictive Modeling
Expense Prediction: Uses a simple arithmetic mean of past expenses to estimate the cost of the next transaction.

Investment Growth: Calculates the average growth rate across all assets in the portfolio and projects the future portfolio value based on that average performance.

## Technical Implementation Details
Language: Python 3.54

Data Structures: Uses Lists of Dictionaries (transactions and investments) for volatile in-memory storage.

Error Handling: Implements try-except blocks in input functions to prevent the program from crashing due to non-numeric inputs for currency values.

User Interface: A standard while True loop provides a persistent menu-driven interface.

## Strengths & Limitations
Strength: The inclusion of "Investment Growth" prediction adds a layer of sophistication beyond standard expense trackers.

Strength: The automated tagging system reduces the manual effort required from the user to categorize every single purchase.

Limitation: Data is stored in RAM; all information is lost once the program is terminated.

Limitation: The keyword matching is strict; a typo in the description (e.g., "Grocries") will result in an "UNCATEGORIZED" tag.
