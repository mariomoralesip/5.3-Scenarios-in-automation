What are scenarios in automation?

If the word "scenarios" makes you think about different cases or courses of action one might take, you're on the right path! Scenarios in automation describe different cases defined by an expression, in which the robot takes the proper steps.

Switch chart_NO PROCESS_.png
For instance, after having decided which credit requests are eligible, there are several scenarios that can take place, depending on a given criterion.

In this situation, the transactions are classified into 3 categories that follow different processing protocols:

Fast Approval: a robot compares the request information against a checklist, and then it approves the credit if the request meets all the requirements.
Due Diligence: a robot writes the request information in another document and sends it to the Loan Officers team.
Upper Level: a robot writes the request information in another document and sends it to the Credit Administration team.
How do we translate this to StudioX? Meet the Switch activity!

To avoid using multiple If activities, you can use a single one instead: Switch - also in the common category. How does this work? Considering the example above, if we'd use a series of If activities, our workflow would tell a story like this: 

If Category = Fast Approval, Then do X tasks, Else If Category = Due Diligence, Then do Y tasks, Else If Category = Upper Level, Then do Z tasks, Else Skip request.

Just imagine if we'd have 10 or 15 categories or more!

If series_NO PROCESS_.png
Switch_NO PROCESS_.png
Switch solves this problem!

When configuring the Switch activity, the expression will be the Category, and the cases will be the expression's values: Fast Approval, Due Diligence, Upper Level, and Default.

The Default case corresponds to any value other than the ones defined, for instance: Pending, Needs Attention, SOS or bananas.

Within each case, there are steps to be followed.

In developing the automation you'll use the following input files, websites, and applications:

The "Total transactions - May2022" spreadsheet - all transactions are documented here.
The Double UI app - this is the transaction processing tool.