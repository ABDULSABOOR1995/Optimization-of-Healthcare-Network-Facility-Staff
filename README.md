# Optimizing a Healthcare Network for Improved Service Delivery

## 1 INTRODUCTION
The Washington State Health Ministry would like to optimally upgrade staff or resources in existing
facilities across Washington so that they can allocate resources to where they are most needed, based
on demand for services in different geographic regions/areas.
To address this problem, the health ministry needs to:<br>
* Make services more accessible by allocating resources to where they are most needed;
increasing capacity in some facilities and decreasing capacity in others.<br>
* Minimize people’s travel time so that they only travel to their nearby facility. <br>

### 1.1 SAMPLE PROBLEM
Majority of the population living in Area A need access to health services, but would need to travel on
average 2 hours per return trip to get their needs met in Facility B, instead of travelling 0.5 hours to their
nearby Facility A. This is because Facility A has only 21 staff/resources as opposed to 52 staff in Facility
B. People living in Area A cannot travel this far, so they need to get their needs met by Facility A,
otherwise they go without healthcare.

### 1.2 DESIRED SOLUTION 
To model how many staff members should be shifted from Facility B to Facility A, so that the population
living in Area A can travel to their nearby Facility A instead of Facility B, improving travel cost/access to
healthcare.
Depending on the level of care, a rule of thumb is that the healthcare worker to patient ratio should be
approximately 1:2808 in order to not overwork staff members. So 1 healthcare worker can reasonably
serve 2808 standard patient needs a year. Not the entire population living nearby a facility would need
healthcare services, but we assume at least more than half would seek services for a variety of
problems. 

### 1.3 DATA SOURCES 

Facility ID | Facility Area-Zipcode | Facility Staff Count
----------  | --------------------- | --------------------
Facility A | 98007 | 21
Facility B | 98290 | 52
Facility C | 98065 | 43
Facility D | 98801 | 9
Facility E | 98104 | 64

### 1.3.2 Maps 
Example sources: Google Maps, Bing Maps, HERE, etc.
These sources can be used for estimating average travel time for people traveling to a facility in their
area or nearby their area, and the average travel time to all other facilities.\

### 1.3.3 Population 
<b>Example sources:</b> US Census Bureau, World Population Review, etc.

These sources can be used to grab population estimates in facility zip areas and nearby areas.

## 2 DELIVERABLE
Write a short technical document addressing the following:<br>
* <b>Introduction:</b> What is your understanding of the problem? Can you write the introduction
and the problem statement in formal conference paper-like format?
* <b>Assumptions:</b> What assumptions would you make to simplify the problem?
* <b>Data gathering, handling, cleaning, processing:</b> How would you acquire the data? What
steps would you perform to process or clean the data? How would you extract useful data
inputs for this task?
* <b>Proposed Solution:</b> Share your optimization technique and any necessary details.
* <b>References:</b> Cite any libraries, APIs, publications. We believe in standing on the shoulders of
giants. Please reuse any existing research papers, source code, libraries but make sure to
cite them.
* <b>Source code:</b> Share your R or Python source code.
