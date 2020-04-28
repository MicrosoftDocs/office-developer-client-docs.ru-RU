---
title: События события connectcomplete и Disconnect (ADO)
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
# <a name="connectcomplete-and-disconnect-events-ado"></a><span data-ttu-id="01700-102">События события connectcomplete и Disconnect (ADO)</span><span class="sxs-lookup"><span data-stu-id="01700-102">ConnectComplete and Disconnect events (ADO)</span></span>

<span data-ttu-id="01700-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="01700-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="01700-104">Событие **события connectcomplete** вызывается после *запуска*подключения.</span><span class="sxs-lookup"><span data-stu-id="01700-104">The **ConnectComplete** event is called after a connection *starts*.</span></span> <span data-ttu-id="01700-105">Событие **Disconnect** вызывается после *завершения*подключения.</span><span class="sxs-lookup"><span data-stu-id="01700-105">The **Disconnect** event is called after a connection *ends*.</span></span>

## <a name="syntax"></a><span data-ttu-id="01700-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01700-106">Syntax</span></span>

<span data-ttu-id="01700-107">События connectcomplete*перрор*, *адстатус*, *пконнектион*</span><span class="sxs-lookup"><span data-stu-id="01700-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="01700-108">Отключение*адстатус*, *пконнектион*</span><span class="sxs-lookup"><span data-stu-id="01700-108">Disconnect*adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="01700-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="01700-109">Parameters</span></span>

|<span data-ttu-id="01700-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="01700-110">Parameter</span></span>|<span data-ttu-id="01700-111">Описание</span><span class="sxs-lookup"><span data-stu-id="01700-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="01700-112">*перрор*</span><span class="sxs-lookup"><span data-stu-id="01700-112">*pError*</span></span> |<span data-ttu-id="01700-113">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="01700-113">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="01700-114">В нем описывается ошибка, которая возникла, если значение *адстатус* равно **адстатусеррорсоккурред**; в противном случае он не задается.</span><span class="sxs-lookup"><span data-stu-id="01700-114">It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>|
|<span data-ttu-id="01700-115">*адстатус*</span><span class="sxs-lookup"><span data-stu-id="01700-115">*adStatus*</span></span> |<span data-ttu-id="01700-116">[Евентстатусенум](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="01700-116">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="01700-117">При вызове **события connectcomplete** этот параметр имеет значение **адстатусканцел** , если событие **событие willconnect** запросило отмену ожидающего подключения.</span><span class="sxs-lookup"><span data-stu-id="01700-117">When **ConnectComplete** is called, this parameter is set to **adStatusCancel** if a **WillConnect** event has requested cancellation of the pending connection.</span></span><br/><br/><span data-ttu-id="01700-118">Перед возвращением любого события установите для этого параметра значение **адстатусунвантедевент** , чтобы предотвратить появление последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="01700-118">Before either event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span> <span data-ttu-id="01700-119">Однако закрытие и повторное открытие [подключения](connection-object-ado.md) приводит к повторному возникновению этих событий.</span><span class="sxs-lookup"><span data-stu-id="01700-119">However, closing and reopening the [Connection](connection-object-ado.md) causes these events to occur again.</span></span>|
|<span data-ttu-id="01700-120">*пконнектион*</span><span class="sxs-lookup"><span data-stu-id="01700-120">*pConnection*</span></span> |<span data-ttu-id="01700-121">Объект **Connection** , к которому относится данное событие.</span><span class="sxs-lookup"><span data-stu-id="01700-121">The **Connection** object for which this event applies.</span></span>|

