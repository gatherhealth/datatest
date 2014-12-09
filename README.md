Overview
===========
Gather Health Data Analysis Homework

In this project, you get to analyze the [blood glucose](http://en.wikipedia.org/wiki/Blood_sugar) readings taken from a collection of patients.  Analyzing the progression of a patient's blood glucose can provide valuable insight into how their health is evolving.

Generally, a healthy patient's blood glucose readings stay between 70 and 100 mg of glucose per deciliter of blood.  A healthy patient can control their readings, so that they rarely fall outside of this range.

An unhealthy patient has difficulty controlling their blood glucose readings.  There may frequently be dangerous episodes during which their blood glucose falls far outside of this range.

In other words, an unhealthy patient's readings will often have a higher standard deviation than those of a healthy patient.

We often abbreviate "blood glucose" to "BG"

Data Format
============
We have two tables: one table with basic patient information, and another containing blood glucose readings.

The data is provided as a collection of CSVs in order to minimize setup time, and to let you use your preferred programming language.

Each patient is associated, via a foreign key, with a collection of blood glucose readings.  These readings evolve over time.


Patient Information Table:
---------------------------
This table has three columns:
* `id`: Integer, Primary Key
* `age`: Integer, patient's current age
* `name`: String, patient's name
* `diabetes_type`: String, either `"type_1"` or `"type_2"`, describes [cause of diabetes](http://en.wikipedia.org/wiki/Diabetes_mellitus#Causes)
* `join_date`: Date when user started using the app.  Format is `YYYY-MM-DD`

Blood Glucose Reading Table:
-----------------------------
* `id`: Integer, Primary Key
* `bg`: Float, describes the patient's Blood Glucose at time of measurement
* `patient_id`: Foreign key to the Patient Information table
* `date`: String, describes date on which measurement was taken.  Format is `YYYY-MM-DD`

Notice that the readings higher primary keys also have later dates.

Assignment
===========

Please write code to answer the following questions.

* Are Type 1 patients better at controlling their BG than Type 2 patients?  Are Type 2 patients better?
* Are there any patients whose performance is clearly deteriorating or improving?
* Does age or gender appear to have an influence on a patient's ability to control BG?

Please submit your code by forking this repository and sending us a link to the fork.
