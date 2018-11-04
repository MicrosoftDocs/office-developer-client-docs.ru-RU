---
title: Событие ExecuteComplete (ADO)
TOCTitle: ExecuteComplete event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 49ab3d51deae86a02a486da224459bcfaaf057b2
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949680"
---
# <a name="executecomplete-event-ado"></a><span data-ttu-id="a58e8-102">Событие ExecuteComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="a58e8-102">ExecuteComplete event (ADO)</span></span>

<span data-ttu-id="a58e8-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a58e8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a58e8-104">Событие **ExecuteComplete** вызывается после завершения выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="a58e8-104">The **ExecuteComplete** event is called after a command has finished executing.</span></span>

## <a name="syntax"></a><span data-ttu-id="a58e8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a58e8-105">Syntax</span></span>

<span data-ttu-id="a58e8-106">ExecuteComplete*RecordsAffected*, *pError*, *adStatus*, *командной*, *pRecordset*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="a58e8-106">ExecuteComplete*RecordsAffected*, *pError*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="a58e8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a58e8-107">Parameters</span></span>

|<span data-ttu-id="a58e8-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="a58e8-108">Parameter</span></span>|<span data-ttu-id="a58e8-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a58e8-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a58e8-110">*RecordsAffected*</span><span class="sxs-lookup"><span data-stu-id="a58e8-110">*RecordsAffected*</span></span> |<span data-ttu-id="a58e8-111">**Длинное** значение, указывающее количество записей командой.</span><span class="sxs-lookup"><span data-stu-id="a58e8-111">A **Long** value indicating the number of records affected by the command.</span></span>|
|<span data-ttu-id="a58e8-112">*pError*</span><span class="sxs-lookup"><span data-stu-id="a58e8-112">*pError*</span></span> |<span data-ttu-id="a58e8-113">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a58e8-113">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="a58e8-114">Описание ошибки, возникшей при имеет значение **adStatus** **adStatusErrorsOccurred**; в противном случае он не задан.</span><span class="sxs-lookup"><span data-stu-id="a58e8-114">It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="a58e8-115">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="a58e8-115">*adStatus*</span></span> |<span data-ttu-id="a58e8-116">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="a58e8-116">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="a58e8-117">Прежде чем возвращает это событие, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="a58e8-117">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="a58e8-118">*Командной*</span><span class="sxs-lookup"><span data-stu-id="a58e8-118">*pCommand*</span></span> |<span data-ttu-id="a58e8-119">Объект [команды](command-object-ado.md) , который был выполнен.</span><span class="sxs-lookup"><span data-stu-id="a58e8-119">The [Command](command-object-ado.md) object that was executed.</span></span> <span data-ttu-id="a58e8-120">Содержит объект **команды** , даже в том случае, если вызов **Connection.Execute** или **Recordset.Open** без явного создания **команды**, в каких случаях объект **команды** создается внутренне с ADO.</span><span class="sxs-lookup"><span data-stu-id="a58e8-120">Contains a **Command** object even when calling **Connection.Execute** or **Recordset.Open** without explicitly creating a **Command**, in which cases the **Command** object is created internally by ADO.</span></span>|
|<span data-ttu-id="a58e8-121">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="a58e8-121">*pRecordset*</span></span> |<span data-ttu-id="a58e8-122">Объект [набора записей](recordset-object-ado.md) , в результате выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="a58e8-122">A [Recordset](recordset-object-ado.md) object that is the result of the executed command.</span></span> <span data-ttu-id="a58e8-123">Этот **набор записей** может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="a58e8-123">This **Recordset** may be empty.</span></span> <span data-ttu-id="a58e8-124">Никогда не следует удалить объект набора записей из в этот обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="a58e8-124">You should never destroy this Recordset object from within this event handler.</span></span> <span data-ttu-id="a58e8-125">Это приведет к нарушение прав доступа, когда ADO пытается получить доступ к объекту, который больше не существует.</span><span class="sxs-lookup"><span data-stu-id="a58e8-125">Doing so will result in an Access Violation when ADO tries to access an object that no longer exists.</span></span>|
|<span data-ttu-id="a58e8-126">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="a58e8-126">*pConnection*</span></span> |<span data-ttu-id="a58e8-127">Объект [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a58e8-127">A [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="a58e8-128">Подключение, для которого была выполнена операция.</span><span class="sxs-lookup"><span data-stu-id="a58e8-128">The connection over which the operation was executed.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a58e8-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="a58e8-129">Remarks</span></span>

<span data-ttu-id="a58e8-130">Событие **ExecuteComplete** может возникнуть из-за **подключения.** [Выполнение](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **команда.** [Выполнение](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **набора записей.** После [открытия](open-method-ado-recordset.md) **набора записей.** [Повторный запрос](requery-method-ado.md), или **набора записей.** Методы [NextRecordset](nextrecordset-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a58e8-130">An **ExecuteComplete** event may occur due to the **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.**[Open](open-method-ado-recordset.md), **Recordset.**[Requery](requery-method-ado.md), or **Recordset.**[NextRecordset](nextrecordset-method-ado.md) methods.</span></span>

