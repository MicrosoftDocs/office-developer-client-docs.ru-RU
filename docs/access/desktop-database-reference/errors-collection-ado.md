---
title: Коллекция Errors (ADO)
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
# <a name="errors-collection-ado"></a><span data-ttu-id="eed5e-102">Коллекция Errors (ADO)</span><span class="sxs-lookup"><span data-stu-id="eed5e-102">Errors collection (ADO)</span></span>


<span data-ttu-id="eed5e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eed5e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eed5e-104">Содержит все объекты [Error](error-object-ado.md) , созданные в ответ на один поставщик сбоев, связанный с поставщиком.</span><span class="sxs-lookup"><span data-stu-id="eed5e-104">Contains all the [Error](error-object-ado.md) objects created in response to a single provider-related failure provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="eed5e-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="eed5e-105">Remarks</span></span>

<span data-ttu-id="eed5e-106">Любая операция, включающая объекты ADO, может создавать одну или несколько ошибок поставщика.</span><span class="sxs-lookup"><span data-stu-id="eed5e-106">Any operation involving ADO objects can generate one or more provider errors.</span></span> <span data-ttu-id="eed5e-107">При возникновении каждой ошибки в коллекцию **Errors** объекта [Connection](connection-object-ado.md) можно поместить один или несколько объектов **Error** .</span><span class="sxs-lookup"><span data-stu-id="eed5e-107">As each error occurs, one or more **Error** objects can be placed in the **Errors** collection of the [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="eed5e-108">Если при выполнении другой операции ADO возникает ошибка, удаляется коллекция **Errors** , и в коллекцию **Errors** можно поместить новый набор объектов **Error** .</span><span class="sxs-lookup"><span data-stu-id="eed5e-108">When another ADO operation generates an error, the **Errors** collection is cleared, and the new set of **Error** objects can be placed in the **Errors** collection.</span></span>

<span data-ttu-id="eed5e-109">Каждый объект **Error** представляет определенную ошибку поставщика, а не ошибку ADO.</span><span class="sxs-lookup"><span data-stu-id="eed5e-109">Each **Error** object represents a specific provider error, not an ADO error.</span></span> <span data-ttu-id="eed5e-110">Ошибки ADO, доступные в механизме обработки исключений времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="eed5e-110">ADO errors are exposed to the run-time exception-handling mechanism.</span></span> <span data-ttu-id="eed5e-111">Например, в Microsoft Visual Basic при возникновении ошибки, относящейся к ADO, вызывается событие [OnError](onerror-event-rds.md) и отображается в объекте **Err** .</span><span class="sxs-lookup"><span data-stu-id="eed5e-111">For example, in Microsoft Visual Basic, the occurrence of an ADO-specific error will trigger an [onError](onerror-event-rds.md) event and appear in the **Err** object.</span></span>

<span data-ttu-id="eed5e-112">Операции ADO, не создающие ошибку, не влияют на коллекцию **Errors** .</span><span class="sxs-lookup"><span data-stu-id="eed5e-112">ADO operations that don't generate an error have no effect on the **Errors** collection.</span></span> <span data-ttu-id="eed5e-113">Используйте метод [clear](clear-method-ado.md) для очистки коллекции **ошибок** вручную.</span><span class="sxs-lookup"><span data-stu-id="eed5e-113">Use the [Clear](clear-method-ado.md) method to manually clear the **Errors** collection.</span></span>

<span data-ttu-id="eed5e-114">Набор объектов **Error** в коллекции **Errors** описывает все ошибки, произошедшие в ответ на один оператор.</span><span class="sxs-lookup"><span data-stu-id="eed5e-114">The set of **Error** objects in the **Errors** collection describes all errors that occurred in response to a single statement.</span></span> <span data-ttu-id="eed5e-115">Перечисление определенных ошибок **в семействе Errors** позволяет подпрограммам обработки ошибок определять причину и происхождение ошибки и выполнять необходимые действия для восстановления.</span><span class="sxs-lookup"><span data-stu-id="eed5e-115">Enumerating the specific errors in the **Errors** collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover.</span></span>

<span data-ttu-id="eed5e-116">Некоторые свойства и методы возвращают предупреждения, которые отображаются как объекты **Error** в коллекции **Errors** , но не приводят к остановке выполнения программы.</span><span class="sxs-lookup"><span data-stu-id="eed5e-116">Some properties and methods return warnings that appear as **Error** objects in the **Errors** collection but do not halt a program's execution.</span></span> <span data-ttu-id="eed5e-117">Перед вызовом методов [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md)или [CancelBatch](cancelbatch-method-ado.md) для объекта [Recordset](recordset-object-ado.md) , метода [Open](open-method-ado-connection.md) для объекта **Connection** или установки свойства [Filter](filter-property-ado.md) для объекта **Recordset** вызовите метод **clear** в коллекции **Errors** .</span><span class="sxs-lookup"><span data-stu-id="eed5e-117">Before you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object, the [Open](open-method-ado-connection.md) method on a **Connection** object, or set the [Filter](filter-property-ado.md) property on a **Recordset** object, call the **Clear** method on the **Errors** collection.</span></span> <span data-ttu-id="eed5e-118">Таким образом можно прочитать свойство [Count](count-property-ado.md) коллекции **Errors** , чтобы проверить наличие возвращенных предупреждений.</span><span class="sxs-lookup"><span data-stu-id="eed5e-118">That way you can read the [Count](count-property-ado.md) property of the **Errors** collection to test for returned warnings.</span></span>


> [!NOTE]
> <span data-ttu-id="eed5e-119">В разделе **Error** Object содержится более подробное объяснение того, как одна операция ADO может создавать несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="eed5e-119">See the **Error** object topic for a more detailed explanation of the way a single ADO operation can generate multiple errors.</span></span>


