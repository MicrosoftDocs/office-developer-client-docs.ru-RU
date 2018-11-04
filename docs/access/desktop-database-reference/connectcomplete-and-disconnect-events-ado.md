---
title: События ConnectComplete и Disconnect (ADO)
TOCTitle: ConnectComplete and Disconnect events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f49bbffc2cfbaec77bf1b0d6aa692412c45254ae
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949686"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a><span data-ttu-id="410cd-102">События ConnectComplete и Disconnect (ADO)</span><span class="sxs-lookup"><span data-stu-id="410cd-102">ConnectComplete and Disconnect events (ADO)</span></span>

<span data-ttu-id="410cd-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="410cd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="410cd-104">Событие **ConnectComplete** вызывается после подключения *запускается*.</span><span class="sxs-lookup"><span data-stu-id="410cd-104">The **ConnectComplete** event is called after a connection *starts*.</span></span> <span data-ttu-id="410cd-105">После подключения *завершается*вызывает события **Disconnect** .</span><span class="sxs-lookup"><span data-stu-id="410cd-105">The **Disconnect** event is called after a connection *ends*.</span></span>

## <a name="syntax"></a><span data-ttu-id="410cd-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="410cd-106">Syntax</span></span>

<span data-ttu-id="410cd-107">ConnectComplete*pError*, *adStatus* *pConnection*</span><span class="sxs-lookup"><span data-stu-id="410cd-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="410cd-108">Отключите*adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="410cd-108">Disconnect*adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="410cd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="410cd-109">Parameters</span></span>

|<span data-ttu-id="410cd-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="410cd-110">Parameter</span></span>|<span data-ttu-id="410cd-111">Описание</span><span class="sxs-lookup"><span data-stu-id="410cd-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="410cd-112">*pError*</span><span class="sxs-lookup"><span data-stu-id="410cd-112">*pError*</span></span> |<span data-ttu-id="410cd-113">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="410cd-113">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="410cd-114">Описание ошибки, возникшей при имеет значение *adStatus* **adStatusErrorsOccurred**; в противном случае он не задан.</span><span class="sxs-lookup"><span data-stu-id="410cd-114">It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="410cd-115">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="410cd-115">*adStatus*</span></span> |<span data-ttu-id="410cd-116">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="410cd-116">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="410cd-117">При вызове **ConnectComplete** этот параметр имеет значение **adStatusCancel** , если событие **WillConnect** запросил отмену ожидающие подключения.</span><span class="sxs-lookup"><span data-stu-id="410cd-117">When **ConnectComplete** is called, this parameter is set to **adStatusCancel** if a **WillConnect** event has requested cancellation of the pending connection.</span></span><br/><br/><span data-ttu-id="410cd-118">Прежде чем возвращает либо события, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="410cd-118">Before either event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span> <span data-ttu-id="410cd-119">Тем не менее закрыть и повторно открыть [подключение](connection-object-ado.md) вызывает эти события к еще раз.</span><span class="sxs-lookup"><span data-stu-id="410cd-119">However, closing and reopening the [Connection](connection-object-ado.md) causes these events to occur again.</span></span>|
|<span data-ttu-id="410cd-120">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="410cd-120">*pConnection*</span></span> |<span data-ttu-id="410cd-121">Объект **подключения** , для которого применяется данное событие.</span><span class="sxs-lookup"><span data-stu-id="410cd-121">The **Connection** object for which this event applies.</span></span>|

