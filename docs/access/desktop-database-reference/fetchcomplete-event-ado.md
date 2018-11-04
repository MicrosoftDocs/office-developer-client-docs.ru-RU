---
title: Событие FetchComplete (ADO)
TOCTitle: FetchComplete event (ADO)
ms:assetid: 4863d5b5-7d77-bdef-c511-f85c9e6dec9d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249224(v=office.15)
ms:contentKeyID: 48544621
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed0f93fc8b58d94675377b3263ba60fb692a9a4e
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949495"
---
# <a name="fetchcomplete-event-ado"></a><span data-ttu-id="386e4-102">Событие FetchComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="386e4-102">FetchComplete event (ADO)</span></span>

<span data-ttu-id="386e4-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="386e4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="386e4-104">Событие **FetchComplete** вызывается после извлечения всех записей в объемных асинхронной операции в [набора записей](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="386e4-104">The **FetchComplete** event is called after all the records in a lengthy asynchronous operation have been retrieved into the [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="386e4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="386e4-105">Syntax</span></span>

<span data-ttu-id="386e4-106">FetchComplete*pError*, *adStatus* *pRecordset*</span><span class="sxs-lookup"><span data-stu-id="386e4-106">FetchComplete*pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="386e4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="386e4-107">Parameters</span></span>

|<span data-ttu-id="386e4-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="386e4-108">Parameter</span></span>|<span data-ttu-id="386e4-109">Описание</span><span class="sxs-lookup"><span data-stu-id="386e4-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="386e4-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="386e4-110">*pError*</span></span> |<span data-ttu-id="386e4-111">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="386e4-111">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="386e4-112">Описание ошибки, возникшей при имеет значение **adStatus** **adStatusErrorsOccurred**; в противном случае он не задан.</span><span class="sxs-lookup"><span data-stu-id="386e4-112">It describes the error that occurred if the value of **adStatus** is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="386e4-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="386e4-113">*adStatus*</span></span> |<span data-ttu-id="386e4-114">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="386e4-114">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="386e4-115">Прежде чем возвращает это событие, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="386e4-115">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="386e4-116">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="386e4-116">*pRecordset*</span></span> |<span data-ttu-id="386e4-117">Объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="386e4-117">A **Recordset** object.</span></span> <span data-ttu-id="386e4-118">Объект, для которого возвращенных записей.</span><span class="sxs-lookup"><span data-stu-id="386e4-118">The object for which the records were retrieved.</span></span>|

## <a name="remarks"></a><span data-ttu-id="386e4-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="386e4-119">Remarks</span></span>

<span data-ttu-id="386e4-120">Чтобы использовать **FetchComplete** с помощью Microsoft Visual Basic, необходим Visual Basic 6.0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="386e4-120">To use **FetchComplete** with Microsoft Visual Basic, Visual Basic 6.0 or later is required.</span></span>

