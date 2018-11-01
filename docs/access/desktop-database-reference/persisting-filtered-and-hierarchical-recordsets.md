---
title: Сохранение отфильтрованных и иерархических наборов записей
TOCTitle: Persisting Filtered and Hierarchical Recordsets
ms:assetid: 3648a997-dac7-d8a3-3cca-a6827f26a4f0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249120(v=office.15)
ms:contentKeyID: 48544162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 931345aff0cd3d8c9b10c53073e640b3cfdd5de5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889716"
---
# <a name="persisting-filtered-and-hierarchical-recordsets"></a><span data-ttu-id="66b64-102">Сохранение отфильтрованных и иерархических наборов записей</span><span class="sxs-lookup"><span data-stu-id="66b64-102">Persisting Filtered and Hierarchical Recordsets</span></span>


<span data-ttu-id="66b64-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="66b64-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="66b64-104">Если **записей**не свойство [фильтра](filter-property-ado.md) , будут сохранены только строки, доступных в группе фильтр.</span><span class="sxs-lookup"><span data-stu-id="66b64-104">If the [Filter](filter-property-ado.md) property is in effect for the **Recordset**, only the rows accessible under the filter are saved.</span></span> <span data-ttu-id="66b64-105">Если **записей** иерархических, дочерние текущего **набора записей** и его дочерние элементы сохраняются, включая родительского **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="66b64-105">If the **Recordset** is hierarchical, the current child **Recordset** and its children are saved, including the parent **Recordset**.</span></span> <span data-ttu-id="66b64-106">Метод **Save** дочернего вызванный **записей** , дочерних и все его дочерние элементы сохраняются, но родительский не.</span><span class="sxs-lookup"><span data-stu-id="66b64-106">If the **Save** method of a child **Recordset** is called, the child and all its children are saved, but the parent is not.</span></span> <span data-ttu-id="66b64-107">Дополнительные сведения о иерархические **наборы записей**в разделе [Глава 9: формирования данных](chapter-9-data-shaping.md).</span><span class="sxs-lookup"><span data-stu-id="66b64-107">For more information about hierarchical **Recordsets**, see [Chapter 9: Data Shaping](chapter-9-data-shaping.md).</span></span>


> [!NOTE]
> <P><span data-ttu-id="66b64-108">Некоторые ограничения при сохранении иерархические <STRONG>наборы записей</STRONG> (данные фигуры) в формате XML.</span><span class="sxs-lookup"><span data-stu-id="66b64-108">Some limitations apply when saving hierarchical <STRONG>Recordsets</STRONG> (data shapes) in XML format.</span></span> <span data-ttu-id="66b64-109">Для получения дополнительных сведений см <A href="hierarchical-recordsets-in-xml.md">Иерархические наборы записей в формате XML</A>.</span><span class="sxs-lookup"><span data-stu-id="66b64-109">For more information, see <A href="hierarchical-recordsets-in-xml.md">Hierarchical Recordsets in XML</A>.</span></span></P>


