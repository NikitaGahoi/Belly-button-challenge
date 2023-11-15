# Belly Button Biodiversity Dashboard

## Overview
This project involves building an interactive dashboard to explore the Belly Button Biodiversity dataset, which catalogs the microbes that colonize human navels. The dashboard will include visualizations such as horizontal bar charts, bubble charts, and a gauge chart to display relevant information.

## Project Components

### 1. Dashboard Features
#### Drop-Down Menu
- Select the Test Subject ID No. from the drop-down menu to toggle visualizations (bar chart, bubble charts).

#### Demographic Info Panel
- Displays demographics information of the chosen test subject.
- Shows each key-value pair from the metadata JSON object.

#### Horizontal Bar Graph
- Generated when a test subject is selected.
- Displays the top 10 OTUs found in that test subject.
  - Values for the bar chart: `sample_values`
  - Labels for the bar chart: `otu_ids`
  - Hovertext for the chart: `otu_labels`

#### Bubble Chart
- Generated when a test subject is selected.
- Displays each sample as a bubble.
  - X values: `otu_ids`
  - Y values: `sample_values`
  - Marker size: `sample_values`
  - Marker colors: `otu_ids`
  - Text values: `otu_labels`

### 2. Implementation Steps

#### Step 1: Read Data
- Use the D3 library to read in `samples.json` from the URL: [https://2u-data-curriculum-team.s3.amazonaws.com/dataviz-classroom/v1.1/14-Interactive-Web-Visualizations/02-Homework/samples.json](https://2u-data-curriculum-team.s3.amazonaws.com/dataviz-classroom/v1.1/14-Interactive-Web-Visualizations/02-Homework/samples.json).

#### Step 2: Bar Chart
- Create a horizontal bar chart with a dropdown menu to display the top 10 OTUs found in the selected individual.
- Use `sample_values` for bar chart values, `otu_ids` for labels, and `otu_labels` for hovertext.

![image](https://github.com/NikitaGahoi/Belly-button-challenge/assets/136101293/cef3f572-5352-42e7-8fdf-e4b387494161)


#### Step 3: Bubble Chart
- Create a bubble chart displaying each sample.
- Use `otu_ids` for x values, `sample_values` for y values, `sample_values` for marker size, `otu_ids` for marker colors, and `otu_labels` for text values.

![image](https://github.com/NikitaGahoi/Belly-button-challenge/assets/136101293/e9ea99a8-4638-4cfe-b367-7075614e0f54)


#### Step 4: Demographic Info Panel
- Display individual's demographic information.
- Show each key-value pair from the metadata JSON object somewhere on the page.

![image](https://github.com/NikitaGahoi/Belly-button-challenge/assets/136101293/60face13-6ec6-4503-9ff6-bc452ec5ef64)


#### Step 5: Update on Selection
- Update all plots when a new sample is selected from the dropdown menu.

#### Step 6: Deployment
- Deploy the app to a free static page hosting service, such as GitHub Pages.

### 4. File Organization and Structure
- **Parent Directory:** Contains three folders and `index.html` file.
  - **Resources Folder:** Contains `samples.json` file.
  - **Assets Folder:** Contains `css` folder with `styles.css` for customization.
  - **Static Folder:** Contains two JavaScript files: `app.js` for dashboard development.

