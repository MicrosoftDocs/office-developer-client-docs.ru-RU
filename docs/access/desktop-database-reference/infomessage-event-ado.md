---
title: Событие InfoMessage (ADO)
TOCTitle: InfoMessage event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 879d8e7b3733937687671a164f86dbb273cf7533
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699900"
---
# <a name="infomessage-event-ado"></a><span data-ttu-id="60416-102">Событие InfoMessage (ADO)</span><span class="sxs-lookup"><span data-stu-id="60416-102">InfoMessage event (ADO)</span></span>

<span data-ttu-id="60416-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="60416-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="60416-104">При появлении предупреждения в процессе выполнения операции **ConnectionEvent** вызывает события **InfoMessage** .</span><span class="sxs-lookup"><span data-stu-id="60416-104">The **InfoMessage** event is called whenever a warning occurs during a **ConnectionEvent** operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="60416-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60416-105">Syntax</span></span>

<span data-ttu-id="60416-106">InfoMessage*pError*, *adStatus* *pConnection*</span><span class="sxs-lookup"><span data-stu-id="60416-106">InfoMessage*pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="60416-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="60416-107">Parameters</span></span>

|<span data-ttu-id="60416-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="60416-108">Parameter</span></span>|<span data-ttu-id="60416-109">Описание</span><span class="sxs-lookup"><span data-stu-id="60416-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="60416-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="60416-110">*pError*</span></span> |<span data-ttu-id="60416-111">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="60416-111">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="60416-112">Этот параметр содержит все ошибки, которые возвращаются.</span><span class="sxs-lookup"><span data-stu-id="60416-112">This parameter contains any errors that are returned.</span></span> <span data-ttu-id="60416-113">Если возвращаются несколько ошибок, перечисление семейство **Errors** их поиск.</span><span class="sxs-lookup"><span data-stu-id="60416-113">If multiple errors are returned, enumerate the **Errors** collection to find them.</span></span>|
|<span data-ttu-id="60416-114">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="60416-114">*adStatus*</span></span> |<span data-ttu-id="60416-115">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="60416-115">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="60416-116">Прежде чем возвращает это событие, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="60416-116">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="60416-117">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="60416-117">*pConnection*</span></span> |<span data-ttu-id="60416-118">Объект [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="60416-118">A [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="60416-119">Подключение, для которого произошло предупреждение.</span><span class="sxs-lookup"><span data-stu-id="60416-119">The connection for which the warning occurred.</span></span> <span data-ttu-id="60416-120">К примеру, можно предупреждений при открытии **подключения** объекта или выполнения [команды](command-object-ado.md) для **подключения**.</span><span class="sxs-lookup"><span data-stu-id="60416-120">For example, warnings can occur when opening a **Connection** object or executing a [Command](command-object-ado.md) on a **Connection**.</span></span>|

