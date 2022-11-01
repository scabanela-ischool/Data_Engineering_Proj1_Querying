# Project 1: Query Project

## Introduction

Project 1 will be an individual project to analyze a sales database.  You will be working in Cloud, specifically in Amazon Web Services, in the official course VM, in a docker cluster running one container for Anaconda (Python distro) and one container for Postgres (SQL-based relational database).   You will be writing Python, Pandas, and SQL code in a Jupyter Notebook for your analysis and will be creating data visualizations to enhance your analytics.

Postgres is an open source database that is famous for separating the SQL engine (front end) from the database engine (back end).  Because of this, most modern databases, especially cloud databases, are using the Postgres SQL engine paired with their own back end.  Their back ends can support all levels from small serverless SQL, to mid-range, to gigantic data warehousing.  Some backends are transactional for executing the business, and some are analytical for evaluating the executing the business.  So, the Postgres dialect of SQL is a great addition to your skills set!

## New Skills

These are the new skills you should gain from this project.  Reading through this list of new skills, most of these skills you will be using regularly in your data science career:

* Expand your GitHub knowledge (working on a branch, creating a pull request, etc.)
* Design queries using a Data Model in ERD format (versus hack style SQL based on just looking at tables and guessing)
* Using a secondary dataset to enhance a primary dataset
* Open ended business questions from executives: analyzing, giving an answer, and supporting that answer with data
* Designing an appropriate data visualization to present supporting data
* Functional programming using Python and SQL
* Working in the Linux command line
* Working in the cloud (AWS)
* Working in a VM in the cloud instead of physical computer
* Working in a cluster of Docker containers running inside a VM in the cloud

## Business Case Scenario

A few years ago, a new startup was born: **Acme Gourmet Meals (AGM)**.

The founder of AGM was a sous chef in a 5-star restaurant, named Joy, who had worked her way up from dishwasher to cook to sous chef.  As part of her job, Joy frequently shopped at the high end grocercy stores that featured organic and healtier selections for their food, at premium prices, as the 5-star restaurant wanted only the highest quality ingrediants for their food.  Also, part of her job was to be paid to eat meals on her time off at other restaurants from fast food to other 5-star to see what types of food and quality were being served.  

Joy noticed that most young, single professionals tended to:  
* Eat out frequently, with a mix of mostly casual dining, with some fast food, and occasional 5-star restaurants
* Order delivery at home or work
* Take out for home or work
* Buy frozen pre-made meals and microwave them at home

Joy also noticed that all of these options were typically not very healthy.

Joy had an idea to create a new business.  She would cook healthy, gourmet quality meals and fix them in containers similar to the frozen pre-made meals purchased in grocery stores, except they would be fresh (not frozen) to improve the taste.  She would seek to market them at a local high end grocery store. 

Joy struck a deal with the high end grocery store to setup a small counter there near the entry way. At the counter she would educate the customers about her meals, take orders, and delivery them.  As the business grew, Joy rented space near the store and setup her kitchen there, hiring someone else to staff the counter at the grocery store.  Joy also hired a web developer to develop a website to take orders, handle payments, etc.

After a couple of years or so, the grocery store's corporate office was so pleased with the arrangement, they asked AGM to expand to several other cities.  They selected stores in the areas of town with more young professionals, and/or areas known for more affluence.  They provided funding for a joint venture to allow AGM to setup kitchens near the store and enhance the web and phone app ordering system. In exchange for their investment, they received controlling interest in the business.  Joy stayed on, where she would continue to act as an expert on the food side of the business.

AGM has just finished a very successful year on the enhanced computer systems, and now has a database of sales data for one year.

AGM charges a flat rate of $12 per meal with no minimum. Since it's food that has to be heated before eating, it is not subject to sales tax.  Customers must order by 10am one day in order to pick up the meals the next day. The thinking is that AGM will waste much less food that way.  Customers will have a maximum of one order per day.  

AGM has just hired you as their first full stack data scientist to analyze the sales data. The executives have a lot of questions about how the business is doing and how to improve the business.

## Executive Questions

The executives have some very specific questions, as well as some open ended questions:

**Sales Specific Questions**

* Total sales as a dollar amount
  * for all of AGM
  * by store
  * by month
  * by store and month
  * by day of week
  * by store and day of week

* Total number of sales
  * for all of AGM
  * by store

* Average dollar amount per sale
  * for all of AGM
  * by store

* The Executives have also asked you to provide your best example of a data visualization for one of the above queries.

**Customer Specific Questions**

* Total number of customers 
  * for all of AGM
  * by store
  * by distance from store

* List of customers who have signed up but not bought anything

* Using the secondary dataset, what is the percentage of customers per population
  * at the zip code level?
  * at the city level?

* The Executives have also asked you to provide your best example of a data visualization for one of the above queries.

**Product Specific Questions**

