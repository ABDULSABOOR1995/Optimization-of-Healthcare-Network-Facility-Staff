# Optimizing a Healthcare Network for Improved Service Delivery

## 1. INTRODUCTION
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
area or nearby their area, and the average travel time to all other facilities.

### 1.3.3 Population 
<b>Example sources:</b> US Census Bureau, World Population Review, etc.

These sources can be used to grab population estimates in facility zip areas and nearby areas.

## 2. DELIVERABLE
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


# Coded Solution of Given Problem
### 1. Data Gathering:
First of all we collect data from <b>"Washington Demographics"</b> and make its dataframe.
<br><br><br>
![Screenshot_46](https://user-images.githubusercontent.com/46135898/68156662-124c8180-ff6e-11e9-8d7c-dc342aa8c262.png)
<br><br><br>

### 2. Data Understanding:
Then we start understanding data by applying basic pandas statistical methods on the above data frame.
<br><br><br>
![Screenshot_47](https://user-images.githubusercontent.com/46135898/68156675-16789f00-ff6e-11e9-873d-4ae346b26765.png)
<br><br><br>
![Screenshot_48](https://user-images.githubusercontent.com/46135898/68156679-17a9cc00-ff6e-11e9-99b5-45f57291092c.png)
<br><br><br>

### 3. Data Cleaning:
Now we prepare data for analysis by removing unnecessary columns that exists in above table(data frame) and changing dtype of columns from object to int32.
<br><br><br>
![Screenshot_49](https://user-images.githubusercontent.com/46135898/68156681-18daf900-ff6e-11e9-8be5-a80c6b6b6d49.png)
<br><br><br>
![Screenshot_50](https://user-images.githubusercontent.com/46135898/68156683-19738f80-ff6e-11e9-9007-807a8d39aec3.png)
<br><br><br>

### 4. Data Manipulation:
After that, we 'll manipulate or prepare data in the format that is suitable for finding solution of the problem.
<br><br><br>
![Screenshot_51](https://user-images.githubusercontent.com/46135898/68156685-1aa4bc80-ff6e-11e9-850c-0e50f7e94186.png)
<br><br><br>
![Screenshot_52](https://user-images.githubusercontent.com/46135898/68156689-1bd5e980-ff6e-11e9-8667-c759e3f2721e.png)
<br><br><br>

### 5- Optimization:
After data preparation or manipulation we'll code the solution of given problem.
<br><br><br>
![Screenshot_53](https://user-images.githubusercontent.com/46135898/68156692-1c6e8000-ff6e-11e9-9a79-21dc2babfc44.png)
<br><br><br>
![Screenshot_54](https://user-images.githubusercontent.com/46135898/68156695-1d9fad00-ff6e-11e9-8ae8-cb4f42d2aa7a.png)
<br><br><br>
![Screenshot_55](https://user-images.githubusercontent.com/46135898/68156697-1ed0da00-ff6e-11e9-9719-04e5c23108a9.png)
<br><br><br>
![Screenshot_56](https://user-images.githubusercontent.com/46135898/68156699-1f697080-ff6e-11e9-8a99-4cb27b2204ec.png)
<br><br><br>
### 6-  Visualizing Distances Using Folium Map:

After finding the distances from each area to other area, we'll visualize them on folium map.

<br><br><br>
####                                          Area A (Bellevue)
![Screenshot_57](https://user-images.githubusercontent.com/46135898/68156705-209a9d80-ff6e-11e9-8306-e5902cb4ec83.png)

<br><br><br>
####                                          Area A (Bellevue) with marker
![Screenshot_58](https://user-images.githubusercontent.com/46135898/68156712-22646100-ff6e-11e9-88a3-035305160fb2.png)

<br><br><br>
####                                          Distance from Area A to B (Bellevue to Snohomish Country)
![Screenshot_59](https://user-images.githubusercontent.com/46135898/68156715-23958e00-ff6e-11e9-8452-36be81874902.png)

<br><br><br>
####                                          Distance from Area A to C (Bellevue to Montalbano Elicona)
![Screenshot_60](https://user-images.githubusercontent.com/46135898/68156719-24c6bb00-ff6e-11e9-8b6b-f350dc20dab0.png)

<br><br><br>
####                                          Distance from Area A to D (Bellevue to Wenatchee)
![Screenshot_61](https://user-images.githubusercontent.com/46135898/68156727-25f7e800-ff6e-11e9-9bc6-46c6b03a8315.png)

<br><br><br>
####                                          Distance from Area A to E (Bellevue to ძველი თბილისის რაიონი, თბილისი)
![Screenshot_62](https://user-images.githubusercontent.com/46135898/68156728-26907e80-ff6e-11e9-8eef-f642f7840676.png)

<br><br><br>
