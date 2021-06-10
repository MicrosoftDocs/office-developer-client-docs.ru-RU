---
title: Размещение наборов записей
TOCTitle: Recordset positioning
ms:assetid: 1b8b08d5-a11c-ec6e-201c-1405171a1264
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248955(v=office.15)
ms:contentKeyID: 48543546
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cffb5adce1266bd7fdd08989e9f92110f4829ba0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284506"
---
# <a name="recordset-positioning"></a><span data-ttu-id="6c886-102">Размещение наборов записей</span><span class="sxs-lookup"><span data-stu-id="6c886-102">Recordset positioning</span></span>

<span data-ttu-id="6c886-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c886-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6c886-104">Используйте свойство **AbsolutePosition** для перемещения к записи на основе его расположения в объекте **Recordset** или для определения координат текущей записи.</span><span class="sxs-lookup"><span data-stu-id="6c886-104">Use the **AbsolutePosition** property to move to a record, based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record.</span></span> <span data-ttu-id="6c886-105">Поставщик должен поддерживать соответствующие функции, чтобы это свойство было доступно.</span><span class="sxs-lookup"><span data-stu-id="6c886-105">The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="6c886-106">**AbsolutePosition** основан на 1 и равен 1, когда текущая запись является первой записью в **Наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="6c886-106">**AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**.</span></span> <span data-ttu-id="6c886-107">Как упоминалось ранее, общее число записей в объекте **Recordset** можно получить из свойства **RecordCount.**</span><span class="sxs-lookup"><span data-stu-id="6c886-107">As mentioned previously, you can obtain the total number of records in the **Recordset** object from the **RecordCount** property.</span></span>

<span data-ttu-id="6c886-108">При задании свойства **AbsolutePosition,** даже если оно записано в текущем кэше, ADO перезагружает кэш новой группой записей, начиная с указанной записи.</span><span class="sxs-lookup"><span data-stu-id="6c886-108">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record you specified.</span></span> <span data-ttu-id="6c886-109">Свойство **CacheSize** определяет размер этой группы.</span><span class="sxs-lookup"><span data-stu-id="6c886-109">The **CacheSize** property determines the size of this group.</span></span>

> [!NOTE]
> <span data-ttu-id="6c886-110">Свойство **AbsolutePosition** не следует использовать в качестве номера записи суррогата.</span><span class="sxs-lookup"><span data-stu-id="6c886-110">You should not use the **AbsolutePosition** property as a surrogate record number.</span></span> <span data-ttu-id="6c886-111">Положение данной записи меняется при удалении предыдущей записи.</span><span class="sxs-lookup"><span data-stu-id="6c886-111">The position of a given record changes when you delete a preceding record.</span></span> <span data-ttu-id="6c886-112">Кроме того, нет уверенности в том, что в случае повторного или повторного открытия объекта **Recordset** у данной записи будет одинаковый **absolutePosition.**</span><span class="sxs-lookup"><span data-stu-id="6c886-112">There also is no assurance that a given record will have the same **AbsolutePosition** if the **Recordset** object is requeried or reopened.</span></span> <span data-ttu-id="6c886-113">Закладки — это рекомендуемый способ сохранения и возвращения в заданную позицию и единственный способ позиционирования во всех типах объектов **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="6c886-113">Bookmarks are the recommended way of retaining and returning to a given position and are the only way of positioning across all types of **Recordset** objects.</span></span>


