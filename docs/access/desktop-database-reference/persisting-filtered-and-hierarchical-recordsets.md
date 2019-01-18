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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725947"
---
# <a name="persisting-filtered-and-hierarchical-recordsets"></a><span data-ttu-id="869d3-102">Сохранение отфильтрованных и иерархических наборов записей</span><span class="sxs-lookup"><span data-stu-id="869d3-102">Persisting filtered and hierarchical Recordsets</span></span>


<span data-ttu-id="869d3-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="869d3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="869d3-104">Если **записей**не свойство [фильтра](filter-property-ado.md) , будут сохранены только строки, доступных в группе фильтр.</span><span class="sxs-lookup"><span data-stu-id="869d3-104">If the [Filter](filter-property-ado.md) property is in effect for the **Recordset**, only the rows accessible under the filter are saved.</span></span> <span data-ttu-id="869d3-105">Если **записей** иерархических, дочерние текущего **набора записей** и его дочерние элементы сохраняются, включая родительского **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="869d3-105">If the **Recordset** is hierarchical, the current child **Recordset** and its children are saved, including the parent **Recordset**.</span></span> <span data-ttu-id="869d3-106">Метод **Save** дочернего вызванный **записей** , дочерних и все его дочерние элементы сохраняются, но родительский не.</span><span class="sxs-lookup"><span data-stu-id="869d3-106">If the **Save** method of a child **Recordset** is called, the child and all its children are saved, but the parent is not.</span></span> <span data-ttu-id="869d3-107">Дополнительные сведения о иерархические **наборы записей**в разделе [Глава 9: формирования данных](chapter-9-data-shaping.md).</span><span class="sxs-lookup"><span data-stu-id="869d3-107">For more information about hierarchical **Recordsets**, see [Chapter 9: Data Shaping](chapter-9-data-shaping.md).</span></span>


> [!NOTE]
> <span data-ttu-id="869d3-108">Некоторые ограничения при сохранении иерархические **наборы записей** (данные фигуры) в формате XML.</span><span class="sxs-lookup"><span data-stu-id="869d3-108">Some limitations apply when saving hierarchical **Recordsets** (data shapes) in XML format.</span></span> <span data-ttu-id="869d3-109">Для получения дополнительных сведений см [Иерархические наборы записей в формате XML](hierarchical-recordsets-in-xml.md).</span><span class="sxs-lookup"><span data-stu-id="869d3-109">For more information, see [Hierarchical Recordsets in XML](hierarchical-recordsets-in-xml.md).</span></span>


