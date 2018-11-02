---
title: Событие ExecuteComplete (ADO)
TOCTitle: ExecuteComplete event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 58683a8721ede0e7535b159f095b44bc6db6c1b7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926733"
---
# <a name="executecomplete-event-ado"></a><span data-ttu-id="b1553-102">Событие ExecuteComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="b1553-102">ExecuteComplete event (ADO)</span></span>


<span data-ttu-id="b1553-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1553-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="b1553-104">Событие **ExecuteComplete** вызывается после завершения выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="b1553-104">The **ExecuteComplete** event is called after a command has finished executing.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1553-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1553-105">Syntax</span></span>

<span data-ttu-id="b1553-106">ExecuteComplete*RecordsAffected*, *pError*, *adStatus*, *командной*, *pRecordset*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="b1553-106">ExecuteComplete*RecordsAffected*, *pError*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="b1553-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1553-107">Parameters</span></span>

  - <span data-ttu-id="b1553-108">*RecordsAffected*</span><span class="sxs-lookup"><span data-stu-id="b1553-108">*RecordsAffected*</span></span>

  - <span data-ttu-id="b1553-109">**Длинное** значение, указывающее количество записей командой.</span><span class="sxs-lookup"><span data-stu-id="b1553-109">A **Long** value indicating the number of records affected by the command.</span></span>

  - <span data-ttu-id="b1553-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="b1553-110">*pError*</span></span>

  - <span data-ttu-id="b1553-111">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b1553-111">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="b1553-112">Описание ошибки, возникшей при имеет значение **adStatus** **adStatusErrorsOccurred**; в противном случае он не задан.</span><span class="sxs-lookup"><span data-stu-id="b1553-112">It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="b1553-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="b1553-113">*adStatus*</span></span>

  - [<span data-ttu-id="b1553-114">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="b1553-114">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="b1553-115">Прежде чем возвращает это событие, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="b1553-115">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="b1553-116">*Командной*</span><span class="sxs-lookup"><span data-stu-id="b1553-116">*pCommand*</span></span>

  - <span data-ttu-id="b1553-117">Объект [команды](command-object-ado.md) , который был выполнен.</span><span class="sxs-lookup"><span data-stu-id="b1553-117">The [Command](command-object-ado.md) object that was executed.</span></span> <span data-ttu-id="b1553-118">Содержит объект **команды** , даже в том случае, если вызов **Connection.Execute** или **Recordset.Open** без явного создания **команды**, в каких случаях объект **команды** создается внутренне с ADO.</span><span class="sxs-lookup"><span data-stu-id="b1553-118">Contains a **Command** object even when calling **Connection.Execute** or **Recordset.Open** without explicitly creating a **Command**, in which cases the **Command** object is created internally by ADO.</span></span>

  - <span data-ttu-id="b1553-119">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="b1553-119">*pRecordset*</span></span>

  - <span data-ttu-id="b1553-120">Объект [набора записей](recordset-object-ado.md) , в результате выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="b1553-120">A [Recordset](recordset-object-ado.md) object that is the result of the executed command.</span></span> <span data-ttu-id="b1553-121">Этот **набор записей** может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="b1553-121">This **Recordset** may be empty.</span></span> <span data-ttu-id="b1553-122">Никогда не следует удалить объект набора записей из в этот обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="b1553-122">You should never destroy this Recordset object from within this event handler.</span></span> <span data-ttu-id="b1553-123">Это приведет к нарушение прав доступа, когда ADO пытается получить доступ к объекту, который больше не существует.</span><span class="sxs-lookup"><span data-stu-id="b1553-123">Doing so will result in an Access Violation when ADO tries to access an object that no longer exists.</span></span>

  - <span data-ttu-id="b1553-124">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="b1553-124">*pConnection*</span></span>

  - <span data-ttu-id="b1553-125">Объект [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b1553-125">A [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="b1553-126">Подключение, для которого была выполнена операция.</span><span class="sxs-lookup"><span data-stu-id="b1553-126">The connection over which the operation was executed.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1553-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="b1553-127">Remarks</span></span>

<span data-ttu-id="b1553-128">Событие **ExecuteComplete** может возникнуть из-за **подключения.** [Выполнение](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **команда.** [Выполнение](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **набора записей.** После [открытия](open-method-ado-recordset.md) **набора записей.** [Повторный запрос](requery-method-ado.md), или **набора записей.** Методы [NextRecordset](nextrecordset-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b1553-128">An **ExecuteComplete** event may occur due to the **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.**[Open](open-method-ado-recordset.md), **Recordset.**[Requery](requery-method-ado.md), or **Recordset.**[NextRecordset](nextrecordset-method-ado.md) methods.</span></span>

