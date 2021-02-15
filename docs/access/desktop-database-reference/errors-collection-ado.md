---
title: Errors collection (ADO)
TOCTitle: Errors collection (ADO)
ms:assetid: 76c234b8-7fec-11c5-275e-864d5d880ee7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249486(v=office.15)
ms:contentKeyID: 48545706
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: db9fa4fccc4f3d13849f34c157f2ea07cc3f171d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293429"
---
# <a name="errors-collection-ado"></a><span data-ttu-id="3f3d9-102">Errors collection (ADO)</span><span class="sxs-lookup"><span data-stu-id="3f3d9-102">Errors collection (ADO)</span></span>


<span data-ttu-id="3f3d9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f3d9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3f3d9-104">Содержит все [объекты Error,](error-object-ado.md) созданные в ответ на один поставщик сбоев, связанный с поставщиком.</span><span class="sxs-lookup"><span data-stu-id="3f3d9-104">Contains all the [Error](error-object-ado.md) objects created in response to a single provider-related failure provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f3d9-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="3f3d9-105">Remarks</span></span>

<span data-ttu-id="3f3d9-106">Любая операция, включаемая объекты ADO, может создавать одну или несколько ошибок поставщика.</span><span class="sxs-lookup"><span data-stu-id="3f3d9-106">Any operation involving ADO objects can generate one or more provider errors.</span></span> <span data-ttu-id="3f3d9-107">При каждой ошибке один или несколько объектов **Error** можно поместить в коллекцию **Errors** объекта [Connection.](connection-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="3f3d9-107">As each error occurs, one or more **Error** objects can be placed in the **Errors** collection of the [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="3f3d9-108">Когда другая операция ADO создает ошибку, коллекция **Errors** очищается, и новый набор объектов **Error** можно поместить в коллекцию **Errors.**</span><span class="sxs-lookup"><span data-stu-id="3f3d9-108">When another ADO operation generates an error, the **Errors** collection is cleared, and the new set of **Error** objects can be placed in the **Errors** collection.</span></span>

<span data-ttu-id="3f3d9-109">Каждый **объект Error** представляет определенную ошибку поставщика, а не ошибку ADO.</span><span class="sxs-lookup"><span data-stu-id="3f3d9-109">Each **Error** object represents a specific provider error, not an ADO error.</span></span> <span data-ttu-id="3f3d9-110">Ошибки ADO оголевются механизмом обработки исключений во время работы.</span><span class="sxs-lookup"><span data-stu-id="3f3d9-110">ADO errors are exposed to the run-time exception-handling mechanism.</span></span> <span data-ttu-id="3f3d9-111">Например, в Microsoft Visual Basic ошибка ADO вызывает событие [onError](onerror-event-rds.md) и появляется в **объекте Err.**</span><span class="sxs-lookup"><span data-stu-id="3f3d9-111">For example, in Microsoft Visual Basic, the occurrence of an ADO-specific error will trigger an [onError](onerror-event-rds.md) event and appear in the **Err** object.</span></span>

<span data-ttu-id="3f3d9-112">Операции ADO, которые не вызывают ошибку, не влияют на **коллекцию ошибок.**</span><span class="sxs-lookup"><span data-stu-id="3f3d9-112">ADO operations that don't generate an error have no effect on the **Errors** collection.</span></span> <span data-ttu-id="3f3d9-113">Используйте метод [Clear](clear-method-ado.md) для очистки коллекции **Errors вручную.**</span><span class="sxs-lookup"><span data-stu-id="3f3d9-113">Use the [Clear](clear-method-ado.md) method to manually clear the **Errors** collection.</span></span>

<span data-ttu-id="3f3d9-114">Набор объектов **Error** в коллекции **Errors** описывает все ошибки, которые произошли в ответ на один из них.</span><span class="sxs-lookup"><span data-stu-id="3f3d9-114">The set of **Error** objects in the **Errors** collection describes all errors that occurred in response to a single statement.</span></span> <span data-ttu-id="3f3d9-115">Enumerating the specific errors in the Errors collection enables your error-handling **routines** to more precisely determine the cause and origin of an error, and take appropriate steps to recover.</span><span class="sxs-lookup"><span data-stu-id="3f3d9-115">Enumerating the specific errors in the **Errors** collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover.</span></span>

<span data-ttu-id="3f3d9-116">Некоторые свойства и методы возвращают предупреждения, которые отображаются как объекты **Error** в коллекции **Errors,** но не останавливают выполнение программы.</span><span class="sxs-lookup"><span data-stu-id="3f3d9-116">Some properties and methods return warnings that appear as **Error** objects in the **Errors** collection but do not halt a program's execution.</span></span> <span data-ttu-id="3f3d9-117">Перед вызовом методов [Resync,](resync-method-ado.md) [UpdateBatch](updatebatch-method-ado.md)или [CancelBatch](cancelbatch-method-ado.md) в [объекте Recordset,](recordset-object-ado.md) [методом Open](open-method-ado-connection.md) для объекта **Connection** или настройкам свойства [Filter](filter-property-ado.md) в **объекте Recordset** вызовите метод **Clear** для коллекции **Errors.**</span><span class="sxs-lookup"><span data-stu-id="3f3d9-117">Before you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object, the [Open](open-method-ado-connection.md) method on a **Connection** object, or set the [Filter](filter-property-ado.md) property on a **Recordset** object, call the **Clear** method on the **Errors** collection.</span></span> <span data-ttu-id="3f3d9-118">Таким образом можно считать свойство [Count](count-property-ado.md) коллекции **Errors** для проверки на возвращенных предупреждений.</span><span class="sxs-lookup"><span data-stu-id="3f3d9-118">That way you can read the [Count](count-property-ado.md) property of the **Errors** collection to test for returned warnings.</span></span>


> [!NOTE]
> <span data-ttu-id="3f3d9-119">Более **подробное описание** того, как одна операция ADO может создавать несколько ошибок, см. в разделе "Объект error".</span><span class="sxs-lookup"><span data-stu-id="3f3d9-119">See the **Error** object topic for a more detailed explanation of the way a single ADO operation can generate multiple errors.</span></span>


