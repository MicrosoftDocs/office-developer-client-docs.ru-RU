---
title: События ConnectComplete и Disconnect (ADO)
TOCTitle: ConnectComplete and Disconnect events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e1e1d4487eb113c25e25ce6b9de051e33a4536b3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699389"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a><span data-ttu-id="542f7-102">События ConnectComplete и Disconnect (ADO)</span><span class="sxs-lookup"><span data-stu-id="542f7-102">ConnectComplete and Disconnect events (ADO)</span></span>

<span data-ttu-id="542f7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="542f7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="542f7-104">Событие **ConnectComplete** вызывается после подключения *запускается*.</span><span class="sxs-lookup"><span data-stu-id="542f7-104">The **ConnectComplete** event is called after a connection *starts*.</span></span> <span data-ttu-id="542f7-105">После подключения *завершается*вызывает события **Disconnect** .</span><span class="sxs-lookup"><span data-stu-id="542f7-105">The **Disconnect** event is called after a connection *ends*.</span></span>

## <a name="syntax"></a><span data-ttu-id="542f7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="542f7-106">Syntax</span></span>

<span data-ttu-id="542f7-107">ConnectComplete*pError*, *adStatus* *pConnection*</span><span class="sxs-lookup"><span data-stu-id="542f7-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="542f7-108">Отключите*adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="542f7-108">Disconnect*adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="542f7-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="542f7-109">Parameters</span></span>

|<span data-ttu-id="542f7-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="542f7-110">Parameter</span></span>|<span data-ttu-id="542f7-111">Описание</span><span class="sxs-lookup"><span data-stu-id="542f7-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="542f7-112">*pError*</span><span class="sxs-lookup"><span data-stu-id="542f7-112">*pError*</span></span> |<span data-ttu-id="542f7-113">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="542f7-113">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="542f7-114">Описание ошибки, возникшей при имеет значение *adStatus* **adStatusErrorsOccurred**; в противном случае он не задан.</span><span class="sxs-lookup"><span data-stu-id="542f7-114">It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="542f7-115">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="542f7-115">*adStatus*</span></span> |<span data-ttu-id="542f7-116">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="542f7-116">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="542f7-117">При вызове **ConnectComplete** этот параметр имеет значение **adStatusCancel** , если событие **WillConnect** запросил отмену ожидающие подключения.</span><span class="sxs-lookup"><span data-stu-id="542f7-117">When **ConnectComplete** is called, this parameter is set to **adStatusCancel** if a **WillConnect** event has requested cancellation of the pending connection.</span></span><br/><br/><span data-ttu-id="542f7-118">Прежде чем возвращает либо события, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="542f7-118">Before either event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span> <span data-ttu-id="542f7-119">Тем не менее закрыть и повторно открыть [подключение](connection-object-ado.md) вызывает эти события к еще раз.</span><span class="sxs-lookup"><span data-stu-id="542f7-119">However, closing and reopening the [Connection](connection-object-ado.md) causes these events to occur again.</span></span>|
|<span data-ttu-id="542f7-120">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="542f7-120">*pConnection*</span></span> |<span data-ttu-id="542f7-121">Объект **подключения** , для которого применяется данное событие.</span><span class="sxs-lookup"><span data-stu-id="542f7-121">The **Connection** object for which this event applies.</span></span>|

