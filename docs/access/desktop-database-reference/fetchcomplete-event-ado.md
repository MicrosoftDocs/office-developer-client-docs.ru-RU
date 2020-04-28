---
title: Событие событие fetchcomplete (ADO)
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
# <a name="fetchcomplete-event-ado"></a><span data-ttu-id="46b1d-102">Событие событие fetchcomplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="46b1d-102">FetchComplete event (ADO)</span></span>

<span data-ttu-id="46b1d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="46b1d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46b1d-104">Событие **событие fetchcomplete** вызывается после того, как в [набор записей](recordset-object-ado.md)были получены все записи длительной асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="46b1d-104">The **FetchComplete** event is called after all the records in a lengthy asynchronous operation have been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="46b1d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46b1d-105">Syntax</span></span>

<span data-ttu-id="46b1d-106">Событие fetchcomplete*перрор*, *адстатус*, *pRecordset* пред</span><span class="sxs-lookup"><span data-stu-id="46b1d-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="46b1d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="46b1d-107">Parameters</span></span>

|<span data-ttu-id="46b1d-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="46b1d-108">Parameter</span></span>|<span data-ttu-id="46b1d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="46b1d-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="46b1d-110">*перрор*</span><span class="sxs-lookup"><span data-stu-id="46b1d-110">*pError*</span></span> |<span data-ttu-id="46b1d-111">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="46b1d-111">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="46b1d-112">В нем описывается ошибка, которая возникла, если значение **адстатус** равно **адстатусеррорсоккурред**; в противном случае он не задается.</span><span class="sxs-lookup"><span data-stu-id="46b1d-112">It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="46b1d-113">*адстатус*</span><span class="sxs-lookup"><span data-stu-id="46b1d-113">*adStatus*</span></span> |<span data-ttu-id="46b1d-114">[Евентстатусенум](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="46b1d-114">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="46b1d-115">Перед возвращением этого события установите для этого параметра значение **адстатусунвантедевент** , чтобы предотвратить появление последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="46b1d-115">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="46b1d-116">*предшнур*</span><span class="sxs-lookup"><span data-stu-id="46b1d-116">*pRecordset*</span></span> |<span data-ttu-id="46b1d-117">Объект **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="46b1d-117">A **Recordset** object.</span></span> <span data-ttu-id="46b1d-118">Объект, для которого были получены записи.</span><span class="sxs-lookup"><span data-stu-id="46b1d-118">The object for which the records were retrieved.</span></span>|

## <a name="remarks"></a><span data-ttu-id="46b1d-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="46b1d-119">Remarks</span></span>

<span data-ttu-id="46b1d-120">Чтобы использовать **событие fetchcomplete** с Microsoft Visual Basic, требуется Visual Basic 6,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="46b1d-120">To use **FetchComplete** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>

