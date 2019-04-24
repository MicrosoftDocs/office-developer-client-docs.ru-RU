---
title: Событие событие executecomplete (ADO)
TOCTitle: ExecuteComplete event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8a094968e70ace5e6cba1df184bf0ba57c2d7789
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293226"
---
# <a name="executecomplete-event-ado"></a><span data-ttu-id="f8120-102">Событие событие executecomplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="f8120-102">ExecuteComplete event (ADO)</span></span>

<span data-ttu-id="f8120-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8120-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f8120-104">Событие **событие executecomplete** вызывается после завершения выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="f8120-104">The **ExecuteComplete** event is called after a command has finished executing.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8120-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8120-105">Syntax</span></span>

<span data-ttu-id="f8120-106">Событие executecomplete*рекордсаффектед*, *перрор*, *адстатус*, *пкомманд*, \*\* пода, *пконнектион*</span><span class="sxs-lookup"><span data-stu-id="f8120-106">ExecuteComplete*RecordsAffected*, *pError*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="f8120-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8120-107">Parameters</span></span>

|<span data-ttu-id="f8120-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="f8120-108">Parameter</span></span>|<span data-ttu-id="f8120-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f8120-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f8120-110">*Рекордсаффектед*</span><span class="sxs-lookup"><span data-stu-id="f8120-110">*RecordsAffected*</span></span> |<span data-ttu-id="f8120-111">**Длинное** значение, указывающее количество записей, на которые влияет команда.</span><span class="sxs-lookup"><span data-stu-id="f8120-111">A **Long** value indicating the number of records affected by the command.</span></span>|
|<span data-ttu-id="f8120-112">*Перрор*</span><span class="sxs-lookup"><span data-stu-id="f8120-112">*pError*</span></span> |<span data-ttu-id="f8120-113">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="f8120-113">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="f8120-114">В нем описывается ошибка, которая возникла, если значение **адстатус** равно **адстатусеррорсоккурред**; в противном случае он не задается.</span><span class="sxs-lookup"><span data-stu-id="f8120-114">It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="f8120-115">*Адстатус*</span><span class="sxs-lookup"><span data-stu-id="f8120-115">*adStatus*</span></span> |<span data-ttu-id="f8120-116">[Евентстатусенум](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="f8120-116">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="f8120-117">Перед возвращением этого события установите для этого параметра значение **адстатусунвантедевент** , чтобы предотвратить появление последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f8120-117">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="f8120-118">*Пкомманд*</span><span class="sxs-lookup"><span data-stu-id="f8120-118">*pCommand*</span></span> |<span data-ttu-id="f8120-119">[Командный](command-object-ado.md) объект, который был выполнен.</span><span class="sxs-lookup"><span data-stu-id="f8120-119">The [Command](command-object-ado.md) object that was executed.</span></span> <span data-ttu-id="f8120-120">Содержит объект **Command** даже при вызове метода **Connection. Execute** или **Recordset. Open** без явного создания **команды**, при этом объект **Command** создается внутри ADO.</span><span class="sxs-lookup"><span data-stu-id="f8120-120">Contains a **Command** object even when calling **Connection.Execute** or **Recordset.Open** without explicitly creating a **Command**, in which cases the **Command** object is created internally by ADO.</span></span>|
|<span data-ttu-id="f8120-121">*предшнур*</span><span class="sxs-lookup"><span data-stu-id="f8120-121">*pRecordset*</span></span> |<span data-ttu-id="f8120-122">Объект [Recordset](recordset-object-ado.md) , являющийся результатом выполненной команды.</span><span class="sxs-lookup"><span data-stu-id="f8120-122">A [Recordset](recordset-object-ado.md) object that is the result of the executed command.</span></span> <span data-ttu-id="f8120-123">Этот **набор записей** может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="f8120-123">This **Recordset** may be empty.</span></span> <span data-ttu-id="f8120-124">Не следует удалять этот объект Recordset из этого обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="f8120-124">You should never destroy this Recordset object from within this event handler.</span></span> <span data-ttu-id="f8120-125">Это приведет к нарушению прав доступа при попытке ADO получить доступ к объекту, который больше не существует.</span><span class="sxs-lookup"><span data-stu-id="f8120-125">Doing so will result in an Access Violation when ADO tries to access an object that no longer exists.</span></span>|
|<span data-ttu-id="f8120-126">*Пконнектион*</span><span class="sxs-lookup"><span data-stu-id="f8120-126">*pConnection*</span></span> |<span data-ttu-id="f8120-127">Объект [Connection](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="f8120-127">A [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="f8120-128">Подключение, для которого выполнялась операция.</span><span class="sxs-lookup"><span data-stu-id="f8120-128">The connection over which the operation was executed.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f8120-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="f8120-129">Remarks</span></span>

<span data-ttu-id="f8120-130">В связи с подключением может возникнуть событие **событие executecomplete** **.** [Выполнение](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **команда.** [EXECUTE](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.** [Открыть](open-method-ado-recordset.md), **Recordset.** [Requery](requery-method-ado.md)или **Recordset.** Методы [NextRecordset](nextrecordset-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="f8120-130">An **ExecuteComplete** event may occur due to the **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.**[Open](open-method-ado-recordset.md), **Recordset.**[Requery](requery-method-ado.md), or **Recordset.**[NextRecordset](nextrecordset-method-ado.md) methods.</span></span>

