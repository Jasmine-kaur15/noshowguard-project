# NoShowGuard

Repository: https://github.com/Jasmine-kaur15/noshowguard-project

## Findings

Part 1: The dataset contains 990 appointments across 8 clinics, with 218 no-shows (22.0%).
Part 2: Gomti Nagar Care Point had the highest clinic rate, 33.3%, across 90 appointments.
Part 3: The selected model was [selected model], chosen using training-set cross-validation; the selected threshold was 0.35.
Part 4: The 10-note review found 5 appointments with no reminder recorded; both notes classified as forgotten/no reminder had `reminder_sent = No` (2 of 2).

## Recommendation

Use the selected model’s risk scores to help the front desk prioritize evening follow-up calls. The dataset had 218 no-shows among 990 appointments (22.0%), and Gomti Nagar Care Point’s rate was 33.3% across 90 appointments. At the 0.35 threshold, my test evaluation flagged 31 appointments, with precision 0.613, recall 0.388, and ROC-AUC 0.732. The note review also found that 5 of 10 appointments had no reminder recorded. These results can guide a follow-up pilot, but the clinic should set its working threshold based on evening call capacity and the cost of an empty slot.

## Limitations

- The 10 notes are an illustration and cannot show the real reasons clinic-wide.
- The same patient can appear in both the training and test sets.
- The split is random, not past-to-future.
