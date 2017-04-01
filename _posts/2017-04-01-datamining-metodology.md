---
layout: post
section-type: post
title: "Datamining Metodology"
category: tech
tags: ['methodology','datamining']
---

## Introduction:

Currently it is generally used the term DataMining to refer to the entire process of extracion of knowledge from large volumes of data. The two main methodologies established for the realization of projects of Dataming have been: CRISP-DM and SEMMA. Basically both have similar principles, only that SEMMA is directed to the use of the system SAS while CRIS-DM is open to the use of any framework.

In 2000 was published the first model projects of Data Mining as agreed-upon by companies. This model is known as CRISP-DM (CRoss Industry Standard Process for Data Mining), and includes the standard to the enterprise level created by a European consortium.

This methodology proposes the activities that should be carried out on a development data mining where each of these activities are divided in tasks, which indicates the output that it produces and the input it needs.


![image](/img/included/methodology_datamining1.jpg "Datamining Project Flow")

![image](/img/included/methodology_datamining2.jpg "Datamining Project Phases")


## Methodologies of software development:

There are two approaches metodologicos at the time of developing the software, the Methodology and Traditional of the Methodology Agile:

#### Methodology Traditional:

It is which defines a set of actions, tasks, principles, and work products required to develop a software with good quality. This methology is guided by a strong planning in the development process, where it performs an intense phase of analysis and design before the construction of the system. They are Prescriptive methodologies.

#### Methodology Agile:

Methodology with a incremental software development (deliveries small software cycles faster), cooperative (customer and developer are in constant communication), straightforward (the method itself is easy to implement, well documented) and adaptive (allows you to make changes last minute). They are especially useful for projects with volatile requirements. They are Descriptive methodologies.

**Some methodologies agile measure the size of the project in ideal days (SCRUM), while others, like for example, story point (Extreme Programming) are according to subjective units of  complexity.**

#### The DataMining projects:

They are closer than the agile methodologies of software development although the generation of documentation and the previous design have a certain importance, without abandoning its simplicity. Your requirements are volatile or non-existent. The business objectives are defined at the beginning and keep invariable while the targets of Datamining projects are specified during the development phase.


## Adaptation of Software engineering models to DataMining:

It is interesting to perform a adapticion of a methodology agile of software engineering to DataMining to cover the deficiencies that exist in the current standard CRISP-DM in terms of the shortage of management processes, organization and the quality of the project. Furthermore, it would be an agile methodology for DataMining projects.


## Phases of the methodology CRISP-DM:

#### Phase I. Business Understanding. Definition of customer needs (understanding the business)

This initial phase focuses on understanding the project objectives. Then it becomes this knowledge of the data in the definition of a problem of data mining and a preliminary plan designed to achieve the objectives.

#### Phase II. Data Understanding. Study and understanding of the data

The understanding phase of data begins with the collection of initial data and continues with activities that allow you to become familiar with the data, identify quality problems, to discover the preliminary knowledge about the data, and/or discover subsets interesting to form hypotheses regarding hidden information.

#### Phase III. Data Preparation. Analysis of the data and feature selection

The phase of data preparation covers all activities necessary to construct the final dataset (data that will be used in the modeling tools) from the raw data initial. The tasks include the selection of tables, records and attributes, as well as transformation and cleaning of data for the tools that shape.

#### Phase IV. Modeling

In this phase, you select and apply the techniques of modeling that are relevant to the problem (the more, the better), and calibrate its parameters to optimal values. Typically there are several techniques for the same type of problem of data mining. Some techniques have specific requirements on the form of the data. Therefore, it is almost always in any project is just getting to the phase of data preparation.

#### Phase V. Evaluation. Assessment (getting results)

At this stage in the project, it have been built one or more models to get a sufficient quality from the perspective of data analysis.
Before proceeding to the final rollout of the model, it is important to evaluate it thoroughly and review the steps executed to create it, to compare the model obtained with the business objectives. A target key is to determine if there are any important matter of business that has not been considered sufficiently. At the end of this phase, you should get a decision on the application of the results of the process of data analysis.

#### Phase VI. Deployment (start production)

Generally, the creation of the model is not the end of the project. Even if the aim of the model is to increase knowledge of the data, the gained knowledge will need to be organized and presented so that the client can use it. Depending on the requirements, the development phase can be as simple as generating a report or as complex as conducting regular and perhaps an automated process of data analysis in the organization.



### References:
- [Un enfoque agil para desarrollos de proyectos DataMining](https://www.researchgate.net/profile/Gonzalo_Mariscal/publication/233425653_AgileDataMining/links/0912f50a9134958879000000.pdf){:target="_blank"}  
- [CRISP-DM: la metodologia para poner orden en los proyectoss de Data Science](https://data.sngular.team/es/art/25/crisp-dm-la-metodologia-para-poner-orden-en-los-proyectos-de-data-science){:target="_blank"} 
- [Metodologias para la realizacion de proyectos de Data Mining](http://www.aeipro.com/files/congresos/2003pamplona/ciip03_0257_0265.2134.pdf){:target="_blank"} 
- [Metodologia de aplicacion de DM](https://www.academia.edu/6665732/CAPITULO_IV_METODOLOGIA_DE_APLICACI%C3%93N_DEL_DATA_MINING_DM){:target="_blank"} 
- [Metodologia de proyectos de Data Mining](https://jpgarcia.cl/2008/07/25/metodologia-para-proyectos-de-mineria-de-datos/){:target="_blank"}
