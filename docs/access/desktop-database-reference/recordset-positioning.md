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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718538"
---
# <a name="recordset-positioning"></a><span data-ttu-id="ecd07-102">Размещение наборов записей</span><span class="sxs-lookup"><span data-stu-id="ecd07-102">Recordset positioning</span></span>

<span data-ttu-id="ecd07-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ecd07-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ecd07-104">Используйте свойство **AbsolutePosition** для перемещения к записи на основании его порядковый номер в объекте **набора записей** или для определения порядковый номер текущей записи.</span><span class="sxs-lookup"><span data-stu-id="ecd07-104">Use the **AbsolutePosition** property to move to a record, based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record.</span></span> <span data-ttu-id="ecd07-105">Поставщик должен поддерживать соответствующие функциональные возможности для этого свойства, чтобы оно было доступно.</span><span class="sxs-lookup"><span data-stu-id="ecd07-105">The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="ecd07-106">**AbsolutePosition** на основе 1 и имеет значение 1, если текущая запись является первой записи в **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="ecd07-106">**AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**.</span></span> <span data-ttu-id="ecd07-107">Как уже было сказано ранее, можно получить общее число записей в объекте **набора записей** из свойства **RecordCount** .</span><span class="sxs-lookup"><span data-stu-id="ecd07-107">As mentioned previously, you can obtain the total number of records in the **Recordset** object from the **RecordCount** property.</span></span>

<span data-ttu-id="ecd07-108">Если задать свойство **AbsolutePosition** даже в том случае, если это записи в текущей кэш-памяти, ADO перезагружает кэша с новой группы записей, начиная с указанной записи.</span><span class="sxs-lookup"><span data-stu-id="ecd07-108">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record you specified.</span></span> <span data-ttu-id="ecd07-109">Свойство **CacheSize** определяет размер этой группы.</span><span class="sxs-lookup"><span data-stu-id="ecd07-109">The **CacheSize** property determines the size of this group.</span></span>

> [!NOTE]
> <span data-ttu-id="ecd07-110">Не следует использовать свойство **AbsolutePosition** как номер заменяющего записи.</span><span class="sxs-lookup"><span data-stu-id="ecd07-110">You should not use the **AbsolutePosition** property as a surrogate record number.</span></span> <span data-ttu-id="ecd07-111">Положение данной записи изменений при удалении предыдущей записи.</span><span class="sxs-lookup"><span data-stu-id="ecd07-111">The position of a given record changes when you delete a preceding record.</span></span> <span data-ttu-id="ecd07-112">Кроме того, не Software assurance, что данной записи будут иметь же **AbsolutePosition** , если опросить или повторном открытии в объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="ecd07-112">There also is no assurance that a given record will have the same **AbsolutePosition** if the **Recordset** object is requeried or reopened.</span></span> <span data-ttu-id="ecd07-113">Закладки являются рекомендуемый способ сохранения и возврата в заданной позиции и являются единственным способом размещения для всех типов объектов **наборов записей** .</span><span class="sxs-lookup"><span data-stu-id="ecd07-113">Bookmarks are the recommended way of retaining and returning to a given position and are the only way of positioning across all types of **Recordset** objects.</span></span>


