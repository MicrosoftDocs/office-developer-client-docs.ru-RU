---
title: Status Property (ADO Recordset)
TOCTitle: Status Property (ADO Recordset)
ms:assetid: bf3ccb36-c985-5fae-4f76-c48a0e20e6f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249930(v=office.15)
ms:contentKeyID: 48547482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1979ad721a01ef72c08da1531a8826ec320915e5
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604619"
---
# <a name="status-property-ado-recordset"></a><span data-ttu-id="14c67-102">Status Property (ADO Recordset)</span><span class="sxs-lookup"><span data-stu-id="14c67-102">Status Property (ADO Recordset)</span></span>


<span data-ttu-id="14c67-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="14c67-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="14c67-104">Указывает состояние текущей записи в отношении пакета обновлений или других массовых операций.</span><span class="sxs-lookup"><span data-stu-id="14c67-104">Indicates the status of the current record with respect to batch updates or other bulk operations.</span></span>

<span data-ttu-id="14c67-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="14c67-105"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="14c67-106">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14c67-106">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="14c67-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14c67-107">Return value</span></span>
>>>>>>> <span data-ttu-id="14c67-108">master</span><span class="sxs-lookup"><span data-stu-id="14c67-108">master</span></span>

<span data-ttu-id="14c67-109">Возвращает сумму значений [RecordStatusEnum](recordstatusenum.md) один или несколько.</span><span class="sxs-lookup"><span data-stu-id="14c67-109">Returns a sum of one or more [RecordStatusEnum](recordstatusenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="14c67-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="14c67-110">Remarks</span></span>

<span data-ttu-id="14c67-111">Используйте свойство **состояние** для просмотра изменений, ожидающих установки для записей, измененные во время обновления пакета.</span><span class="sxs-lookup"><span data-stu-id="14c67-111">Use the **Status** property to see what changes are pending for records modified during batch updating.</span></span> <span data-ttu-id="14c67-112">Также можно использовать свойство **состояние** для просмотра состояния с ошибкой во время массовых операций, таких как при вызове метода [выполнить повторную синхронизацию](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md)или [CancelBatch](cancelbatch-method-ado.md) методы для объекта [набора записей](recordset-object-ado.md) и задать [фильтра записи ](filter-property-ado.md)свойство объекта **набора записей** в массив закладки.</span><span class="sxs-lookup"><span data-stu-id="14c67-112">You can also use the **Status** property to view the status of records that fail during bulk operations, such as when you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object, or set the [Filter](filter-property-ado.md) property on a **Recordset** object to an array of bookmarks.</span></span> <span data-ttu-id="14c67-113">Это свойство можно определить, как данной записи не удалось и соответствующим образом ее решения.</span><span class="sxs-lookup"><span data-stu-id="14c67-113">With this property, you can determine how a given record failed and resolve it accordingly.</span></span>

