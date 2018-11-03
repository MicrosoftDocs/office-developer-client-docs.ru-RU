---
title: Гибридные команды (Справочник по для настольных баз данных Access)
TOCTitle: Hybrid commands
ms:assetid: 55654274-0494-349f-820d-92108284449d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249286(v=office.15)
ms:contentKeyID: 48544929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 046d005eb4a9e1c8097908e0104b8d1e5c76e2af
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946917"
---
# <a name="hybrid-commands"></a><span data-ttu-id="9e82a-102">Гибридные команд</span><span class="sxs-lookup"><span data-stu-id="9e82a-102">Hybrid commands</span></span>


<span data-ttu-id="9e82a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e82a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9e82a-104">Гибридные команды, частично параметризованные команды.</span><span class="sxs-lookup"><span data-stu-id="9e82a-104">Hybrid commands are partially parameterized commands.</span></span> <span data-ttu-id="9e82a-105">Пример:</span><span class="sxs-lookup"><span data-stu-id="9e82a-105">For example:</span></span>

```vb 
 
SHAPE {select * from plants} 
 APPEND( {select * from customers where country = ?} 
 RELATE PlantCountry TO PARAMETER 0, 
 PlantRegion TO CustomerRegion ) 
```

<span data-ttu-id="9e82a-106">Поведение кэширования для гибридных команды — это же, что регулярное параметризованные команды.</span><span class="sxs-lookup"><span data-stu-id="9e82a-106">The caching behavior for a hybrid command is the same as that of regular parameterized commands.</span></span>

