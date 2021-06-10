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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293191"
---
# <a name="fetchcomplete-event-ado"></a><span data-ttu-id="953da-102">Событие FetchComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="953da-102">FetchComplete event (ADO)</span></span>

<span data-ttu-id="953da-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="953da-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="953da-104">Событие **FetchComplete** вызвано после того, как все записи в длинной асинхронной операции были извлечены в [набор Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="953da-104">The **FetchComplete** event is called after all the records in a lengthy asynchronous operation have been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="953da-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="953da-105">Syntax</span></span>

<span data-ttu-id="953da-106">FetchComplete *pError*, *adStatus*, *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="953da-106">FetchComplete *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="953da-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="953da-107">Parameters</span></span>

|<span data-ttu-id="953da-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="953da-108">Parameter</span></span>|<span data-ttu-id="953da-109">Описание</span><span class="sxs-lookup"><span data-stu-id="953da-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="953da-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="953da-110">*pError*</span></span> |<span data-ttu-id="953da-111">Объект [Ошибки.](error-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="953da-111">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="953da-112">Он описывает ошибку, которая произошла, если значение **adStatus** **является adStatusErrorsOccurred;** в противном случае она не установлена.</span><span class="sxs-lookup"><span data-stu-id="953da-112">It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="953da-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="953da-113">*adStatus*</span></span> |<span data-ttu-id="953da-114">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="953da-114">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="953da-115">Перед возвращением этого события установите этот параметр **adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="953da-115">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="953da-116">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="953da-116">*pRecordset*</span></span> |<span data-ttu-id="953da-117">Объект **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="953da-117">A **Recordset** object.</span></span> <span data-ttu-id="953da-118">Объект, для которого были извлечены записи.</span><span class="sxs-lookup"><span data-stu-id="953da-118">The object for which the records were retrieved.</span></span>|

## <a name="remarks"></a><span data-ttu-id="953da-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="953da-119">Remarks</span></span>

<span data-ttu-id="953da-120">Чтобы использовать **FetchComplete** с microsoft Visual Basic, Visual Basic 6.0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="953da-120">To use **FetchComplete** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>

