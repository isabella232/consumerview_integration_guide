# Aperture Data Studio Consumer View Integration
Written By Ashley Laing

## Overview

Experian Data Quality has updated the enrichment step, Consumer View, into Aperture Data Studio 2.0. Experian Marketing Services and EDQ have collaborated to integrate Consumer View Data into Aperture Data Studio.

## Installation prerequisites
Before starting, it's important to make sure you have access to the following
things:

* Aperture Data Studio
* The .jar file for the step

## Installation instructions

For the purposes of this tutorial we will assume you have already installed and logged into Aperture Data Studio.

### Step 1
You will need the jar file for the Consumer View Add-on Step. Download the jar that is given to you by EDQ, and drop it into C:\Program Files\Experian\Aperture Data Studio 2.0.14\addons (the folder name Aperture Data Studio 2.0.14 should end in the version of Aperture Data Studio you are using), if you cannot find it on the C drive look on the drive you had downloaded Aperture Data Studio . Restart the Aperture Data Studio Server service so that the add-on will be added.

### Step 2
Next, you will need to add the license key into the step setting for the Consumer View Step.

## Using The Consumer View Add-on Step

### Step 1


### Step 2


### Step 3


### Step 4


### Step 5


## Troubleshooting


## FAQs

1. What columns to tag?

I would recommend using the following data tags:
    You must use:
        -Name for full name (if name is separated, use Forenames and Surname)
        -Postal Code or Zip Code
    In addition you can use:
        -Email if the column is there (not required though)
        -Address or Premise and Street
        -City
        -State

2. Why do I only get data back for US records?

This Integration only works for USA data.

3. How does ConsumerView Add-on know it is a US record?

The ConsumerView Step uses the Zip code and checks to see if it is a US formatted zipcode.

4. Will the records process if I don't have the data tags?

The table won't generate. It uses the datatags to find the information needed to get back data. 

5. How to check my remaining transactions?

There is a separate step that will allow you to view how many clicks are left.