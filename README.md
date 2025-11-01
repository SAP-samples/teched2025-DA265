# DA254 - Discover AI in SAP Business Data Cloud with Joule

## Description

This repository contains the material for the SAP TechEd 2025 session called DA254 - Discover AI in SAP Business Data Cloud with Joule.  

## Overview

Join us for an engaging workshop designed to empower your users by unlocking the full potential of AI and natural language processing. Discover how to extract valuable analytical insights from your data models, whether stored in SAP Analytics Cloud or SAP Business Data Cloud. Your users can seamlessly access information—either as casual consumers through Joule in standalone applications or integrated directly within SAP Analytics Cloud.

Experience Joule in action outside of SAP Analytics Cloud, within SAP Workzone, to see how effortlessly it delivers powerful analytics. Learn how Just Ask, the intelligent engine behind Joule, drives this innovative experience.

After exploring Just Ask, you'll be guided through enhancing your underlying data model and refining the Just Ask setup. This will optimise both the user experience and adoption of Joule and Just Ask, making insight discovery simpler and more efficient than ever.

Throughout the workshop, you'll gain best practices and valuable insights to maximise your data strategy.

Cap it all off by leveraging one of the many AI-assisted features for intelligent commentary support, elevating your analytics capabilities to new heights. support.

## Requirements:

+ A SAP Build environment that includes Joule Studio and SAP Analytics Cloud.
+ SAP Analytics Cloud must be part of a Business Data Cloud Formation, which includes SAP Datasphere, to support a planned ‘tunnel’ connection for Just Ask to index BDC models.
+ User synchronisation is required between SAP Build and SAP Analytics Cloud.
+ SAP Analytics Cloud has enabled AI-assisted features. 
+ Both SAC and SAP Build utilise the same Identity Authentication service.

This workshop does not connect to SAP Datasphere, as the ‘tunnel’ connection between SAP Analytics Cloud and SAP Datasphere is currently in beta and not available at TechEd. Instead, a standard SAP Analytics Cloud acquired model is used. The planned ‘tunnel’ will enable model indexing, like that of acquired models. Lessons learned and best practices are applicable to both current acquired models and the planned future ‘tunnel’ connection, which is also expected to index Business Data Cloud models. 

### Related SAP help guides

+ [SAC AI-assisted feature]( https://help.sap.com/docs/SAP_ANALYTICS_CLOUD/18850a0e13944f53aa8a8b7c094ea29e/8dcc1f1915b241b3a10c8e5b8a76b062.html?version=LATEST&locale=en-US)
+ [Joule Studio](https://help.sap.com/docs/Joule_Studio/45f9d2b8914b4f0ba731570ff9a85313/4444cd1ce4cd471bbe127ea2e4735b40.html?locale=en-US&version=LATEST)
+ [Joule Studio integration with SAP Analytics Cloud](
https://help.sap.com/docs/joule/integrating-joule-with-sap/integration-with-sap-analytics-cloud?locale=en-US&version=LATEST)


## Exercises


- [Exercise 1 - Use case 1: Workzone user](exercises/ex1/)
- [Exercise 2 - Use case 2: Information consumer](exercises/ex2/)
- [Exercise 3 - Use case 3: Explore the data model and find additional insights](exercises/ex3/)
- [Exercise 4 - Enhance the user experience](exercises/ex4/)
- [Exercise 5 - Understanding Indexing](exercises/ex5/)
- [Exercise 6 - Comparing Joule inside and outside SAP Analytics Cloud](exercises/ex6/)
- [Exercise 7 - Revisting Joule](exercises/ex7/)
- [Exercise 8 - AI-Assisted Commenting](exercises/ex8/)

  

## Contributing
Please read the [CONTRIBUTING.md](./CONTRIBUTING.md) to understand the contribution guidelines.

## Code of Conduct
Please read the [SAP Open Source Code of Conduct](https://github.com/SAP-samples/.github/blob/main/CODE_OF_CONDUCT.md).

## How to obtain support

Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

This session is currently scheduled:
- Berlin, Germany - 5th November 2025, 2.30 pm local time

## License
Copyright (c) 2024 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
