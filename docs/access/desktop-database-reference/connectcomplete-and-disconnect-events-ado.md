---
title: ConnectComplete и отключите события (ADO)
TOCTitle: ConnectComplete and Disconnect Events (ADO)
ms:assetid: 8ecb080b-7fc9-7565-25bd-bd57b983750d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249629(v=office.15)
ms:contentKeyID: 48546293
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f9233ba547ecf746d3b4db7b4e008976a813afff
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891186"
---
# <a name="connectcomplete-and-disconnect-events-ado"></a><span data-ttu-id="574dd-102">ConnectComplete и отключите события (ADO)</span><span class="sxs-lookup"><span data-stu-id="574dd-102">ConnectComplete and Disconnect Events (ADO)</span></span>


<span data-ttu-id="574dd-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="574dd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="574dd-104">Событие **ConnectComplete** вызывается после подключения *запускается*.</span><span class="sxs-lookup"><span data-stu-id="574dd-104">The **ConnectComplete** event is called after a connection *starts*.</span></span> <span data-ttu-id="574dd-105">После подключения *завершается*вызывает события **Disconnect** .</span><span class="sxs-lookup"><span data-stu-id="574dd-105">The **Disconnect** event is called after a connection *ends*.</span></span>

## <a name="syntax"></a><span data-ttu-id="574dd-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="574dd-106">Syntax</span></span>

<span data-ttu-id="574dd-107">ConnectComplete*pError*, *adStatus* *pConnection*</span><span class="sxs-lookup"><span data-stu-id="574dd-107">ConnectComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="574dd-108">Отключите*adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="574dd-108">Disconnect*adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="574dd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="574dd-109">Parameters</span></span>

  - <span data-ttu-id="574dd-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="574dd-110">*pError*</span></span>

  - <span data-ttu-id="574dd-111">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="574dd-111">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="574dd-112">Описание ошибки, возникшей при имеет значение *adStatus* **adStatusErrorsOccurred**; в противном случае он не задан.</span><span class="sxs-lookup"><span data-stu-id="574dd-112">It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="574dd-113">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="574dd-113">*adStatus*</span></span>

  - [<span data-ttu-id="574dd-114">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="574dd-114">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="574dd-115">При вызове **ConnectComplete** этот параметр имеет значение **adStatusCancel** , если событие **WillConnect** запросил отмену ожидающие подключения.</span><span class="sxs-lookup"><span data-stu-id="574dd-115">When **ConnectComplete** is called, this parameter is set to **adStatusCancel** if a **WillConnect** event has requested cancellation of the pending connection.</span></span>
    
    <span data-ttu-id="574dd-116">Прежде чем возвращает либо события, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="574dd-116">Before either event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span> <span data-ttu-id="574dd-117">Тем не менее закрыть и повторно открыть [подключение](connection-object-ado.md) вызывает эти события к еще раз.</span><span class="sxs-lookup"><span data-stu-id="574dd-117">However, closing and reopening the [Connection](connection-object-ado.md) causes these events to occur again.</span></span>

  - <span data-ttu-id="574dd-118">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="574dd-118">*pConnection*</span></span>

  - <span data-ttu-id="574dd-119">Объект **подключения** , для которого применяется данное событие.</span><span class="sxs-lookup"><span data-stu-id="574dd-119">The **Connection** object for which this event applies.</span></span>

