---
title: Status Property (ADO Recordset)
TOCTitle: Status Property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1ce4e3fc2d879521bbe1bbdb34d203a640fbe06c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480039"
---
# <a name="status-property-ado-recordset"></a><span data-ttu-id="38d09-102">Status Property (ADO Recordset)</span><span class="sxs-lookup"><span data-stu-id="38d09-102">Status Property (ADO Recordset)</span></span>


<span data-ttu-id="38d09-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="38d09-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="38d09-104">Указывает состояние текущей записи в отношении пакета обновлений или других массовых операций.</span><span class="sxs-lookup"><span data-stu-id="38d09-104">Indicates the status of the current record with respect to batch updates or other bulk operations.</span></span>

## <a name="return-value"></a><span data-ttu-id="38d09-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="38d09-105">Return Value</span></span>

<span data-ttu-id="38d09-106">Возвращает сумму значений [RecordStatusEnum](recordstatusenum.md) один или несколько.</span><span class="sxs-lookup"><span data-stu-id="38d09-106">Returns a sum of one or more [RecordStatusEnum](recordstatusenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="38d09-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="38d09-107">Remarks</span></span>

<span data-ttu-id="38d09-108">Используйте свойство **состояние** для просмотра изменений, ожидающих установки для записей, измененные во время обновления пакета.</span><span class="sxs-lookup"><span data-stu-id="38d09-108">Use the **Status** property to see what changes are pending for records modified during batch updating.</span></span> <span data-ttu-id="38d09-109">Также можно использовать свойство **состояние** для просмотра состояния с ошибкой во время массовых операций, таких как при вызове метода [выполнить повторную синхронизацию](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md)или [CancelBatch](cancelbatch-method-ado.md) методы для объекта [набора записей](recordset-object-ado.md) и задать [фильтра записи ](filter-property-ado.md)свойство объекта **набора записей** в массив закладки.</span><span class="sxs-lookup"><span data-stu-id="38d09-109">You can also use the **Status** property to view the status of records that fail during bulk operations, such as when you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object, or set the [Filter](filter-property-ado.md) property on a **Recordset** object to an array of bookmarks.</span></span> <span data-ttu-id="38d09-110">Это свойство можно определить, как данной записи не удалось и соответствующим образом ее решения.</span><span class="sxs-lookup"><span data-stu-id="38d09-110">With this property, you can determine how a given record failed and resolve it accordingly.</span></span>

