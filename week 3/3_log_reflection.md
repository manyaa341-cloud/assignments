{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "c70fae67-0565-4f17-b152-3503a5f8ca47",
   "metadata": {},
   "source": [
    "Log, Audit Table, and Reflection\n",
    "\n",
    "AI Interpretation Audit Table\n",
    "Claim / Statement from AI: \"Price increases are driven by steady retail adjustments.\"\n",
    "\n",
    "Color Code: Amber\n",
    "\n",
    "How It Was Checked: Checked variance in Python. Intro of \"steady retail adjustments\" lacks direct proof in basic stats.\n",
    "\n",
    "Acceptance Status: Modified / Caution\n",
    "\n",
    "Claim / Statement from AI: \"Sweetener D saw the highest increase at +23.83%.\"\n",
    "\n",
    "Color Code: Green\n",
    "\n",
    "How It Was Checked: Recomputed using percentage change formula in Jupyter Notebook.\n",
    "\n",
    "Acceptance Status: Accepted\n",
    "\n",
    "Claim / Statement from AI: \"Mean and median alignment improves purchasing power by 15%.\"\n",
    "\n",
    "Color Code: Red\n",
    "\n",
    "How It Was Checked: Refers to external consumer income data absent from the teaching sheet.\n",
    "\n",
    "Acceptance Status: Rejected\n",
    "\n",
    "Confused Classmate Transcript Excerpt\n",
    "• Classmate AI: \"Why bother checking both the mean and median if the mean is just the regular average?\"\n",
    "\n",
    "• User: \"If prices spike in one city, the mean gets pulled up while the median stays in the true middle where most transactions happen.\"\n",
    "\n",
    "• Classmate AI: \"Ah, so the median protects you from being skewed by extreme prices?\"\n",
    "\n",
    "• User: \"Exactly. For a newsroom audience, the median shows what typical shoppers actually pay.\"\n",
    "\n",
    "Reflection • Where did the first draft exceed the data? I caught myself assuming external causes (like transport issues) when the ledger only contained raw prices and dates.\n",
    "• What did the audit reveal? The audit forced me to separate strict mathematical observations from unverified assumptions about consumer behavior."
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
