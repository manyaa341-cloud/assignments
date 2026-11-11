{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "80a3d582-8f7f-4c9e-b6e4-c1f45735b42c",
   "metadata": {},
   "source": [
    "# Initial Dataset Diagnosis — Reconstructed\n",
    "\n",
    "**Dataset:** teaching_prices_messy.csv\n",
    "\n",
    "**Purpose:** Identify data-quality problems before cleaning.\n",
    "\n",
    "## 1. Initial inspection\n",
    "\n",
    "The dataset contains 97 rows and 6 columns:\n",
    "\n",
    "- date\n",
    "- item\n",
    "- city\n",
    "- price\n",
    "- unit\n",
    "- data_label\n",
    "\n",
    "The data contains several inconsistencies that could affect analysis.\n",
    "\n",
    "## 2. Problems identified\n",
    "\n",
    "**Missing price:** One observation has no price. I would flag and retain it because the correct value cannot be determined from the dataset.\n",
    "\n",
    "**Inconsistent price formatting:** The value 1,250 contains a comma. I would convert it into a numeric value but investigate whether the resulting price is plausible.\n",
    "\n",
    "**Extreme price:** The value 9999 for Sweetener D appears unusually high. I would flag it rather than automatically replace it.\n",
    "\n",
    "**Inconsistent capitalisation:** The labels Oil B and oil b appear to refer to the same item. I would standardise their capitalisation while preserving the original labels.\n",
    "\n",
    "**Duplicate observation:** An identical Staple A observation for City 1 on 8 January appears twice. I would remove one exact duplicate.\n",
    "\n",
    "**Data provenance:** The dataset identifies itself as illustrative data rather than actual PBS observations. This warning should be preserved.\n",
    "\n",
    "## 3. Expected dataset structure\n",
    "\n",
    "There are 12 dates, 4 items and 2 cities.\n",
    "\n",
    "12 × 4 × 2 = 96 expected date-item-city combinations.\n",
    "\n",
    "The original dataset contains 97 rows, so duplicate and conflicting observations need investigation.\n",
    "\n",
    "## 4. Planned cleaning principles\n",
    "\n",
    "1. Preserve the original dataset.\n",
    "2. Work on a separate copy.\n",
    "3. Standardise labels only when their meaning is clear.\n",
    "4. Convert prices to numeric values.\n",
    "5. Flag missing and suspicious values.\n",
    "6. Remove only exact duplicates.\n",
    "7. Verify all changes using counts and descriptive statistics.\n"
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
