## Requirement 1

When the app is started, the user is presented with the main menu, which allows the user to (1) enter or edit current job details, (2) enter job offers, (3) adjust the comparison settings, or (4) compare job offers (disabled if no job offers were entered yet ).

## Answer 1

This is realized by a MainMenu class which functions as the entry point of the system and contains the below 4 methods to perform those 4 operations. When a user opens this app, a MainMenu object will be created and the user interface will be shown which includes 4 buttons allowing the user to perform those 4 operations. Since this is a single user app, any user specific attributes will all be contained within this class.
- enterOrEditCurrentJob()
- enterJobOffer()
- adjustComparisonSettings()
- compareJobOffers()

## Requirement 2

When choosing to enter current job details, a user will: a. Be shown a user interface to enter (if it is the first time) or edit all the details of their current job, which consist of: i. Title ii. Company iii. Location (entered as city and state) iv. Cost of living in the location (expressed as an index) v. Yearly salary vi. Yearly bonus vii. Restricted Stock Unit Award (expressed as a lump sum vested over 4 years) viii. Relocation stipend (A single value from $0 to $25,000) ix. Personal Choice Holidays (A single overall number of days from 0 to 20)

## Answer 2

This is realized by the MainMenu.enterOrEditCurrentJob() method which does the following:
If there is a CurrentJob object in the system, then this method would call the CurrentJob.editInfo() method which shows an interface with the current details of the current job in editable text boxes and allows the user to edit the details and save the change.
If there isn’t a CurrentJob object in the system, then this method would show an interface with empty editable text boxes which allows the user to enter information, and a CurrentJob object will be created with the provided details. Then this CurrentJob object will be assigned to the MainMenu.currentJob attribute. 

## Requirement 3

b. Be able to either save the job details or cancel and exit without saving, returning in both cases to the main menu.

## Answer 3

This will be realized in the user interface using 2 buttons: ‘Save’, ‘Cancel without saving’.

## Requirement 4

When choosing to enter job offers, a user will: a. Be shown a user interface to enter all the details of the offer, which are the same ones listed above for the current job.

## Answer 4

This is realized by the MainMenu.enterJobOffer() method which does the following:
It provides an user interface with editable text boxes allowing the user to enter the details.
A new JobOffer object is created using the provided details and is then added to the job offer array in the MainMenu object.


## Requirement 5

b. Be able to either save the job offer details or cancel.

## Answer 5

Two buttons will be shown on the interface allowing the user to save the new offer or cancel it.


## Requirement 6

c. Be able to (1) enter another offer, (2) return to the main menu, or (3) compare the offer (if they saved it) with the current job details (if present).

## Answer 6

Three buttons will be shown on the user interface to allow the user to enter another offer, return to the main menu or compare with the current job. The last button is enabled only when the offer is saved and there is a CurrentJob object in the system.

## Requirement 7

When adjusting the comparison settings, the user can assign integer weights to: a. Yearly salary b. Yearly bonus c. Restricted Stock Unit Award d. Relocation stipend e. Personal Choice Holidays If no weights are assigned, all factors are considered equal.

## Answer 7

The MainMenu class has the below 5 attributes to store those 5 weights, and they are initially set to 1. The MainMenu.adjustComparisonSetting() method shows an user interface with 5 editable text boxes allowing the user to enter 5 integer weights and update the weight attributes
- weightAYS
- weightAYB
- weightRSU
- weightRELO
- weightPCH

## Requirement 8

When choosing to compare job offers, a user will: a. Be shown a list of job offers, displayed as Title and Company, ranked from best to worst (see below for details), and including the current job (if present), clearly indicated.

## Answer 8

This is realized by the MainMenu.showRankedJobs() method which does the following: 
It calculates a score for each Job object using the provided formula and updates their score attributes.
It sorts all the Job objects by their scores in descending order and displays the titles and company names on the user interface. 

## Requirement 9

b. Select two jobs to compare and trigger the comparison.

## Answer 9

On the user interface in the last step, the user can select 2 Job objects and click a button which would call the compareJobOffers() method with these 2 Job objects as arguments.

## Requirement 10

c. Be shown a table comparing the two jobs, displaying, for each job: i. Title ii. Company iii. Location iv. Yearly salary adjusted for cost of living v. Yearly bonus adjusted for cost of living vi. Restricted Stock Unit Award vii. Relocation stipend viii. Personal Choice Holidays

## Answer 10

The MainMenu.compareJobOffers() method takes 2 Job objects as arguments and compares all the details of these 2 Job objects side by side in the user interface. 

## Requirement 11

d. Be offered to perform another comparison or go back to the main menu.

## Answer 11

The user interface has 2 buttons allowing the user to perform another comparison or go back to the main menu respectively. 

## Requirement 12

When ranking jobs, a job’s score is computed as the weighted sum of:
AYS + AYB + (RSUA / 4) + RELO + (PCH * AYS / 260)
where: AYS = yearly salary adjusted for cost of living AYB = yearly bonus adjusted for cost of living RSU = restricted stock unit award RELO = relocation stipend PCH = personal choice holidays
For example, if the weights are 2 for the yearly salary, 2 for relocation stipend and 1 for all other factors, the score would be computed as:
2/7 * AYS + 1/7 * AYB + 1/7 * (RSUA / 4) + 2/7 * RELO + 1/7 * (PCH * AYS / 260)

## Answer 12

The Job class has a score attribute which is initially set to 0. When the MainMenu.showRankedJobs() method is called, the score attribute of each Job object is calculated and updated using the provided formula.

## Requirement 13

The user interface must be intuitive and responsive.

## Answer 13

This is not represented in my design as it will be handled entirely within the GUI implementation. We will keep the app interface simple and make sure it can adapt to different screen sizes.

## Requirement 14

For simplicity, you may assume there is a single system running the app (no communication or saving between devices is necessary).

## Answer 14

To realize this requirement, our design doesn't have a user class.








