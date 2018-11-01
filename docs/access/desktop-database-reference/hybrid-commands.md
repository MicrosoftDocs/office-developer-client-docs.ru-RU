---
title: Гибридные команды (Справочник по для настольных баз данных Access)
TOCTitle: Hybrid Commands
ms:assetid: 55654274-0494-349f-820d-92108284449d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249286(v=office.15)
ms:contentKeyID: 48544929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 363f305fee12cb2e46ab9d4c628030f7dc4bcd78
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873854"
---
# <a name="hybrid-commands"></a><span data-ttu-id="2abb9-102">Гибридные команды</span><span class="sxs-lookup"><span data-stu-id="2abb9-102">Hybrid Commands</span></span>


<span data-ttu-id="2abb9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2abb9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2abb9-104">Гибридные команды, частично параметризованные команды.</span><span class="sxs-lookup"><span data-stu-id="2abb9-104">Hybrid commands are partially parameterized commands.</span></span> <span data-ttu-id="2abb9-105">Пример:</span><span class="sxs-lookup"><span data-stu-id="2abb9-105">For example:</span></span>

```vb 
 
SHAPE {select * from plants} 
 APPEND( {select * from customers where country = ?} 
 RELATE PlantCountry TO PARAMETER 0, 
 PlantRegion TO CustomerRegion ) 
```

<span data-ttu-id="2abb9-106">Поведение кэширования для гибридных команды — это же, что регулярное параметризованные команды.</span><span class="sxs-lookup"><span data-stu-id="2abb9-106">The caching behavior for a hybrid command is the same as that of regular parameterized commands.</span></span>

