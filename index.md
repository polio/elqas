---
layout: index
---

## Overview and Background

This website contains all the information you will need to implement Electronic Lot Quality Assurance Sampling (eLQAS) on mobile devices. eLQAS was developed by the [Bill and Melinda Gates Foundation](http://www.gatesfoundation.org/What-We-Do/Global-Development/Polio) and [Nafundi](http://nafundi.com/) to improve the way we measure polio campaign coverage. 

You can read more about eLQAS and the pilot project in South Sudan on [Nafundi's blog](http://nafundi.com/blog/posts/elqas-collecting-real-time-polio-vaccination-data-with-odk/).

### LQAS

Lot Quality Assurance Sampling (LQAS) is a rapid survey method to assess the quality of vaccination coverage following supplementary immunization activities in pre-defined areas such as a health district (lots) using a small sample size.

For more information about LQAS, read the WHO's [LQAS field manual](http://polioeradication.org/portals/0/document/research/opvdelivery/lqas.pdf).

### eLQAS

eLQAS is an electronic version of LQAS that uses phones and tablets to improve LQAS on paper. eLQAS enables real time results, increased data quality, improved accountability, easier implementation, and support for multiple languages. 

* **Real time results**. If internet connectivity is available, data collected in eLQAS can be instantly sent over cellular or WiFi networks to supervisors. If internet connectivity is not available, it will store the data locally on the device until connectivity is available, at which point it can be sent the data out to supervisors.

* **Increased data quality**. eLQAS has built-in checks that constraints inputs and standardizes responses for easier analysis.

* **Improved accountability**. Each eLQAS submission comes with GPS coordinates of each house and start/end times of each form to ensure proper coverage and accountability.

* **Easier implementation**. eLQAS walks surveyor through questions, automates analysis calculations, and reduces paper work and training.

* **Multiple languages**. eLQAS comes translated in English and French, but can be translated to multiple languages by editing the form in Excel.


### Open Data Kit

eLQAS is implemented as a form within [Open Data Kit](http://opendatakit.org) (ODK) platform. ODK is a free and open-source set of tools which replace paper forms and surveys with phones and tablets. It's great for field staff who need to collect data accurately, quickly, off-line and at scale. 

ODK is safe, secure, and easy to use. It has been used by tens of thousands of organizations (e.g., WHO, WFP, USAID, CDC, Red Cross) to collect millions of forms. ODK provides an out-of-the-box solution to:

1. Build a data collection form or survey
2. Collect the data on a mobile device and send it to a server
3. Aggregate the collected data on a server and extract it in useful formats

Be sure to watch ODK's [overview video](http://youtube.com/watch?v=HqqUdfz9Uyc), read [usage directions](http://opendatakit.org/use) and review [help resources](http://opendatakit.org/help) for more information.


## Implementation Guide

In order to implement eLQAS you will need implementors, Android devices, an ODK aggregate server, and the eLQAS collection form and analysis tool.

eLQAS can be treated as a standard ODK deployment, but following these steps will help ensure a successful and high-quality survey. 

1. **Plan for LQAS**

	a. Read the [LQAS field manual](http://polioeradication.org/portals/0/document/research/opvdelivery/lqas.pdf)

	b. Identify the lots and clusters to be surveyed using the methodology described in the manual. 

	c. Plan for training of the surveyors and survey logistics as you normally would for the paper form.

2. **Prepare electronic form**

	a. Download the [eLQAS Collection Form](assets/elqas_form.xlsx).

    b. Update the form with provinces/clusters/districts specific to the region of interest. This is done by changing the *External Choices* tab in the form.

    c. Convert the Excel form to XML format, which can be read by ODK using the online tool [XLSForm](http://xlsform.opendatakit.org) (requires Internet connection) or [XLSForm Offline ](http://nafundi.com/products).

3. **Setup server**

    a. The easiest option is to [contact Nafundi](http://nafundi.com/contact), who can quickly set up a private server on a cloud service. You as the implementer will control who has access to the server.

    b. Alternately, follow step-by-step instructions on [installing ODK Aggregate](http://opendatakit.org/use/aggregate) to set up an ODK Aggregate server. 

4. **Configure devices**

    a. Any Android device (phone or tablet) will work, but newer devices running Android 4 or later are recommended. We recommend distributing one device per survey team. Additional devices may be useful for training.

    b. Where possible, configure each device with data package on a local cellular or Wi-Fi network. This is required for real-time data collection.

    c. Download the free application ODK Collect from the [Google Play](https://play.google.com/store/apps/details?id=org.odk.collect.android&hl=en) store (requires Internet connection on device) or install it through a USB cable after downloading it from the [ODK Downloads](https://opendatakit.org/downloads) page.

    d. Configure ODK Collect to download forms and send data to the Aggregate server from Step 3. 

5. **Train surveyors**

    a. Plan for between two to three days of training on survey methodology, as described in Chapter IV of the LQAS field manual.

    b. Depending on surveyor experience, plan one additional day of training the surveyors on how to use ODK Collect. The ODK community has useful [training guides and strategies](https://opendatakit.org/help/training-guides) you should review. 

    c. We highly recommend survey training in the field with the devices, in an area near the training is taking place, to address any issues with the survey methodology, technical issues with the devices, and to ensure data collected can be viewed and analyzed easily.

6. **Implement eLQAS**

    a. We recommend surveyors be given backup paper copies of the survey, in case of device failure. 

7. **Analyze results**

	a. Download the [eLQAS Analysis Tool](assets/elqas_analysis.xlsx).

    b. The raw data is available on your ODK Aggregate server, but for viewing and analyzing the data, it is easiest to publish the data to [Google Fusion Tables](http://google.com/fusiontable), using the *Outer-Join* link in Published Data.

    c. Use Analysis Tool to classify Lot coverage according to the WHO guidelines. The Analysis Tool relies on the format of the *Outer Join* data from Google Fusion Tables.

    d. Google Fusion Tables also allows you to map the results of the campaign and share underlying data.

## Notes and Tips

### Form design

* Only change the provinces, districts, lots, and clusters. Changing other parts of the form may introduce technical glitches into your campaign.

* Labels vs name Do not use spaces or special characters in names of districts or go over the 32 character limit. Doing so will likely break downstream analysis of resulting data. Using spaces or special characters in labels is fine.

### Training
* Most of the questions and difficulties in the training will be about LQAS in general, rather than how to use the mobile devices. Plan accordingly.

### More help
* [LQAS Field Manual](http://polioeradication.org/portals/0/document/research/opvdelivery/lqas.pdf)
* [ODK Help Resources](http://opendatakit.org/help)
* [eLQAS Experience report from Nafundi](http://nafundi.com/blog/posts/elqas-collecting-real-time-polio-vaccination-data-with-odk)
* [Contact Nafundi](http://nafundi.com/contact)
* [Contact Gates Foundation](mailto:arend.voorman@gatesfoundation.org)




