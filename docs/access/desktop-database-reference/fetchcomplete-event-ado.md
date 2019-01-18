---
title: Событие FetchComplete (ADO)
TOCTitle: FetchComplete event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f4c1cb1379d1faec39fd44fa8273fba4aadca548
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701965"
---
# <a name="fetchcomplete-event-ado"></a><span data-ttu-id="50f85-102">Событие FetchComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="50f85-102">FetchComplete event (ADO)</span></span>

<span data-ttu-id="50f85-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="50f85-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="50f85-104">Событие **FetchComplete** вызывается после извлечения всех записей в объемных асинхронной операции в [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="50f85-104">The **FetchComplete** event is called after all the records in a lengthy asynchronous operation have been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="50f85-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50f85-105">Syntax</span></span>

<span data-ttu-id="50f85-106">FetchComplete*pError*, *adStatus* *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="50f85-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="50f85-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="50f85-107">Parameters</span></span>

|<span data-ttu-id="50f85-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="50f85-108">Parameter</span></span>|<span data-ttu-id="50f85-109">Описание</span><span class="sxs-lookup"><span data-stu-id="50f85-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="50f85-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="50f85-110">*pError*</span></span> |<span data-ttu-id="50f85-111">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="50f85-111">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="50f85-112">Описание ошибки, возникшей при имеет значение **adStatus** **adStatusErrorsOccurred**; в противном случае он не задан.</span><span class="sxs-lookup"><span data-stu-id="50f85-112">It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="50f85-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="50f85-113">*adStatus*</span></span> |<span data-ttu-id="50f85-114">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="50f85-114">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="50f85-115">Прежде чем возвращает это событие, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="50f85-115">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="50f85-116">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="50f85-116">*pRecordset*</span></span> |<span data-ttu-id="50f85-117">Объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="50f85-117">A **Recordset** object.</span></span> <span data-ttu-id="50f85-118">Объект, для которого возвращенных записей.</span><span class="sxs-lookup"><span data-stu-id="50f85-118">The object for which the records were retrieved.</span></span>|

## <a name="remarks"></a><span data-ttu-id="50f85-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="50f85-119">Remarks</span></span>

<span data-ttu-id="50f85-120">Чтобы использовать **FetchComplete** с помощью Microsoft Visual Basic, необходим Visual Basic 6.0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="50f85-120">To use **FetchComplete** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>

