---
title: Событие EndOfRecordset (ADO)
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
# <a name="endofrecordset-event-ado"></a><span data-ttu-id="b269f-102">Событие EndOfRecordset (ADO)</span><span class="sxs-lookup"><span data-stu-id="b269f-102">EndOfRecordset event (ADO)</span></span>

<span data-ttu-id="b269f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b269f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b269f-104">Событие **EndOfRecordset** вызвано при попытке перейти к строке, прошедшей в конце [recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b269f-104">The **EndOfRecordset** event is called when there is an attempt to move to a row past the end of the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b269f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b269f-105">Syntax</span></span>

<span data-ttu-id="b269f-106">EndOfRecordset *fMoreData*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="b269f-106">EndOfRecordset *fMoreData*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="b269f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b269f-107">Parameters</span></span>

|<span data-ttu-id="b269f-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="b269f-108">Parameter</span></span>|<span data-ttu-id="b269f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b269f-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b269f-110">*fMoreData*</span><span class="sxs-lookup"><span data-stu-id="b269f-110">*fMoreData*</span></span> |<span data-ttu-id="b269f-111">Значение **VARIANT \_ BOOL,** которое при заданном значении VARIANT TRUE указывает, что в набор Recordset добавлено больше \_ **строк.**</span><span class="sxs-lookup"><span data-stu-id="b269f-111">A **VARIANT\_BOOL** value that, if set to VARIANT\_TRUE, indicates more rows have been added to the **Recordset**.</span></span>|
|<span data-ttu-id="b269f-112">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="b269f-112">*adStatus*</span></span> |<span data-ttu-id="b269f-113">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="b269f-113">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="b269f-114">Когда **вызывается EndOfRecordset,** этот параметр задан **adStatusOK,** если операция, которая вызвала событие, была успешной.</span><span class="sxs-lookup"><span data-stu-id="b269f-114">When **EndOfRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="b269f-115">Оно задалось **adStatusCantDeny,** если это событие не может запросить отмену операции, которая вызвала это событие.</span><span class="sxs-lookup"><span data-stu-id="b269f-115">It is set to **adStatusCantDeny** if this event cannot request cancellation of the operation that caused this event.</span></span><br/><br/><span data-ttu-id="b269f-116">Перед **возвращением EndOfRecordset** установите этот параметр **adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="b269f-116">Before **EndOfRecordset** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="b269f-117">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="b269f-117">*pRecordset*</span></span> | <span data-ttu-id="b269f-118">Объект **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="b269f-118">A **Recordset** object.</span></span> <span data-ttu-id="b269f-119">**Набор записей,** для которого произошло это событие.</span><span class="sxs-lookup"><span data-stu-id="b269f-119">The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b269f-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="b269f-120">Remarks</span></span>

<span data-ttu-id="b269f-121">Событие **EndOfRecordset может** произойти в случае срыва операции [MoveNext.](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b269f-121">An **EndOfRecordset** event may occur if the [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) operation fails.</span></span>

<span data-ttu-id="b269f-122">Обработец этого события вызывается при попытке переместиться за конец объекта **Recordset,** возможно, в результате вызова **MoveNext**.</span><span class="sxs-lookup"><span data-stu-id="b269f-122">This event handler is called when an attempt is made to move past the end of the **Recordset** object, perhaps as a result of calling **MoveNext**.</span></span> <span data-ttu-id="b269f-123">Тем не менее, в этом случае можно получить больше записей из базы данных и примкать их к концу **recordset**.</span><span class="sxs-lookup"><span data-stu-id="b269f-123">However, while in this event, you could retrieve more records from a database and append them to the end of the **Recordset**.</span></span> <span data-ttu-id="b269f-124">В этом случае установите *fMoreData* в VARIANT \_ TRUE и вернись из **EndOfRecordset.**</span><span class="sxs-lookup"><span data-stu-id="b269f-124">In that case, set *fMoreData* to VARIANT\_TRUE, and return from **EndOfRecordset**.</span></span> <span data-ttu-id="b269f-125">Затем снова **позвоните в MoveNext,** чтобы получить доступ к вновь полученным записям.</span><span class="sxs-lookup"><span data-stu-id="b269f-125">Then call **MoveNext** again to access the newly retrieved records.</span></span>

