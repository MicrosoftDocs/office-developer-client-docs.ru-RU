---
title: Свойство Status (Recordset в ADO)
TOCTitle: Status property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4017ff216c17479a69d6d07d0abe51b30fd5e680
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308521"
---
# <a name="status-property-ado-recordset"></a><span data-ttu-id="50d14-102">Свойство Status (Recordset в ADO)</span><span class="sxs-lookup"><span data-stu-id="50d14-102">Status property (ADO Recordset)</span></span>


<span data-ttu-id="50d14-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="50d14-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="50d14-104">Указывает состояние текущей записи в отношении пакетных обновлений или других массовых операций.</span><span class="sxs-lookup"><span data-stu-id="50d14-104">Indicates the status of the current record with respect to batch updates or other bulk operations.</span></span>

## <a name="return-value"></a><span data-ttu-id="50d14-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50d14-105">Return value</span></span>

<span data-ttu-id="50d14-106">Возвращает сумму из одного или более [значений RecordStatusEnum.](recordstatusenum.md)</span><span class="sxs-lookup"><span data-stu-id="50d14-106">Returns a sum of one or more [RecordStatusEnum](recordstatusenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="50d14-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="50d14-107">Remarks</span></span>

<span data-ttu-id="50d14-108">Используйте свойство **Status,** чтобы узнать, какие изменения ожидаются для записей, измененных во время пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="50d14-108">Use the **Status** property to see what changes are pending for records modified during batch updating.</span></span> <span data-ttu-id="50d14-109">Можно также использовать свойство **Status** для просмотра состояния записей, которые не удается получить во время массовых операций, например при вызове методов [Resync,](resync-method-ado.md) [UpdateBatch](updatebatch-method-ado.md)или [CancelBatch](cancelbatch-method-ado.md) в [объекте Recordset,](recordset-object-ado.md) или установить для свойства [Filter](filter-property-ado.md) объекта **Recordset** массив закладок.</span><span class="sxs-lookup"><span data-stu-id="50d14-109">You can also use the **Status** property to view the status of records that fail during bulk operations, such as when you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object, or set the [Filter](filter-property-ado.md) property on a **Recordset** object to an array of bookmarks.</span></span> <span data-ttu-id="50d14-110">С помощью этого свойства можно определить, как не удалось получить запись, и разрешить ее соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="50d14-110">With this property, you can determine how a given record failed and resolve it accordingly.</span></span>

