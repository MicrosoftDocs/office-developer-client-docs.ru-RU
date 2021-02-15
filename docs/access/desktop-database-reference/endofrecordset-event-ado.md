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
# <a name="endofrecordset-event-ado"></a><span data-ttu-id="c0ef7-102">Событие EndOfRecordset (ADO)</span><span class="sxs-lookup"><span data-stu-id="c0ef7-102">EndOfRecordset event (ADO)</span></span>

<span data-ttu-id="c0ef7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c0ef7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c0ef7-104">Событие **EndOfRecordset** вызвано при попытке перейти к строке за конец [recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="c0ef7-104">The **EndOfRecordset** event is called when there is an attempt to move to a row past the end of the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c0ef7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0ef7-105">Syntax</span></span>

<span data-ttu-id="c0ef7-106">EndOfRecordset *fMoreData*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="c0ef7-106">EndOfRecordset *fMoreData*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="c0ef7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0ef7-107">Parameters</span></span>

|<span data-ttu-id="c0ef7-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="c0ef7-108">Parameter</span></span>|<span data-ttu-id="c0ef7-109">Описание</span><span class="sxs-lookup"><span data-stu-id="c0ef7-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c0ef7-110">*fMoreData*</span><span class="sxs-lookup"><span data-stu-id="c0ef7-110">*fMoreData*</span></span> |<span data-ttu-id="c0ef7-111">Значение **VARIANT \_ BOOL,** если задано значение VARIANT TRUE, указывает, что в набор Recordset добавлены \_ **дополнительные строки.**</span><span class="sxs-lookup"><span data-stu-id="c0ef7-111">A **VARIANT\_BOOL** value that, if set to VARIANT\_TRUE, indicates more rows have been added to the **Recordset**.</span></span>|
|<span data-ttu-id="c0ef7-112">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="c0ef7-112">*adStatus*</span></span> |<span data-ttu-id="c0ef7-113">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="c0ef7-113">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="c0ef7-114">При **вызываемом endOfRecordset** этот параметр задан как **adStatusOK,** если операция, которая привела к событию, была успешной.</span><span class="sxs-lookup"><span data-stu-id="c0ef7-114">When **EndOfRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="c0ef7-115">Если это событие не может запросить отмену операции, которая привела к этому событию, устанавливается в качестве **adStatusCantDeny.**</span><span class="sxs-lookup"><span data-stu-id="c0ef7-115">It is set to **adStatusCantDeny** if this event cannot request cancellation of the operation that caused this event.</span></span><br/><br/><span data-ttu-id="c0ef7-116">Перед **возвращением EndOfRecordset** установите для этого параметра **параметр adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="c0ef7-116">Before **EndOfRecordset** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="c0ef7-117">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="c0ef7-117">*pRecordset*</span></span> | <span data-ttu-id="c0ef7-118">Объект **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="c0ef7-118">A **Recordset** object.</span></span> <span data-ttu-id="c0ef7-119">Набор **записей,** для которого произошло это событие.</span><span class="sxs-lookup"><span data-stu-id="c0ef7-119">The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="c0ef7-120">Заметки</span><span class="sxs-lookup"><span data-stu-id="c0ef7-120">Remarks</span></span>

<span data-ttu-id="c0ef7-121">Событие **EndOfRecordset может** произойти, если произойдет сбой операции [MoveNext.](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)</span><span class="sxs-lookup"><span data-stu-id="c0ef7-121">An **EndOfRecordset** event may occur if the [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) operation fails.</span></span>

<span data-ttu-id="c0ef7-122">Этот обработец событий вызывается при попытке переместиться за конец объекта **Recordset,** возможно, в результате вызова **MoveNext.**</span><span class="sxs-lookup"><span data-stu-id="c0ef7-122">This event handler is called when an attempt is made to move past the end of the **Recordset** object, perhaps as a result of calling **MoveNext**.</span></span> <span data-ttu-id="c0ef7-123">Однако в этом событии можно получить больше записей из базы данных и применить их к концу **recordset.**</span><span class="sxs-lookup"><span data-stu-id="c0ef7-123">However, while in this event, you could retrieve more records from a database and append them to the end of the **Recordset**.</span></span> <span data-ttu-id="c0ef7-124">В этом случае установите *для fMoreData* variant \_ TRUE и вернетесь из **EndOfRecordset.**</span><span class="sxs-lookup"><span data-stu-id="c0ef7-124">In that case, set *fMoreData* to VARIANT\_TRUE, and return from **EndOfRecordset**.</span></span> <span data-ttu-id="c0ef7-125">Затем снова **вызовите MoveNext,** чтобы получить доступ к недавно полученным записям.</span><span class="sxs-lookup"><span data-stu-id="c0ef7-125">Then call **MoveNext** again to access the newly retrieved records.</span></span>

