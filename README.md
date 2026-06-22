### EX4 Implementation of Cluster and Visitor Segmentation for Navigation patterns
### DATE: 16-05-2026
### AIM: To implement Cluster and Visitor Segmentation for Navigation patterns in Python.
### Description:
<div align= "justify">Cluster visitor segmentation refers to the process of grouping or categorizing visitors to a website, 
  application, or physical location into distinct clusters or segments based on various characteristics or behaviors they exhibit. 
  This segmentation allows businesses or organizations to better understand their audience and tailor their strategies, marketing efforts, 
  or services to meet the specific needs and preferences of each cluster.</div>
  
### Procedure:
1) Read the CSV file: Use pd.read_csv to load the CSV file into a pandas DataFrame.
2) Define Age Groups by creating a dictionary containing age group conditions using Boolean conditions.
3) Segment Visitors by iterating through the dictionary and filter the visitors into respective age groups.
4) Visualize the result using matplotlib.

### Program:
```python
# Visitor segmentation based on characteristics
# read the data
/*WRITE YOUR CODE HERE

# Perform segmentation based on characteristics (e.g., age groups)
/*WRITE YOUR CODE HERE

```
### Output:

### Visualization:
```python
# Visitor segmentation based on characteristics

import pandas as pd

# Read the data
data = pd.read_csv("/content/data.csv")

# Perform segmentation based on characteristics (e.g., age groups)

age_groups = {
    '18-25': (data['Age'] >= 18) & (data['Age'] <= 25),
    '26-35': (data['Age'] >= 26) & (data['Age'] <= 35),
    '36-50': (data['Age'] >= 36) & (data['Age'] <= 50),
    '50+': (data['Age'] > 50)
}

# Segment visitors
segmented_visitors = {}

for group, condition in age_groups.items():
    segmented_visitors[group] = data[condition]

# Display segmented visitors
for group, visitors in segmented_visitors.items():
    print("\nAge Group:", group)
    print(visitors)

```
## Define age group labels and plot a bar chart

```
import matplotlib.pyplot as plt

# Create a list to store counts of visitors in each age group
visitor_counts = []

# Count visitors in each age group
for condition in age_groups.values():
    visitor_counts.append(len(data[condition]))

# Define age group labels and plot a bar chart
age_group_labels = list(age_groups.keys())

plt.figure(figsize=(8, 6))
plt.bar(age_group_labels, visitor_counts, color='skyblue')
plt.xlabel('Age Groups')
plt.ylabel('Number of Visitors')
plt.title('Visitor Distribution Across Age Groups')
plt.show()

```
### Output:
<img width="700" height="547" alt="image" src="https://github.com/user-attachments/assets/0d2c3187-17b6-4f54-beef-033c3a2174f0" />


### Result:
Thus, the Cluster and Visitor Segmentation for Navigation Patterns was implemented successfully in Python.
