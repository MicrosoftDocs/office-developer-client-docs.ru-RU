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
# <a name="persisting-filtered-and-hierarchical-recordsets"></a><span data-ttu-id="b38e7-102">Сохранение отфильтрованных и иерархических наборов записей</span><span class="sxs-lookup"><span data-stu-id="b38e7-102">Persisting filtered and hierarchical Recordsets</span></span>


<span data-ttu-id="b38e7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b38e7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b38e7-104">Если свойство [Filter](filter-property-ado.md) применяется для объекта **Recordset**, сохраняются только те строки, которые доступны в фильтре.</span><span class="sxs-lookup"><span data-stu-id="b38e7-104">If the [Filter](filter-property-ado.md) property is in effect for the **Recordset**, only the rows accessible under the filter are saved.</span></span> <span data-ttu-id="b38e7-105">Если объект **Recordset** является иерархический, сохраняются текущий доЧерний **набор записей** и его дочерние элементы, в том числе родительский **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="b38e7-105">If the **Recordset** is hierarchical, the current child **Recordset** and its children are saved, including the parent **Recordset**.</span></span> <span data-ttu-id="b38e7-106">При вызове метода **Save** дочернего объекта **Recordset** , дочерний объект и все его дочерние элементы сохраняются, а родитель — нет.</span><span class="sxs-lookup"><span data-stu-id="b38e7-106">If the **Save** method of a child **Recordset** is called, the child and all its children are saved, but the parent is not.</span></span> <span data-ttu-id="b38e7-107">Дополнительные сведения о иерархических **наборАх записей**приведены в [главе 9: формирование данных](chapter-9-data-shaping.md).</span><span class="sxs-lookup"><span data-stu-id="b38e7-107">For more information about hierarchical **Recordsets**, see [Chapter 9: Data Shaping](chapter-9-data-shaping.md).</span></span>


> [!NOTE]
> <span data-ttu-id="b38e7-108">При сохранении иерархических **наборов записей** (форм данных) в формате XML применяются некоторые ограничения.</span><span class="sxs-lookup"><span data-stu-id="b38e7-108">Some limitations apply when saving hierarchical **Recordsets** (data shapes) in XML format.</span></span> <span data-ttu-id="b38e7-109">Более подробную информацию можно узнать [в статье иерархиЧеские наборы записей в XML](hierarchical-recordsets-in-xml.md).</span><span class="sxs-lookup"><span data-stu-id="b38e7-109">For more information, see [Hierarchical Recordsets in XML](hierarchical-recordsets-in-xml.md).</span></span>


