{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "48e042b2-6857-4b18-8d08-58cf271c4fc6",
   "metadata": {},
   "source": [
    "# Reflection — The Dirty Ledger\n",
    "\n",
    "## 1. What problems did I identify?\n",
    "\n",
    "The initial inspection revealed missing prices, inconsistent numeric formatting, unusually high values, inconsistent item capitalisation and an exact duplicate observation.\n",
    "\n",
    "Further investigation revealed a conflicting date-item-city combination. On 5 February, the item labelled oil b for City 1 had a price of 108.5, while another Oil B observation existed for the same date and city with a price of 318.0.\n",
    "\n",
    "## 2. Where did my decisions differ from the AI's suggestions?\n",
    "\n",
    "I did not automatically accept every suggested cleaning operation. Suspicious prices such as 1250 and 9999 were not replaced because the dataset did not provide evidence of their correct values.\n",
    "\n",
    "I also preserved the original item labels and flagged the conflicting Oil B records rather than assuming that one of them was incorrectly labelled.\n",
    "\n",
    "## 3. Which decisions were better supported?\n",
    "\n",
    "Removing the exact duplicate was justified because the observations were identical.\n",
    "\n",
    "Standardising item capitalisation was reasonable, but preserving the original labels was important.\n",
    "\n",
    "Flagging suspicious prices instead of inventing replacements was also a better-supported decision because it maintained the original evidence.\n",
    "\n",
    "## 4. What did AI help identify?\n",
    "\n",
    "AI helped structure the cleaning process and introduced a check for repeated date-item-city combinations.\n",
    "\n",
    "This was important because checking only exact duplicates would not identify conflicting records with different prices.\n",
    "\n",
    "## 5. What did I learn?\n",
    "\n",
    "I learned that data cleaning is not simply about removing unusual values or making a dataset look consistent.\n",
    "\n",
    "A value may be unusual without necessarily being incorrect. Cleaning decisions should be supported by evidence, and uncertain observations should be flagged for further investigation.\n",
    "\n",
    "I also learned that AI-generated code should be tested and understood rather than accepted automatically.\n",
    "\n",
    "## 6. Conclusion\n",
    "\n",
    "The dataset originally contained 97 rows. Removing one exact duplicate reduced it to 96 rows.\n",
    "\n",
    "However, there were only 95 unique date-item-city combinations after standardising item labels. This revealed a conflicting observation that requires further investigation.\n",
    "\n",
    "Three prices were excluded from the analysis price column: one missing value and two suspicious high values.\n",
    "\n",
    "The dataset is improved but not fully verified. It is also explicitly labelled as illustrative teaching data, not actual PBS observations, so it should not be represented as official price statistics."
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.14.6"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
