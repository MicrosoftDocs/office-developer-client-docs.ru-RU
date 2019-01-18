---
title: Гибридные команды (Справочник по для настольных баз данных Access)
TOCTitle: Hybrid commands
ms:assetid: 55654274-0494-349f-820d-92108284449d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249286(v=office.15)
ms:contentKeyID: 48544929
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7fe3e6d0afbba82cacd5a55c630f1ca41f3e318a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709154"
---
# <a name="hybrid-commands"></a><span data-ttu-id="91d14-102">Гибридные команды</span><span class="sxs-lookup"><span data-stu-id="91d14-102">Hybrid commands</span></span>


<span data-ttu-id="91d14-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="91d14-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="91d14-104">Гибридные команды, частично параметризованные команды.</span><span class="sxs-lookup"><span data-stu-id="91d14-104">Hybrid commands are partially parameterized commands.</span></span> <span data-ttu-id="91d14-105">Пример:</span><span class="sxs-lookup"><span data-stu-id="91d14-105">For example:</span></span>

```vb 
 
SHAPE {select * from plants} 
 APPEND( {select * from customers where country = ?} 
 RELATE PlantCountry TO PARAMETER 0, 
 PlantRegion TO CustomerRegion ) 
```

<span data-ttu-id="91d14-106">Поведение кэширования для гибридных команды — это же, что регулярное параметризованные команды.</span><span class="sxs-lookup"><span data-stu-id="91d14-106">The caching behavior for a hybrid command is the same as that of regular parameterized commands.</span></span>

