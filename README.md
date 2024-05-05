# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
NAME : kabilan T
REG NO : 212222230059
```
```
import matplotlib.pyplot as plt
x_val = [0,1,2,3,4,5]
y_val = [0,1,4,9,16,25]
plt.plot(x_val,y_val)
plt.show()
```
![Screenshot 2024-04-25 222532](https://github.com/Yamunaasri/EXNO-5-DS/assets/115707860/7ea276da-329c-4e1b-af27-3ccbc2e158e8)
```
import matplotlib.pyplot as plt
x = [1,2,3]
y = [2,4,1]
plt.plot(x,y)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('My first graph')
plt.show()
```
![Screenshot 2024-04-25 222628](https://github.com/Yamunaasri/EXNO-5-DS/assets/115707860/53f92332-e90c-481d-b3db-b3a8b253211b)
```
import matplotlib.pyplot as plt
x1 = [1,2,3]
y1 = [2,5,3]
plt.plot(x1,y1,label = 'line 1')
x2 = [1,2,3]
y2 = [3,1,6]
plt.plot(x2,y2,label = 'line 2')
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title("Two lines on the same graph")
plt.legend()
plt.show()
```
![Screenshot 2024-04-25 222724](https://github.com/Yamunaasri/EXNO-5-DS/assets/115707860/2cc396f0-67ac-4526-9301-1126cb6eb146)
```
import matplotlib.pyplot as plt
import numpy as np
x = [1,2,3,4,5]
y1 = [10,12,14,16,18]
y2 = [5,7,9,11,13]
y3 = [2,4,6,8,10]
plt.fill_between(x,y1,color = 'blue')
plt.fill_between(x,y2,color = 'orange')
```
![Screenshot 2024-04-25 222824](https://github.com/Yamunaasri/EXNO-5-DS/assets/115707860/12d2d32e-2a72-4864-aeec-89af7b2f681d)
```
plt.stackplot(x,y1,y2,y3,labels = ['line1','line2','line3'])
plt.legend(loc = 'upper left')
plt.title('Stacked line charts')
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.show()
```
![Screenshot 2024-04-25 222900](https://github.com/Yamunaasri/EXNO-5-DS/assets/115707860/676db96f-5e9c-4ee4-a139-d42346831da8)

### 5.Spline Chart
```
from scipy.interpolate import make_interp_spline
x=np.array([1,2,3,4,5,6,7,8,9,10])
y=np.array([2,4,5,7,8,8,9,10,11,12])
spl=make_interp_spline(x,y)
x1=np.linspace(x.min(),x.max(),100)
y1=spl(x1)
plt.plot(x,y,'*',label='data')
plt.plot(x1,y1,'-',label="spline")
plt.legend()
plt.show()
```
![5-5](https://github.com/Divya110205/EXNO-5-DS/assets/119404855/052795a4-7ab1-48a3-9e18-16bd30f17142)

### TO VISUALIZE RELATIONSHIPS
### 1.Bar Chart
```
val=[5,6,3,7,2]
names=["A","B","C","D","E"]
plt.bar(names,val,color="blue")
plt.show()
```
![5-6](https://github.com/Divya110205/EXNO-5-DS/assets/119404855/39bbd8d3-a82f-49bd-9c8f-13037dfdb978)

### 2.Scatter Plot
```
x=[0,1,2,3,4,5]
y=[0,1,4,9,16,25]
plt.scatter(x,y,s=30,color="red")
plt.show()
```
![5-7](https://github.com/Divya110205/EXNO-5-DS/assets/119404855/8f67a4bb-03ad-4c64-903c-453ca8760169)

### 3.Bubble Chart
```
x = [1, 2, 3, 4, 5]
y = [10, 15, 20, 25, 30]
sizes = [100, 200, 300, 400, 500]
plt.scatter(x, y, s=sizes, alpha=0.5)
plt.xlabel('x_values')
plt.ylabel('y_values')
plt.title('Bubble Chart')
plt.show()
```
![5-8](https://github.com/Divya110205/EXNO-5-DS/assets/119404855/212820b5-2e8e-4796-83ac-7827b2d94c37)


### TO CAPTURE DISTRIBUTIONS
### 1.Histogram




```
import numpy as np
import matplotlib.pyplot as plt
val = [2,4,7,3]
names = ['A','B','C','D']
plt.bar(names, val,color = 'purple')
plt.show()
```
![Screenshot 2024-04-25 222938](https://github.com/Yamunaasri/EXNO-5-DS/assets/115707860/7d71481a-1aa6-4b57-a5af-95af9b12a4be)
```
import matplotlib.pyplot as plt
import numpy as np
ages = [2,6,4,12,13,12,16,18,18,19,26,24,39,34,45,42,54,56,90,56,86,79]
range = (0,100)
bins = 10
plt.hist(ages,bins,range,color='green',histtype='bar',rwidth=0.8)
plt.xlabel('age')
plt.ylabel('no of people')
plt.title('histogram')
plt.show()
```
![Screenshot 2024-04-25 223015](https://github.com/Yamunaasri/EXNO-5-DS/assets/115707860/5b088d34-b1ee-4b3e-a229-39360d583bf6)


```
val=[5,6,3,7,2]
names=["A","B","C","D","E"]
plt.barh(names,val,color="yellowgreen")
plt.show()
```

<img width="392" alt="image" src="https://github.com/Prakashmathi15/EXNO-5-DS/assets/118350045/9cb9b6a8-745b-4976-a7d0-c2c64b9e9d8b">


```
import matplotlib.pyplot as plt
import numpy as np
np.random.seed(0)
data=np.random.normal(loc=0,scale=1,size=100)
data
```
![Screenshot 2024-04-25 223122](https://github.com/Yamunaasri/EXNO-5-DS/assets/115707860/d66d7f36-ff0d-41de-9fdd-1ebd34f79828)
```
fig,ax=plt.subplots()
ax.boxplot(data)
ax.set_xlabel("data")
ax.set_ylabel("values")
ax.set_title("box plot")
```
![Screenshot 2024-04-25 223203](https://github.com/Yamunaasri/EXNO-5-DS/assets/115707860/4cdf0d14-c240-4e56-9ef1-ed0ac3eef7d2)

### 3.Violin Plot
```
data = [np.random.normal(loc=0, scale=1, size=100),
        np.random.normal(loc=2, scale=1, size=100),
        np.random.normal(loc=1, scale=2, size=100)]
