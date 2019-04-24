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
# <a name="infomessage-event-ado"></a><span data-ttu-id="d8ec1-102">Событие InfoMessage (ADO)</span><span class="sxs-lookup"><span data-stu-id="d8ec1-102">InfoMessage event (ADO)</span></span>

<span data-ttu-id="d8ec1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d8ec1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d8ec1-104">Событие **InfoMessage** вызывается при возникновении предупреждения в ходе операции **коннектионевент** .</span><span class="sxs-lookup"><span data-stu-id="d8ec1-104">The **InfoMessage** event is called whenever a warning occurs during a **ConnectionEvent** operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8ec1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8ec1-105">Syntax</span></span>

<span data-ttu-id="d8ec1-106">InfoMessage*перрор*, *адстатус*, *пконнектион*</span><span class="sxs-lookup"><span data-stu-id="d8ec1-106">InfoMessage*pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="d8ec1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8ec1-107">Parameters</span></span>

|<span data-ttu-id="d8ec1-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="d8ec1-108">Parameter</span></span>|<span data-ttu-id="d8ec1-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d8ec1-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d8ec1-110">*Перрор*</span><span class="sxs-lookup"><span data-stu-id="d8ec1-110">*pError*</span></span> |<span data-ttu-id="d8ec1-111">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d8ec1-111">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="d8ec1-112">Этот параметр содержит все возвращенные ошибки.</span><span class="sxs-lookup"><span data-stu-id="d8ec1-112">This parameter contains any errors that are returned.</span></span> <span data-ttu-id="d8ec1-113">Если возвращено несколько ошибок, перечислите \*\*\*\* коллекцию Errors, чтобы найти их.</span><span class="sxs-lookup"><span data-stu-id="d8ec1-113">If multiple errors are returned, enumerate the **Errors** collection to find them.</span></span>|
|<span data-ttu-id="d8ec1-114">*Адстатус*</span><span class="sxs-lookup"><span data-stu-id="d8ec1-114">*adStatus*</span></span> |<span data-ttu-id="d8ec1-115">[Евентстатусенум](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="d8ec1-115">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="d8ec1-116">Перед возвращением этого события установите для этого параметра значение **адстатусунвантедевент** , чтобы предотвратить появление последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="d8ec1-116">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>|
|<span data-ttu-id="d8ec1-117">*Пконнектион*</span><span class="sxs-lookup"><span data-stu-id="d8ec1-117">*pConnection*</span></span> |<span data-ttu-id="d8ec1-118">Объект [Connection](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d8ec1-118">A [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="d8ec1-119">Подключение, для которого возникло предупреждение.</span><span class="sxs-lookup"><span data-stu-id="d8ec1-119">The connection for which the warning occurred.</span></span> <span data-ttu-id="d8ec1-120">Например, предупреждения могут возникать при открытии объекта **Connection** или при выполнении [команды](command-object-ado.md) для **подключения**.</span><span class="sxs-lookup"><span data-stu-id="d8ec1-120">For example, warnings can occur when opening a **Connection** object or executing a [Command](command-object-ado.md) on a **Connection**.</span></span>|

