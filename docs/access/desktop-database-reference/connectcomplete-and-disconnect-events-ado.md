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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295991"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a><span data-ttu-id="738f9-102">События ConnectComplete и Disconnect (ADO)</span><span class="sxs-lookup"><span data-stu-id="738f9-102">ConnectComplete and Disconnect events (ADO)</span></span>

<span data-ttu-id="738f9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="738f9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="738f9-104">Событие **ConnectComplete** вызвано после начала *подключения.*</span><span class="sxs-lookup"><span data-stu-id="738f9-104">The **ConnectComplete** event is called after a connection *starts*.</span></span> <span data-ttu-id="738f9-105">Событие **Disconnect** вызвано после *окончания* подключения.</span><span class="sxs-lookup"><span data-stu-id="738f9-105">The **Disconnect** event is called after a connection *ends*.</span></span>

## <a name="syntax"></a><span data-ttu-id="738f9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="738f9-106">Syntax</span></span>

<span data-ttu-id="738f9-107">ConnectComplete *pError,* *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="738f9-107">ConnectComplete *pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="738f9-108">Disconnect *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="738f9-108">Disconnect *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="738f9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="738f9-109">Parameters</span></span>

|<span data-ttu-id="738f9-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="738f9-110">Parameter</span></span>|<span data-ttu-id="738f9-111">Описание</span><span class="sxs-lookup"><span data-stu-id="738f9-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="738f9-112">*pError*</span><span class="sxs-lookup"><span data-stu-id="738f9-112">*pError*</span></span> |<span data-ttu-id="738f9-113">Объект [Error.](error-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="738f9-113">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="738f9-114">В ней описывается ошибка, которая произошла, если *значением adStatus* является **adStatusErrorsOccurred;** в противном случае он не установлен.</span><span class="sxs-lookup"><span data-stu-id="738f9-114">It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="738f9-115">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="738f9-115">*adStatus*</span></span> |<span data-ttu-id="738f9-116">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="738f9-116">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="738f9-117">При **этом параметре** задан параметр **adStatusCancel,** если событие **WillConnect** запросит отмену ожидающих подключений.</span><span class="sxs-lookup"><span data-stu-id="738f9-117">When **ConnectComplete** is called, this parameter is set to **adStatusCancel** if a **WillConnect** event has requested cancellation of the pending connection.</span></span><br/><br/><span data-ttu-id="738f9-118">Перед возвратом любого из событий установите для этого параметра **параметр adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="738f9-118">Before either event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span> <span data-ttu-id="738f9-119">Однако закрытие и повторное открытие [подключения](connection-object-ado.md) приводит к повтору этих событий.</span><span class="sxs-lookup"><span data-stu-id="738f9-119">However, closing and reopening the [Connection](connection-object-ado.md) causes these events to occur again.</span></span>|
|<span data-ttu-id="738f9-120">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="738f9-120">*pConnection*</span></span> |<span data-ttu-id="738f9-121">Объект **Connection,** к которому применяется это событие.</span><span class="sxs-lookup"><span data-stu-id="738f9-121">The **Connection** object for which this event applies.</span></span>|

