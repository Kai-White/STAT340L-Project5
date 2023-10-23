# STAT340L-Project5
Provide a python code that illustrates each of the following cases: (1) Data Interpretation, (2) Data
Categorization, (3) Data Representation , (4) Emphasis and Hierarchy, (5) User Engagement, (6) Color
Scales, (7) Contrast, (8) Color Symbolism, and (9) Consistency

import matplotlib.pyplot as plt

# Sample data
categories = ["Tigers", "Royals", "White Sox"]
values = [661, 676, 641]

# Define different colors for each category
category_colors = ['Navy', 'LightBlue', 'Black']

# Case 1: Data Interpretation - Using color to highlight specific data points
plt.figure(figsize=(24, 12))

# Plot a bar chart with color to emphasize Category B
plt.subplot(331)
plt.bar(categories, values, color=[category_colors[2], category_colors[1], category_colors[2]])
plt.title("MLB Teams Runs Scored")
plt.xlabel("Teams")
plt.ylabel("Runs")

# Case 2: Data Categorization - Using color to differentiate categories
plt.subplot(332)

# Plot a pie chart with different colors for each category
plt.pie(values, labels=categories, colors=category_colors, autopct='%1.1f%%')
plt.title("Runs Scored Between the Teams")

# Case 3: Data Representation - Using color to represent data values
plt.subplot(333)

# Plot a heatmap with color representing values
heatmap_data = [[10, 20, 30], [40, 50, 60], [70, 80, 90]]
plt.imshow(heatmap_data, cmap='rainbow')
plt.colorbar()
plt.title("Sample Heatmap")

# Case 4: Emphasis and Hierarchy - Using color to emphasize specific elements
plt.subplot(334)

# Plot a bar chart with emphasis on Category C
colors = ['Gray', 'Gray', category_colors[2]]
plt.bar(categories, values, color=colors)
plt.title("Emphasis and Hierarchy")

# Case 5: User Engagement - Using color for visual appeal
plt.subplot(335)

# Plot a scatter plot with various colors for engagement
x = [4.08, 4.17, 3.96, 3.61, 4.09]
y = [4.57, 5.3, 5.19, 5.7, 4.3]
colors = ["Navy", "LightBlue", "Black", "Green", "Red"]
plt.scatter(x, y, c=colors, s=100)
plt.title("Runs Scored to Runs Allowed Per Game")

# Case 6: Color Scales - Using a color scale for continuous data
plt.subplot(336)

import numpy as np
x = [1,2,3,4,5]
y = [1,2,3,4,5]
values = [1,2,3,4,5]

colormap = plt.cm.RdYlBu
norm = plt.Normalize(min(values),max(values))

colors = colormap(norm(values))

plt.scatter(x,y,c=colors,s=100,cmap = colormap, marker= 'o')

cbar = plt.colorbar()
cbar.set_label('Values')

plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Scatterplot with Color Scale')
plt.show()
# Case 7: Contrast - Using high contrast for readability
categories = ['McDonalds','Burger King','Taco Bell']
values = [6,7,4]


# Plot a bar chart with high-contrast colors
colors = ["#FFFF11", "#000000", "#FF0000"]
plt.bar(categories, values, color=colors)
plt.title("Contrast")
plt.show()

# Case 8: Color Symbolism - Using colors with specific symbolism

# Plot a bar chart with colors symbolizing emotions (e.g., red for anger)
colors = ["#FF5733", "#FFFF00", "#3366FF"]
plt.bar(categories, values, color=colors)
plt.title("Color Symbolism")
plt.show()
# Case 9: Consistency - Using consistent colors throughout a visualization


# Plot a line chart with consistent colors
x = [0,1,2,3,4,5]
y1 = [0,0,2,1,7,6]
y2 = [0,0,0,4,9,1]
y3 = [0,3,3,4,6,3]

colors = ["#FF5733", "#33FF57", "#3366FF"]
plt.plot(x,y1, label = 'Tigers', color = "#FF5733")
plt.plot(x,y2, label = 'Royals', color = "#33FF57")
plt.plot(x,y3, label = 'White-Sox', color = "#3366FF")
plt.title("Consistency")

plt.tight_layout()
plt.show()



![image](https://github.com/Kai-White/STAT340L-Project5/assets/148802394/0f48f62d-d9df-4499-8353-b98cd7bd80d3)
![image](https://github.com/Kai-White/STAT340L-Project5/assets/148802394/258aef08-97c1-409e-90a1-f9dddaabec9c)
![image](https://github.com/Kai-White/STAT340L-Project5/assets/148802394/46d8eec5-8d35-41c9-89a9-a45e906790a1)
![image](https://github.com/Kai-White/STAT340L-Project5/assets/148802394/b1fbc3e2-9851-4fe0-8529-8531a675a1a4)
