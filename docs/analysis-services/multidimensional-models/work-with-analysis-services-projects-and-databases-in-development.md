---
title: "Work with Analysis Services Projects and Databases in Development | Microsoft Docs"
ms.custom: ""
ms.date: "03/07/2017"
ms.prod: "sql-non-specified"
ms.prod_service: "analysis-services"
ms.service: ""
ms.component: "multidimensional-models"
ms.reviewer: ""
ms.suite: "sql"
ms.technology: 
  - "analysis-services"
  - "analysis-services/multidimensional-tabular"
  - "analysis-services/data-mining"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "Analysis Services, projects"
ms.assetid: 39cf9166-fa92-40fe-9962-210a52461257
caps.latest.revision: 16
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
ms.workload: "Inactive"
---
# Work with Analysis Services Projects and Databases in Development
  You can develop an [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] database by using [!INCLUDE[ssBIDevStudioFull](../../includes/ssbidevstudiofull-md.md)] in either project mode or online mode.  
  
## Single Developer  
 When only a single developer is developing the entire [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] database and all of its constituent objects, the developer can use [!INCLUDE[ssBIDevStudioFull](../../includes/ssbidevstudiofull-md.md)] in either project mode or online mode at any time during the lifecycle of the business intelligence solution. In the case of a single developer, the choice of modes is not particularly critical. The maintenance of an offline project file integrated with a source control system has many benefits, such as archiving and rollback. However, with a single developer you will not have the problem of communicating changes with another developer.  
  
## Multiple Developers  
 When multiple developers are working on a business intelligence solution, problems will arise if the developers do not work in project mode with source control under most, if not all circumstances. Source control ensures that two developers are not making changes to the same object at the same time.  
  
 For example, suppose a developer is working in project mode and making changes to selected objects. While the developer is making these changes, suppose that another developer makes a change to the deployed database in online mode. A problem will arise when the first developer attempts to deploy his or her modified [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] project. Namely, [!INCLUDE[ssBIDevStudioFull](../../includes/ssbidevstudiofull-md.md)] will detect that objects have changed within the deployed database and prompt the developer to overwrite the entire database, overwriting the changes of the second developer. Since [!INCLUDE[ssBIDevStudioFull](../../includes/ssbidevstudiofull-md.md)] has no means of resolving the changes between the [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] database instance and the objects in the project about to be overwritten, the only real choice the first developer has is to discard all of his or her changes and starting anew from a new project based on the current version of the [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] database.  
  
  
