---
title: События ConnectComplete и Disconnect (ADO)
TOCTitle: ConnectComplete and Disconnect events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2799feebc3d2c2c4599249f0af310cf4020dcb49
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945518"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a><span data-ttu-id="744d4-102">События ConnectComplete и Disconnect (ADO)</span><span class="sxs-lookup"><span data-stu-id="744d4-102">ConnectComplete and Disconnect events (ADO)</span></span>


<span data-ttu-id="744d4-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="744d4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="744d4-104">Событие **ConnectComplete** вызывается после подключения *запускается*.</span><span class="sxs-lookup"><span data-stu-id="744d4-104">The **ConnectComplete** event is called after a connection *starts*.</span></span> <span data-ttu-id="744d4-105">После подключения *завершается*вызывает события **Disconnect** .</span><span class="sxs-lookup"><span data-stu-id="744d4-105">The **Disconnect** event is called after a connection *ends*.</span></span>

## <a name="syntax"></a><span data-ttu-id="744d4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="744d4-106">Syntax</span></span>

<span data-ttu-id="744d4-107">ConnectComplete*pError*, *adStatus* *pConnection*</span><span class="sxs-lookup"><span data-stu-id="744d4-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="744d4-108">Отключите*adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="744d4-108">Disconnect*adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="744d4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="744d4-109">Parameters</span></span>

- <span data-ttu-id="744d4-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="744d4-110">*pError*</span></span>

  - <span data-ttu-id="744d4-111">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="744d4-111">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="744d4-112">Описание ошибки, возникшей при имеет значение *adStatus* **adStatusErrorsOccurred**; в противном случае он не задан.</span><span class="sxs-lookup"><span data-stu-id="744d4-112">It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

- <span data-ttu-id="744d4-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="744d4-113">*adStatus*</span></span>

  - [<span data-ttu-id="744d4-114">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="744d4-114">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="744d4-115">При вызове **ConnectComplete** этот параметр имеет значение **adStatusCancel** , если событие **WillConnect** запросил отмену ожидающие подключения.</span><span class="sxs-lookup"><span data-stu-id="744d4-115">When **ConnectComplete** is called, this parameter is set to **adStatusCancel** if a **WillConnect** event has requested cancellation of the pending connection.</span></span>
    
    <span data-ttu-id="744d4-116">Прежде чем возвращает либо события, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="744d4-116">Before either event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span> <span data-ttu-id="744d4-117">Тем не менее закрыть и повторно открыть [подключение](connection-object-ado.md) вызывает эти события к еще раз.</span><span class="sxs-lookup"><span data-stu-id="744d4-117">However, closing and reopening the [Connection](connection-object-ado.md) causes these events to occur again.</span></span>

- <span data-ttu-id="744d4-118">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="744d4-118">*pConnection*</span></span>

  - <span data-ttu-id="744d4-119">Объект **подключения** , для которого применяется данное событие.</span><span class="sxs-lookup"><span data-stu-id="744d4-119">The **Connection** object for which this event applies.</span></span>

