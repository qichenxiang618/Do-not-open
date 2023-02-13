## Requirement 1

1.	When the app is started, the user is presented with the main menu, which allows the user to (1) enter or edit current job details, (2) enter job offers, (3) adjust the comparison settings, or (4) compare job offers (disabled if no job offers were entered yet ).  

## Answer 1

To realize this requirement, I added a MainActivity class which has the below 4 methods to perform those 4 tasks. When a user opens this app, an MainActivity object will be created, and the GUI will show 4 buttons allowing the user to perform those 4 tasks.
- enterOrEditCuJob(): void
- enterJobOffer(): void
- adjustComparisonSetting(): void
- compareJobOffer(): void

## Requirement 2

2.	When choosing to enter current job details, a user will:
a.	Be shown a user interface to enter (if it is the first time) or edit all the details of their current job, which consist of:
i.	Title
ii.	Company
iii.	Location (entered as city and state)
iv.	Cost of living in the location (expressed as an index)
v.	Yearly salary
vi.	Yearly bonus
vii.	Restricted Stock Unit Award (expressed as a lump sum vested over 4 years)
viii.	Relocation stipend (A single value from $0 to $25,000)
ix.	Personal Choice Holidays (A single overall number of days from 0 to 20)

## Answer 2

First of all, I created an attribute in the Job or Company classes for each point in the above list.
This is realized by the MainActivity.enterOrEditCuJob() method which does the following:
- If the there exists a CurrentJob object in the system, then this method would call the CurretJob.editInfo() method which display the current details of the current job on the GUI in editable input boxes and allows the user to edit the details and save the change. 
- If there isn’t a CurrentJob object in the system, then this method would display edtitable input boxes on the GUI which allows the user to enter information, and then initiates a CurrentJob object using the input values provided by the user.
- In either case, the score of this CurrentJob object is calculated using the formula provided.

## Requirement 3

b.	Be able to either save the job details or cancel and exit without saving, returning in both cases to the main menu.

## Answer 3

This will be realized in the GUI using 2 buttons: ‘Save’, ‘Cancel without saving’.

## Requirement 4

3.	When choosing to enter job offers, a user will:
a.	Be shown a user interface to enter all the details of the offer, which are the same ones listed above for the current job.

## Answer 4

This is realized by the MainActivity.enterJobOffer() method which does the following:
- It displays editable input boxes on the GUI allowing the user to input values.
- It creates a new JobOffer object using the provided inputs. During this process, the score of this object is calculated using the formula provided. 

## Requirement 5

b.	Be able to either save the job offer details or cancel.

## Answer 5

This will be realized in the GUI using 2 buttons: ‘Save’, ‘Cancel without saving’.

## Requirement 6

c.	Be able to (1) enter another offer, (2) return to the main menu, or (3) compare the offer (if they saved it) with the current job details (if present).

## Answer 6

This will be realized in the GUI using 3 buttons: ‘Enter another offer’, ‘Return’ and ‘Compare offers’.


## Requirement 7

4.	When adjusting the comparison settings, the user can assign integer weights to:
a.	Yearly salary
b.	Yearly bonus
c.	Restricted Stock Unit Award 
d.	Relocation stipend 
e.	Personal Choice Holidays 
If no weights are assigned, all factors are considered equal.

## Answer 7

This is realized by the MainActivity.adjustCpSetting() method which display editable input boxes on the GUI allowing the user to provide 5 integer weights, and then update the below attributes of the MainActivity object using the provided weights.
- weightAYS: integer
- weightAYB: integer
- weightRSU: integer
- weightRELO: integer
- weightPCH: integer

## Requirement 8

5.	When choosing to compare job offers, a user will:
a.	Be shown a list of job offers, displayed as Title and Company, ranked from best to worst (see below for details), and including the current job (if present), clearly indicated.

## Answer 8

This is realized by the MainActivity.showRankedOffer() method which sort all the Job objects by their scores and display the title and company name columns of this sorted list on the GUI.

## Requirement 9

b.	Select two jobs to compare and trigger the comparison.

## Answer 9

This will be realized in the GUI which allows the user to select 2 jobs and click on a ‘Compare” button to compare them.

## Requirement 10

c.	Be shown a table comparing the two jobs, displaying, for each job:
i.	Title
ii.	Company
iii.	Location 
iv.	Yearly salary adjusted for cost of living
v.	Yearly bonus adjusted for cost of living
vi.	Restricted Stock Unit Award 
vii.	Relocation stipend 
viii.	Personal Choice Holidays 

## Answer 10

This is realized by the MainActivity.compareJobOffer() method which accepts 2 Job objects as arguments and display all the details of these 2 Job objects side by side for comparison on the GUI.

## Requirement 11

d.	Be offered to perform another comparison or go back to the main menu.

## Answer 11

This will be realized in the GUI using 2 buttons: ‘Compare other jobs’, ‘Return’.

## Requirement 12

6.	When ranking jobs, a job’s score is computed as the weighted sum of:

AYS + AYB + (RSUA / 4) + RELO + (PCH * AYS / 260)

where:
AYS = yearly salary adjusted for cost of living
AYB = yearly bonus adjusted for cost of living
RSU = restricted stock unit award
RELO = relocation stipend
PCH = personal choice holidays


For example, if the weights are 2 for the yearly salary, 2 for relocation stipend and 1 for all other factors, the score would be computed as:

2/7 * AYS + 1/7 * AYB + 1/7 * (RSUA / 4) + 2/7 * RELO + 1/7 * (PCH * AYS / 260)

## Answer 12

The scores of the Job objects are calculated when they are created or edited using the provided formula.

## Requirement 13

7.	The user interface must be intuitive and responsive.

## Answer 13

This is realized by keeping the app interface simple and making sure it can adapt to different screen sizes.

## Requirement 14

8.	For simplicity, you may assume there is a single system running the app (no communication or saving between devices is necessary).

## Answer 14

Sure






