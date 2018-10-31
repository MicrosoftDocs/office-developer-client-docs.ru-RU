---
title: Семейство errors (ADO)
TOCTitle: Errors Collection (ADO)
ms:assetid: 76c234b8-7fec-11c5-275e-864d5d880ee7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249486(v=office.15)
ms:contentKeyID: 48545706
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 568524bf2be93720ec319b48a784dfc62bd03f65
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863306"
---
# <a name="errors-collection-ado"></a><span data-ttu-id="4ced2-102">Семейство errors (ADO)</span><span class="sxs-lookup"><span data-stu-id="4ced2-102">Errors Collection (ADO)</span></span>


<span data-ttu-id="4ced2-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ced2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4ced2-104">Содержит все объекты [ошибки](error-object-ado.md) , созданные в ответ на сбой поставщика единого поставщика.</span><span class="sxs-lookup"><span data-stu-id="4ced2-104">Contains all the [Error](error-object-ado.md) objects created in response to a single provider-related failure provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ced2-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="4ced2-105">Remarks</span></span>

<span data-ttu-id="4ced2-106">Любые операции, включающие использование объекты ADO можно создать одну или несколько ошибок поставщика.</span><span class="sxs-lookup"><span data-stu-id="4ced2-106">Any operation involving ADO objects can generate one or more provider errors.</span></span> <span data-ttu-id="4ced2-107">Как возникают ошибки, один или несколько объектов **об ошибках** могут размещаться в семействе **Errors** объекта [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="4ced2-107">As each error occurs, one or more **Error** objects can be placed in the **Errors** collection of the [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="4ced2-108">Когда другой операции ADO создает сообщение об ошибке, семейство **Errors** снят и новый набор объектов **ошибок** , которые могут размещаться в семействе **Errors** .</span><span class="sxs-lookup"><span data-stu-id="4ced2-108">When another ADO operation generates an error, the **Errors** collection is cleared, and the new set of **Error** objects can be placed in the **Errors** collection.</span></span>

<span data-ttu-id="4ced2-109">Каждый объект **Error** представляет ошибку определенного поставщика, не ошибка ADO.</span><span class="sxs-lookup"><span data-stu-id="4ced2-109">Each **Error** object represents a specific provider error, not an ADO error.</span></span> <span data-ttu-id="4ced2-110">Ошибки ADO предоставляются механизм обработки исключений времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="4ced2-110">ADO errors are exposed to the run-time exception-handling mechanism.</span></span> <span data-ttu-id="4ced2-111">Например в Microsoft Visual Basic возникновение ошибки конкретного ADO будет активировать событие [onError](onerror-event-rds.md) и отображаются в объекта **Err** .</span><span class="sxs-lookup"><span data-stu-id="4ced2-111">For example, in Microsoft Visual Basic, the occurrence of an ADO-specific error will trigger an [onError](onerror-event-rds.md) event and appear in the **Err** object.</span></span>

<span data-ttu-id="4ced2-112">ADO операций, которые не возникнет ошибка не оказывают влияния на семейство **Errors** .</span><span class="sxs-lookup"><span data-stu-id="4ced2-112">ADO operations that don't generate an error have no effect on the **Errors** collection.</span></span> <span data-ttu-id="4ced2-113">Используйте метод [снимите](clear-method-ado.md) как вручную удалить семейство **Errors** .</span><span class="sxs-lookup"><span data-stu-id="4ced2-113">Use the [Clear](clear-method-ado.md) method to manually clear the **Errors** collection.</span></span>

<span data-ttu-id="4ced2-114">Набор объектов **об ошибке** в семействе **Errors** описаны все ошибки, возникшие в ответ на одной инструкции.</span><span class="sxs-lookup"><span data-stu-id="4ced2-114">The set of **Error** objects in the **Errors** collection describes all errors that occurred in response to a single statement.</span></span> <span data-ttu-id="4ced2-115">Перечисление отдельных ошибок в семействе **Errors** позволяет вашей процедуры обработки ошибок более точно определить причину и источник ошибки и выполните соответствующие действия для восстановления.</span><span class="sxs-lookup"><span data-stu-id="4ced2-115">Enumerating the specific errors in the **Errors** collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover.</span></span>

<span data-ttu-id="4ced2-116">Некоторые свойства и методы возвращают предупреждения, которые отображаются в виде объектов **ошибок** в семействе **Errors** , но не приостановить выполнение программы.</span><span class="sxs-lookup"><span data-stu-id="4ced2-116">Some properties and methods return warnings that appear as **Error** objects in the **Errors** collection but do not halt a program's execution.</span></span> <span data-ttu-id="4ced2-117">Прежде чем вызов [выполнить повторную синхронизацию](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md)или [CancelBatch](cancelbatch-method-ado.md) методы объекта [набора записей](recordset-object-ado.md) , метод [Open](open-method-ado-connection.md) на объект **подключения** или установить свойство [фильтра](filter-property-ado.md) для объекта **набора записей** , звонков метод **Clear** на семейство **Errors** .</span><span class="sxs-lookup"><span data-stu-id="4ced2-117">Before you call the [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), or [CancelBatch](cancelbatch-method-ado.md) methods on a [Recordset](recordset-object-ado.md) object, the [Open](open-method-ado-connection.md) method on a **Connection** object, or set the [Filter](filter-property-ado.md) property on a **Recordset** object, call the **Clear** method on the **Errors** collection.</span></span> <span data-ttu-id="4ced2-118">В этом случае могут читать свойство [Count](count-property-ado.md) коллекции **ошибок** для проверки возвращенных предупреждения.</span><span class="sxs-lookup"><span data-stu-id="4ced2-118">That way you can read the [Count](count-property-ado.md) property of the **Errors** collection to test for returned warnings.</span></span>


> [!NOTE]
> <span data-ttu-id="4ced2-119">В разделе **ошибки** объекта для более подробное описание способа за одну операцию ADO можно создать несколько ошибок.</span><span class="sxs-lookup"><span data-stu-id="4ced2-119">See the **Error** object topic for a more detailed explanation of the way a single ADO operation can generate multiple errors.</span></span>


