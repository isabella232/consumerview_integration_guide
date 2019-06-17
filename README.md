# Aperture Data Studio Consumer View Integration
Written By Ashley Laing

## Overview

Experian Data Quality is now introducing enrichment into Aperture Data Studio.
Experian Marketing Services and EDQ have collaborated to integrate Consumer View Data into Aperture Data Studio.

## Installation prerequisites
Before starting, it's important to make sure you have access to the following
things:

* Aperture Data Studio
* The .jar file for the step
* Administrator access to the Glossary

## Installation instructions

For the purposes of this tutorial we will assume you have already installed and logged into Aperture Data Studio.

### Step 1
You will need the jar file for the Consumer View Add-on Step. Download the jar that is given to you by EDQ, and drop it into C:\Program Files\Experian\Aperture Data Studio 1.3.0\addons (the folder name Aperture Data Studio 1.3.0 should end in the version of Aperture Data Studio you are using).

### Step 2
Restart the service by clicking on the user name in the top-right corner and select "Restart service."

![Aperture - Restart Service](media/cv-restartService.PNG)

### Step 3
Once the service is running again, you will need to add the license key into the glossary.
After you’re logged in to Aperture Data Studio, on the home screen click on the Glossary.

![Aperture - Glossary](media/cv-glossary.PNG)

Once in the Glossary click on Constants.

![Aperture - Selecting Constant](media/cv-constant.PNG)

Create a new Constant Library and give it a name (ie ConsumerView).

![Aperture - Constant Library](media/cv-constantLib.PNG)

Create a Business Constant.

![Aperture - Business Constant](media/cv-businessConstant.PNG)

You will name the Business Constant EDQ_TOKEN, and the value will be the license key you got during the onboarding process from EDQ.

![Aperture - Glossary Values](media/glossaryCV.PNG)

## Using The Consumer View Add-on Step

### Step 1
When using the Consumer View Step, you must have your table data tagged.
Instructions on how to data tag your tables is located in the [Aperture Data Studio User Guide](https://www.edq.com/documentation/aperture-data-studio/user-guide/#data-tagging).

Once you tagged the table, the header should look like this header with word bubbles in the tagged headers:

![Aperture - Table Tagged](media/cv-taggedHeader.PNG)

### Step 2
After data tagging the table, create your workflow in the Workflow Designer.

![Aperture - Workflow Designer](media/cv-glossary.PNG)

![Aperture - Create Workflow](media/cv-createWF.PNG)

### Step 3
Select your table and put together your workflow to meet your needs.
The Consumer View step is called "Custom - Consumer View", it will be in the sidebar to the left.

![Aperture - Selecting Table](media/screen3.PNG)

![Aperture - Setting Workflow](media/screen5.PNG)

### Step 4
For the Consumer View Step, you will see 8 predefined Bundles; you will only be able to use the purchased bundles. Select as many purchased bundles as you may.

![Aperture - Setting Workflow](media/cv-bundles.PNG)

### Step 5
If the Record Completion feature was purchased, you also have the ability to have two completion options: Name Completion and Address Completion.

![Aperture - Setting Workflow](media/cv-completion.PNG)

### Step 6
Once you have finished configuring your workflow, you can click on "Show data" to see the results.

## Troubleshooting

1. Leading Zero Missing

Data Studio will sometimes remove leading zeros for standardization. It is important to avoid this on the zip code/postal code column, as the API relies on a full zip code to make a match. To maintain leading zeros, go to Data Explorer and right click on the file. In the drop down menu, select "Preview and configure". Right click on the zip code/postal code column and select "Edit." In the pop up window, turn off all standardization options for that column by toggling each switch into the "Off" position.

## FAQs

1. What columns to tag?

The more columns you tag the better the result will be. However, you must you at least these Data Tags: Forename, Surname, Zip Code/Postal Code, and Country.

2. Why do I only get data back for US records?

This Integration only works for USA data.