* How many meals were purchased?
  * for all of AGM
  * for all of AGM by meal
  * by store and meal
  * by month
  * by month and meal
  * by day of week and meal
  
* Average number of meals per sale
  * for all of AGM
  * by store

* The Executives have also asked you to provide your best example of a data visualization for one of the above queries.

**Suggestions**

It's highly recommended that you use the Data Model in ERD format to design your queries. See the sales_db_erd_data_dict.md file.  The data dictionary also answers a lot of questions about the data:


For data visualizations, keep in mind the recommendations presented in the Asynch.

**Holiday Analytics (open ended)**

How do holidays affect the sales, considering both the actual holiday, and the days before and after the holiday?  Create an executive summary explaining how holidays have affected sales.  You must support your sumary with data, in the form of output of queries, data visualization, etc.  There is a 1 query minimum.

**Best Customer Analytics (open ended)** 

The executives want you to come up with a high level design of a model, in the form of written criteria, to determine who the best customers are.  You do NOT have to code the model.  You do NOT have to give an actual list of best customers. Create an executive summary explaining your model.  You must support your summary with data, in the form of output of queries, data visualization, etc.  There is a 1 query minimum.

**Best Recommendation (open ended)**

The executives would like your best recommendation for the business.  Create an executive summary giving and explaining your best recommendation for the business.  You must support your summary with data, in the form of output of queries, data visualization, etc.  There is a 1 query minimum.

**Suggestions**

For the open ended questions where you are required to provide executive summaries, consider BBI and CCC (triple C):
* BBI
  * Bold
  * Brief
  * Impactful
* CCC (triple C)
  * Clear
  * Concise
  * Convincing

## Grading Rubrics

Semester Weighting
* Project 1
  * 29%
* Project 1 Feedback Acknowledgement
  * 1%

Late Submissions
* Submission time will the date and time the final pull request was created
* If a student forgot to create the pull request, but their last commit was before the due date and time, they will be allowed to create a pull request with a penality of -1 in lieu of the hours based late submission penalty
* 1 second late to 24 hours late: penalty -5
* 24 to 48 hours late: penalty -10
* 48 to 72 hours late: penalty -15
* 72 to 96 hours late: penalty -20
* No submissions will be accepted after 96 hours late

Objective 
* 80% 
* Right or wrong
* GitHub procedures
* Sales Specific Questions
* Customer Specific Questions
* Product Specific Questions

Subjective 
* 20% 
* Personal opinion
* Holiday Analytics
* Best Customer Analytics
* Best Recommendations

**Objective Items 80%**

GitHub procedures
* Maximum deduction for GitHub procedures: -3
* Did not name the repo the name given in proper case, penalty -1
* Did not name the branch the name given in proper case, penalty -1
* Altered the main branch, penalty -1
* Did not name the Jupyter Notebooks the names given in proper case, penalty -1
* Non-essential files were checked in, such as checkpoint files and directories, penalty -1
* More than 1 open pull reqeust, penalty -1

Queries for Sales Specific Questions, Customer Specific Questions, Product Specific Questions
* Did not provide a query, penalty -2
* Provided a query, but answer was wrong, penalty -1

Data Visualizations Sales Specific Questions, Customer Specific Questions, Product Specific Questions
* Did not provide a data visualization, penalty -2
* Provided a data visualization, but did not properly title the data visualization, penalty -1

**Subjective Items 20%**

Grader will evaluate the quality of the three executive summaries:
* Holiday Analytics
* Best Customer Analytics
* Best Recommendations

Here are the main scores and their criteria.  Grader may award scores in between if they feel a submission was in between.

Above 15/20 is very hard and very rare to achieve.

20/20
* Absolute perfection in all aspects
* Publication quality - similar to what would be published in an industry journal
* If reviewed by a data science team prior to presentation, no minor edits would be suggested
* All three executive summaries provided, with 1 query minimum each

17/20
* Excellence above and beyond
* Publication quality - similar to what would be published in an industry journal
* If reviewed by a data science team prior to presentation, no more than two minor edits would be suggested
* All three executive summaries provided, with 1 query minimum each

15/20
* Excellence above and beyond
* Publication quality - similar to what would be published in an industry journal
* If reviewed by a data science team prior to presentation, several minor edits would be suggested, but no major edits would be suggested
* All three executive summaries provided, with 1 query minimum each

13/20
* Excellent work
* Very high quality
* Very strong arguments
* If reviewed by a data science team prior to presentation, several minor edits would be suggested, but no more than one major edit would be suggested
* All three executive summaries provided, with 1 query minimum each

10/20
* High quality
* Very strong arguments
* All three executive summaries provided, with 1 query minimum each

8/20
* High quality
* Strong arguments
* At least two of the three executive summaries provided, with 1 query minimum each

6/20
* High quality
* Strong arguments
* At least one of the three executive summaries provided, with 1 query minimum

4/20
* Low quality
* Weak arguments

0/20
* No submissions for any of the three executie summaries

