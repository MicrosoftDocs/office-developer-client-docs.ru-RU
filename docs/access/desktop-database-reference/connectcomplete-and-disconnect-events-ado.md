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
# <a name="connectcomplete-and-disconnect-events-ado"></a><span data-ttu-id="3cd52-102">События ConnectComplete и Disconnect (ADO)</span><span class="sxs-lookup"><span data-stu-id="3cd52-102">ConnectComplete and Disconnect events (ADO)</span></span>

<span data-ttu-id="3cd52-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3cd52-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3cd52-104">Событие **ConnectComplete** вызвано после начала *подключения.*</span><span class="sxs-lookup"><span data-stu-id="3cd52-104">The **ConnectComplete** event is called after a connection *starts*.</span></span> <span data-ttu-id="3cd52-105">Событие **Отключение** вызвано после окончания *подключения.*</span><span class="sxs-lookup"><span data-stu-id="3cd52-105">The **Disconnect** event is called after a connection *ends*.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cd52-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3cd52-106">Syntax</span></span>

<span data-ttu-id="3cd52-107">ConnectComplete *pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="3cd52-107">ConnectComplete *pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="3cd52-108">*Отключение adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="3cd52-108">Disconnect *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="3cd52-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3cd52-109">Parameters</span></span>

|<span data-ttu-id="3cd52-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="3cd52-110">Parameter</span></span>|<span data-ttu-id="3cd52-111">Описание</span><span class="sxs-lookup"><span data-stu-id="3cd52-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3cd52-112">*pError*</span><span class="sxs-lookup"><span data-stu-id="3cd52-112">*pError*</span></span> |<span data-ttu-id="3cd52-113">Объект [Ошибки.](error-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="3cd52-113">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="3cd52-114">Он описывает ошибку, которая произошла, если значение *adStatus* **является adStatusErrorsOccurred;** в противном случае она не установлена.</span><span class="sxs-lookup"><span data-stu-id="3cd52-114">It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="3cd52-115">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="3cd52-115">*adStatus*</span></span> |<span data-ttu-id="3cd52-116">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="3cd52-116">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="3cd52-117">Когда **вызвана ConnectComplete,** этот параметр задан **adStatusCancel,** если событие **WillConnect** запрашивало отмену ожидаемого подключения.</span><span class="sxs-lookup"><span data-stu-id="3cd52-117">When **ConnectComplete** is called, this parameter is set to **adStatusCancel** if a **WillConnect** event has requested cancellation of the pending connection.</span></span><br/><br/><span data-ttu-id="3cd52-118">Перед возвращением любого события установите этот параметр **adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="3cd52-118">Before either event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span> <span data-ttu-id="3cd52-119">Однако закрытие и открытие подключения приводит [к](connection-object-ado.md) повторному повтору этих событий.</span><span class="sxs-lookup"><span data-stu-id="3cd52-119">However, closing and reopening the [Connection](connection-object-ado.md) causes these events to occur again.</span></span>|
|<span data-ttu-id="3cd52-120">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="3cd52-120">*pConnection*</span></span> |<span data-ttu-id="3cd52-121">Объект **Connection,** для которого применяется это событие.</span><span class="sxs-lookup"><span data-stu-id="3cd52-121">The **Connection** object for which this event applies.</span></span>|

