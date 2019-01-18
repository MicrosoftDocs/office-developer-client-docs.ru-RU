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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721362"
---
# <a name="endofrecordset-event-ado"></a><span data-ttu-id="cb1e0-102">Событие EndOfRecordset (ADO)</span><span class="sxs-lookup"><span data-stu-id="cb1e0-102">EndOfRecordset event (ADO)</span></span>

<span data-ttu-id="cb1e0-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cb1e0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cb1e0-104">Событие **EndOfRecordset** вызывается при попытке перейдите к строке за пределами [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="cb1e0-104">The **EndOfRecordset** event is called when there is an attempt to move to a row past the end of the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cb1e0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb1e0-105">Syntax</span></span>

<span data-ttu-id="cb1e0-106">EndOfRecordset*fMoreData*, *adStatus* *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="cb1e0-106">EndOfRecordset*fMoreData*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="cb1e0-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="cb1e0-107">Parameters</span></span>

|<span data-ttu-id="cb1e0-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="cb1e0-108">Parameter</span></span>|<span data-ttu-id="cb1e0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="cb1e0-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="cb1e0-110">*fMoreData*</span><span class="sxs-lookup"><span data-stu-id="cb1e0-110">*fMoreData*</span></span> |<span data-ttu-id="cb1e0-111">A **ВАРИАНТА\_BOOL** значение, которое, если значение типа VARIANT\_имеет значение TRUE, указывает, были добавлены увеличение количества строк **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="cb1e0-111">A **VARIANT\_BOOL** value that, if set to VARIANT\_TRUE, indicates more rows have been added to the **Recordset**.</span></span>|
|<span data-ttu-id="cb1e0-112">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="cb1e0-112">*adStatus*</span></span> |<span data-ttu-id="cb1e0-113">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="cb1e0-113">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="cb1e0-114">При вызове **EndOfRecordset** этот параметр имеет значение **adStatusOK** , если операция, которая вызвала событие прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="cb1e0-114">When **EndOfRecordset** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful.</span></span> <span data-ttu-id="cb1e0-115">Если это событие не могут запрашивать отмену операции, вызвавшей это событие перейдут в **adStatusCantDeny** .</span><span class="sxs-lookup"><span data-stu-id="cb1e0-115">It is set to **adStatusCantDeny** if this event cannot request cancellation of the operation that caused this event.</span></span><br/><br/><span data-ttu-id="cb1e0-116">Прежде чем возвращает **EndOfRecordset** , присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="cb1e0-116">Before **EndOfRecordset** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="cb1e0-117">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="cb1e0-117">*pRecordset*</span></span> | <span data-ttu-id="cb1e0-118">Объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="cb1e0-118">A **Recordset** object.</span></span> <span data-ttu-id="cb1e0-119">**Набор записей** , для которого произошло это событие.</span><span class="sxs-lookup"><span data-stu-id="cb1e0-119">The **Recordset** for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="cb1e0-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="cb1e0-120">Remarks</span></span>

<span data-ttu-id="cb1e0-121">Событие **EndOfRecordset** может возникнуть, если происходит сбой операции [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="cb1e0-121">An **EndOfRecordset** event may occur if the [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) operation fails.</span></span>

<span data-ttu-id="cb1e0-122">Этот обработчик событий вызывается при попытке переместить за пределами объекта **набора записей** , может быть выполнена в результате вызова **MoveNext**.</span><span class="sxs-lookup"><span data-stu-id="cb1e0-122">This event handler is called when an attempt is made to move past the end of the **Recordset** object, perhaps as a result of calling **MoveNext**.</span></span> <span data-ttu-id="cb1e0-123">Тем не менее в это событие может получить несколько записей из базы данных и добавить их в конец **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="cb1e0-123">However, while in this event, you could retrieve more records from a database and append them to the end of the **Recordset**.</span></span> <span data-ttu-id="cb1e0-124">В этом случае значение типа VARIANT *fMoreData* \_значение TRUE, а возвращаемое из **EndOfRecordset**.</span><span class="sxs-lookup"><span data-stu-id="cb1e0-124">In that case, set *fMoreData* to VARIANT\_TRUE, and return from **EndOfRecordset**.</span></span> <span data-ttu-id="cb1e0-125">Затем вызовите **MoveNext** еще раз, чтобы получить доступ к недавно полученные записи.</span><span class="sxs-lookup"><span data-stu-id="cb1e0-125">Then call **MoveNext** again to access the newly retrieved records.</span></span>

