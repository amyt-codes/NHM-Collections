# NHM-Collections
A project for fun to show the current composition of the NHM collections, their place of origin and internal departmental ratings of collection digitisation

This project is an example of my ability to explore a dataset, manipulate and clean the data for analysis, and use Excel to create a dashboard and report.
The original dataset is the publically available Join the Dots collection level records at https://data.nhm.ac.uk/dataset/join-the-dots-collection-level-descriptions which is also in the repository as ‘resource (original).csv’
Prior to cleaning the data, I thought in advance of the data visualisations I wanted to show and the data I would need for this. I have written the steps taken to clean, manipulated and check the quality of data in Excel PowerQuery below.
With the use of Pivot tables, I then created a dashboard showing the current composition of digitised NHM collection records by department and their continent of origin. It also visualises how divisions rate the current quality of their collections’ digitised records and their confidence in the accuracy of their reported counts.
Insights from these visualisations are helpful for identifying divisions to prioritise prior to the next annual specimen collection in checking if the current collection templates meet their needs and what updates could help.
Caveats to this data are that its original dataset is less accurate as it is intended as a discovery tool and indicative view of the museum’s collections rather than an in depth record. In calculating the sites of origin of the collection, the majority of the data was blank (64% had no geographic origin recorded) and so the current composition of sites of origin is likely inaccurate.

Data Visualisations I wanted to ask show
1.	The percentage of total collection item count by department
2.	Visualise a bubble map of items country of origin
3.	Visualise the degree of confidence by department in their reported totals
4.	Visualise a scatter plot of how each department rates their collections digitised records

Steps of Data Cleaning
1.	Select columns of data to extract for dashboard:
a.	_id
b.	Department
c.	Division
d.	Geographic origin
e.	Reporting Count
f.	Reporting metric used
g.	Item count
h.	Item count confidence
i.	Curatorial unit count
j.	Curatorial unit count confidence
k.	C1: Physical accessibility
l.	S1: Strategy/mission/research
m.	S2: Scope and depth
n.	S3: Significance by comparison
o.	S4: Usage
p.	I1: Digitisation
q.	I2: Identification
r.	I4: Development potential
s.	O1: Education suitability
t.	O3: Exhibition suitability

2.	Remove columns
a.	Collection unit ID
b.	Section
c.	Collection unit name
d.	Taxon
e.	Taxon rank
f.	Taxon ID
g.	Taxon ID source
h.	Informal taxon
i.	Type collection
j.	Earliest geological period
k.	Latest geological period
l.	Item type
m.	Preservation method
n.	Curatorial unit type
o.	Bibliographic level
p.	Fond reference
3.	Created conditional column accurately reporting confidence of reporting metric based on method
4.	Reordered this column to be after reporting metric
5.	Entered null values into blank spaces in geographic origin
6.	Then hid the item and curatorial unit count and confidence columns respectively
7.	Changed data type of KPI measures to 1 decimal place

Data quality check
8.	Checked for any duplicate values in unique ID number

Data Validation
9.	Checking each data type was correct when in Excel PowerQuery

Thank you to Kevin Mueller for uploading the photo of the Natural History Museum for public use available at https://unsplash.com/photos/1gUES9J7Ph8
