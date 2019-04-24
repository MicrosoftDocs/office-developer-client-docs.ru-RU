---
title: Событие событие endofrecordset (ADO)
TOCTitle: EndOfRecordset event (ADO)
ms:assetid: 8995b851-dff6-2525-1d62-a2cfb4f95393
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249603(v=office.15)
ms:contentKeyID: 48546167
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48e0eb25b443175013a144fafaa433df12c2cc9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293562"
---
# <a name="endofrecordset-event-ado"></a><span data-ttu-id="d8611-102">Событие событие endofrecordset (ADO)</span><span class="sxs-lookup"><span data-stu-id="d8611-102">EndOfRecordset event (ADO)</span></span>

<span data-ttu-id="d8611-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d8611-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d8611-104">Событие **событие endofrecordset** вызывается при попытке переместиться в строку, находящиеся за концом объекта [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d8611-104">The **EndOfRecordset** event is called when there is an attempt to move to a row past the end of the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d8611-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8611-105">Syntax</span></span>

<span data-ttu-id="d8611-106">Событие endofrecordset*фморедата*, *адстатус*, \*\* пред</span><span class="sxs-lookup"><span data-stu-id="d8611-106">EndOfRecordset*fMoreData*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="d8611-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8611-107">Parameters</span></span>

|<span data-ttu-id="d8611-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="d8611-108">Parameter</span></span>|<span data-ttu-id="d8611-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d8611-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d8611-110">*Фморедата*</span><span class="sxs-lookup"><span data-stu-id="d8611-110">*fMoreData*</span></span> |<span data-ttu-id="d8611-111">**Логическое значение\_Variant** , которое, если задано значение\_Variant true, указывает, что в **набор записей**Добавлено больше строк.</span><span class="sxs-lookup"><span data-stu-id="d8611-111">A **VARIANT\_BOOL** value that, if set to VARIANT\_TRUE, indicates more rows have been added to the **Recordset**.</span></span>|
|<span data-ttu-id="d8611-112">*Адстатус*</span><span class="sxs-lookup"><span data-stu-id="d8611-112">*adStatus*</span></span> |<span data-ttu-id="d8611-113">[Евентстатусенум](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="d8611-113">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="d8611-114">При вызове **событие endofrecordset** этот параметр имеет значение **адстатусок** , если операция, вызвавшая событие, прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="d8611-114">When **EndOfRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="d8611-115">Он имеет значение **адстатускантдени** , если данное событие не может запрашивать отмену операции, вызвавшей это событие.</span><span class="sxs-lookup"><span data-stu-id="d8611-115">It is set to **adStatusCantDeny** if this event cannot request cancellation of the operation that caused this event.</span></span><br/><br/><span data-ttu-id="d8611-116">Перед возвратом **событие endofrecordset** присвойте этому параметру значение **адстатусунвантедевент** , чтобы предотвратить появление последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d8611-116">Before **EndOfRecordset** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="d8611-117">*предшнур*</span><span class="sxs-lookup"><span data-stu-id="d8611-117">*pRecordset*</span></span> | <span data-ttu-id="d8611-118">Объект **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="d8611-118">A **Recordset** object.</span></span> <span data-ttu-id="d8611-119">Объект **Recordset** , для которого произошло это событие.</span><span class="sxs-lookup"><span data-stu-id="d8611-119">The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d8611-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="d8611-120">Remarks</span></span>

<span data-ttu-id="d8611-121">Если не удается выполнить операцию [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) , может произойти событие **событие endofrecordset** .</span><span class="sxs-lookup"><span data-stu-id="d8611-121">An **EndOfRecordset** event may occur if the [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) operation fails.</span></span>

<span data-ttu-id="d8611-122">Этот обработчик событий вызывается при попытке переместиться за конец объекта **Recordset** , возможно, в результате вызова **MoveNext**.</span><span class="sxs-lookup"><span data-stu-id="d8611-122">This event handler is called when an attempt is made to move past the end of the **Recordset** object, perhaps as a result of calling **MoveNext**.</span></span> <span data-ttu-id="d8611-123">Однако в этом событии можно получить дополнительные записи из базы данных и добавить их в конец **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="d8611-123">However, while in this event, you could retrieve more records from a database and append them to the end of the **Recordset**.</span></span> <span data-ttu-id="d8611-124">В этом случае задайте для *фморедата* \_значение true и вернитесь из **событие endofrecordset**.</span><span class="sxs-lookup"><span data-stu-id="d8611-124">In that case, set *fMoreData* to VARIANT\_TRUE, and return from **EndOfRecordset**.</span></span> <span data-ttu-id="d8611-125">Затем снова вызовите **MoveNext** , чтобы получить доступ к недавно извлеченным записям.</span><span class="sxs-lookup"><span data-stu-id="d8611-125">Then call **MoveNext** again to access the newly retrieved records.</span></span>

