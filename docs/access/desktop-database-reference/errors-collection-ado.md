---
title: Коллекция ошибок (ADO)
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
# <a name="errors-collection-ado"></a><span data-ttu-id="52d48-102">Коллекция ошибок (ADO)</span><span class="sxs-lookup"><span data-stu-id="52d48-102">Errors collection (ADO)</span></span>


<span data-ttu-id="52d48-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="52d48-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="52d48-104">Содержит все [объекты ошибки,](error-object-ado.md) созданные в ответ на один поставщик сбоев, связанных с поставщиком.</span><span class="sxs-lookup"><span data-stu-id="52d48-104">Contains all the [Error](error-object-ado.md) objects created in response to a single provider-related failure provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="52d48-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="52d48-105">Remarks</span></span>

<span data-ttu-id="52d48-106">Любая операция с объектами ADO может создавать одну или несколько ошибок поставщика.</span><span class="sxs-lookup"><span data-stu-id="52d48-106">Any operation involving ADO objects can generate one or more provider errors.</span></span> <span data-ttu-id="52d48-107">По мере возникновения каждой ошибки в коллекцию **Ошибок** объекта Подключения можно поместить один или несколько объектов [ошибки.](connection-object-ado.md) </span><span class="sxs-lookup"><span data-stu-id="52d48-107">As each error occurs, one or more **Error** objects can be placed in the **Errors** collection of the [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="52d48-108">Когда другая операция ADO создает  ошибку, коллекция ошибок очищается,  и новый набор объектов ошибки может быть помещен в коллекцию **Ошибок.**</span><span class="sxs-lookup"><span data-stu-id="52d48-108">When another ADO operation generates an error, the **Errors** collection is cleared, and the new set of **Error** objects can be placed in the **Errors** collection.</span></span>

<span data-ttu-id="52d48-109">Каждый **объект Ошибки** представляет собой определенную ошибку поставщика, а не ошибку ADO.</span><span class="sxs-lookup"><span data-stu-id="52d48-109">Each **Error** object represents a specific provider error, not an ADO error.</span></span> <span data-ttu-id="52d48-110">Ошибки ADO подвергаются воздействию механизма обработки исключений во время работы.</span><span class="sxs-lookup"><span data-stu-id="52d48-110">ADO errors are exposed to the run-time exception-handling mechanism.</span></span> <span data-ttu-id="52d48-111">Например, в microsoft Visual Basic, возникновение ошибки, определенной для ADO, вызовет событие [onError](onerror-event-rds.md) и появится в объекте **Err.**</span><span class="sxs-lookup"><span data-stu-id="52d48-111">For example, in Microsoft Visual Basic, the occurrence of an ADO-specific error will trigger an [onError](onerror-event-rds.md) event and appear in the **Err** object.</span></span>

<span data-ttu-id="52d48-112">Операции ADO, которые не создают ошибку, не влияют на коллекцию **ошибок.**</span><span class="sxs-lookup"><span data-stu-id="52d48-112">ADO operations that don't generate an error have no effect on the **Errors** collection.</span></span> <span data-ttu-id="52d48-113">Используйте метод [Clear,](clear-method-ado.md) чтобы вручную очистить коллекцию **ошибок.**</span><span class="sxs-lookup"><span data-stu-id="52d48-113">Use the [Clear](clear-method-ado.md) method to manually clear the **Errors** collection.</span></span>

<span data-ttu-id="52d48-114">Набор объектов **ошибки** в коллекции **Errors** описывает все ошибки, которые произошли в ответ на одно утверждение.</span><span class="sxs-lookup"><span data-stu-id="52d48-114">The set of **Error** objects in the **Errors** collection describes all errors that occurred in response to a single statement.</span></span> <span data-ttu-id="52d48-115">Переопределение определенных ошибок  в коллекции Ошибок позволяет вашим процедурам обработки ошибок точнее определить причину и происхождение ошибки и принять соответствующие меры для восстановления.</span><span class="sxs-lookup"><span data-stu-id="52d48-115">Enumerating the specific errors in the **Errors** collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover.</span></span>

<span data-ttu-id="52d48-116">Некоторые свойства и методы возвращают предупреждения, которые отображаются как объекты ошибки в коллекции **Errors,** но не останавливают выполнение программы. </span><span class="sxs-lookup"><span data-stu-id="52d48-116">Some properties and methods return warnings that appear as **Error** objects in the **Errors** collection but do not halt a program's execution.</span></span> <span data-ttu-id="52d48-117">Прежде чем вызывать  методы [Resync,](resync-method-ado.md) [UpdateBatch или CancelBatch](cancelbatch-method-ado.md) на [](open-method-ado-connection.md) [объекте Recordset,](recordset-object-ado.md) метод [](filter-property-ado.md) Open на объекте Подключение или установить свойство Filter на **объекте Recordset,** вызывай метод Clear в коллекции **Ошибок.** [](updatebatch-method-ado.md) </span><span class="sxs-lookup"><span data-stu-id="52d48-117">Before you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object, the [Open](open-method-ado-connection.md) method on a **Connection** object, or set the [Filter](filter-property-ado.md) property on a **Recordset** object, call the **Clear** method on the **Errors** collection.</span></span> <span data-ttu-id="52d48-118">Таким образом вы можете прочитать свойство [Count](count-property-ado.md) из коллекции **Ошибок** для проверки на возврат предупреждений.</span><span class="sxs-lookup"><span data-stu-id="52d48-118">That way you can read the [Count](count-property-ado.md) property of the **Errors** collection to test for returned warnings.</span></span>


> [!NOTE]
> <span data-ttu-id="52d48-119">Дополнительные **сведения** о том, как одна операция ADO может создавать несколько ошибок, см. в разделе Объект Error.</span><span class="sxs-lookup"><span data-stu-id="52d48-119">See the **Error** object topic for a more detailed explanation of the way a single ADO operation can generate multiple errors.</span></span>


