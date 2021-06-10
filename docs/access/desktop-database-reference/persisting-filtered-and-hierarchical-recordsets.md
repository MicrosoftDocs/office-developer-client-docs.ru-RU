---
title: Сохранение отфильтрованных и иерархических наборов записей
TOCTitle: Persisting filtered and hierarchical Recordsets
ms:assetid: 3648a997-dac7-d8a3-3cca-a6827f26a4f0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249120(v=office.15)
ms:contentKeyID: 48544162
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1332d4348c993f94d8b2ee61280b8b35c02324c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287589"
---
# <a name="persisting-filtered-and-hierarchical-recordsets"></a><span data-ttu-id="303e6-102">Сохранение отфильтрованных и иерархических наборов записей</span><span class="sxs-lookup"><span data-stu-id="303e6-102">Persisting filtered and hierarchical Recordsets</span></span>


<span data-ttu-id="303e6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="303e6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="303e6-104">Если свойство [Filter](filter-property-ado.md) действует для **recordset,** сохраняются только строки, доступные под фильтром.</span><span class="sxs-lookup"><span data-stu-id="303e6-104">If the [Filter](filter-property-ado.md) property is in effect for the **Recordset**, only the rows accessible under the filter are saved.</span></span> <span data-ttu-id="303e6-105">Если набор **записей** иерархичен, текущий **набор** записей ребенка и его дети сохраняются, в том числе родительский **набор записей.**</span><span class="sxs-lookup"><span data-stu-id="303e6-105">If the **Recordset** is hierarchical, the current child **Recordset** and its children are saved, including the parent **Recordset**.</span></span> <span data-ttu-id="303e6-106">Если называется **метод** Сохранить  набор записей для ребенка, ребенок и все его дети сохраняются, но родитель — нет.</span><span class="sxs-lookup"><span data-stu-id="303e6-106">If the **Save** method of a child **Recordset** is called, the child and all its children are saved, but the parent is not.</span></span> <span data-ttu-id="303e6-107">Дополнительные сведения о иерархических **наборов записей** см. в [главе 9: Формирование данных.](chapter-9-data-shaping.md)</span><span class="sxs-lookup"><span data-stu-id="303e6-107">For more information about hierarchical **Recordsets**, see [Chapter 9: Data Shaping](chapter-9-data-shaping.md).</span></span>


> [!NOTE]
> <span data-ttu-id="303e6-108">Некоторые ограничения применяются при сохранении иерархических **наборов** записей (форм данных) в формате XML.</span><span class="sxs-lookup"><span data-stu-id="303e6-108">Some limitations apply when saving hierarchical **Recordsets** (data shapes) in XML format.</span></span> <span data-ttu-id="303e6-109">Дополнительные сведения см. в [таблице Иерархические записи в XML.](hierarchical-recordsets-in-xml.md)</span><span class="sxs-lookup"><span data-stu-id="303e6-109">For more information, see [Hierarchical Recordsets in XML](hierarchical-recordsets-in-xml.md).</span></span>


