---
title: Гибридные команды (Справочник по для настольных баз данных Access)
TOCTitle: Hybrid Commands
ms:assetid: 55654274-0494-349f-820d-92108284449d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249286(v=office.15)
ms:contentKeyID: 48544929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aa95956fb50a5cd15fa4415e65d4a701f2e48feb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481510"
---
# <a name="hybrid-commands"></a><span data-ttu-id="e4fe6-102">Hybrid Commands</span><span class="sxs-lookup"><span data-stu-id="e4fe6-102">Hybrid Commands</span></span>


<span data-ttu-id="e4fe6-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e4fe6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e4fe6-104">Гибридные команды, частично параметризованные команды.</span><span class="sxs-lookup"><span data-stu-id="e4fe6-104">Hybrid commands are partially parameterized commands.</span></span> <span data-ttu-id="e4fe6-105">Пример:</span><span class="sxs-lookup"><span data-stu-id="e4fe6-105">For example:</span></span>

```vb 
 
SHAPE {select * from plants} 
 APPEND( {select * from customers where country = ?} 
 RELATE PlantCountry TO PARAMETER 0, 
 PlantRegion TO CustomerRegion ) 
```

<span data-ttu-id="e4fe6-106">Поведение кэширования для гибридных команды — это же, что регулярное параметризованные команды.</span><span class="sxs-lookup"><span data-stu-id="e4fe6-106">The caching behavior for a hybrid command is the same as that of regular parameterized commands.</span></span>

