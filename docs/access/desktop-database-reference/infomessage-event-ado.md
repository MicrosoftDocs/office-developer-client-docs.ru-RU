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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291444"
---
# <a name="infomessage-event-ado"></a><span data-ttu-id="94ff7-102">Событие InfoMessage (ADO)</span><span class="sxs-lookup"><span data-stu-id="94ff7-102">InfoMessage event (ADO)</span></span>

<span data-ttu-id="94ff7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="94ff7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="94ff7-104">Событие **InfoMessage** возникает при любом предупреждении во время операции **ConnectionEvent.**</span><span class="sxs-lookup"><span data-stu-id="94ff7-104">The **InfoMessage** event is called whenever a warning occurs during a **ConnectionEvent** operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="94ff7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94ff7-105">Syntax</span></span>

<span data-ttu-id="94ff7-106">InfoMessage *pError,* *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="94ff7-106">InfoMessage *pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="94ff7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="94ff7-107">Parameters</span></span>

|<span data-ttu-id="94ff7-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="94ff7-108">Parameter</span></span>|<span data-ttu-id="94ff7-109">Описание</span><span class="sxs-lookup"><span data-stu-id="94ff7-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="94ff7-110">*pError*</span><span class="sxs-lookup"><span data-stu-id="94ff7-110">*pError*</span></span> |<span data-ttu-id="94ff7-111">Объект [Error.](error-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="94ff7-111">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="94ff7-112">Этот параметр содержит все возвращаемые ошибки.</span><span class="sxs-lookup"><span data-stu-id="94ff7-112">This parameter contains any errors that are returned.</span></span> <span data-ttu-id="94ff7-113">Если возвращается несколько ошибок, выйдите из коллекции **Errors,** чтобы найти их.</span><span class="sxs-lookup"><span data-stu-id="94ff7-113">If multiple errors are returned, enumerate the **Errors** collection to find them.</span></span>|
|<span data-ttu-id="94ff7-114">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="94ff7-114">*adStatus*</span></span> |<span data-ttu-id="94ff7-115">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="94ff7-115">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="94ff7-116">Перед возвращением этого события установите для этого параметра **параметр adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="94ff7-116">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="94ff7-117">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="94ff7-117">*pConnection*</span></span> |<span data-ttu-id="94ff7-118">Объект [Connection.](connection-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="94ff7-118">A [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="94ff7-119">Подключение, для которого возникло предупреждение.</span><span class="sxs-lookup"><span data-stu-id="94ff7-119">The connection for which the warning occurred.</span></span> <span data-ttu-id="94ff7-120">Например, предупреждения могут возникать при открытии объекта **Connection** или выполнении [команды](command-object-ado.md) **подключения.**</span><span class="sxs-lookup"><span data-stu-id="94ff7-120">For example, warnings can occur when opening a **Connection** object or executing a [Command](command-object-ado.md) on a **Connection**.</span></span>|