plt.violinplot(data)
plt.xlabel('Groups')
plt.ylabel('Values')
plt.title('Violin Plot')
plt.xticks([1, 2, 3], ['Group 1', 'Group 2', 'Group 3'])
plt.show()
```

![5-11](https://github.com/Divya110205/EXNO-5-DS/assets/119404855/03740c40-7a6e-4d7c-b6c6-1f2905f036d1)

### 4.Density Chart
```
data = np.random.normal(0, 1, 1000)
plt.hist(data, bins=30, density=True, alpha=0.5)
plt.title('Density Plot Example')
plt.xlabel('Values')
plt.ylabel('Density')
from scipy.stats import gaussian_kde
kde = gaussian_kde(data)
x_vals = np.linspace(min(data), max(data), 1000)
plt.plot(x_vals, kde(x_vals), 'r')
plt.show()
```

![5-12](https://github.com/Divya110205/EXNO-5-DS/assets/119404855/2b218374-d635-4ea6-a5d0-5ffec3052560)

```
import matplotlib.pyplot as plt
activities=['eat','sleep','work','play']
slices=[3,7,8,6]
colors=['r','y','g','b']
plt.pie(slices,labels = slices,colors=colors,startangle=90,shadow = True,explode = (0,0,0.1,0),radius=1.2,autopct='%1.1f%%')
plt.legend()
plt.show()
```
![Screenshot 2024-04-25 223241](https://github.com/Yamunaasri/EXNO-5-DS/assets/115707860/ddb35914-91b3-478a-81cf-f76e9cc9c071)

![Screenshot 2024-04-26 222959](https://github.com/RENUGASARAVANAN/EXNO-5-DS/assets/119292258/448d681a-92e7-41a8-8362-91fbbb95eef8)

# Result:
  Thus, We have successfullu performed Data Visualization using matplot python library for the given datas.
