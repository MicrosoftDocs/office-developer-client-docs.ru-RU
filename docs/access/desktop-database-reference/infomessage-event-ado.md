---
title: Событие InfoMessage (ADO)
TOCTitle: InfoMessage Event (ADO)
ms:assetid: 5d4f487f-96c8-4cf6-60ab-583510d3096f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249328(v=office.15)
ms:contentKeyID: 48545109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35e3962ed16415cf2d1ef2f470071a00185749bc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875303"
---
# <a name="infomessage-event-ado"></a><span data-ttu-id="175af-102">Событие InfoMessage (ADO)</span><span class="sxs-lookup"><span data-stu-id="175af-102">InfoMessage Event (ADO)</span></span>


<span data-ttu-id="175af-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="175af-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="175af-104">При появлении предупреждения в процессе выполнения операции **ConnectionEvent** вызывает события **InfoMessage** .</span><span class="sxs-lookup"><span data-stu-id="175af-104">The **InfoMessage** event is called whenever a warning occurs during a **ConnectionEvent** operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="175af-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="175af-105">Syntax</span></span>

<span data-ttu-id="175af-106">InfoMessage*pError*, *adStatus* *pConnection*</span><span class="sxs-lookup"><span data-stu-id="175af-106">InfoMessage*pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="175af-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="175af-107">Parameters</span></span>

  - <span data-ttu-id="175af-108">*pError*</span><span class="sxs-lookup"><span data-stu-id="175af-108">*pError*</span></span>

  - <span data-ttu-id="175af-109">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="175af-109">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="175af-110">Этот параметр содержит все ошибки, которые возвращаются.</span><span class="sxs-lookup"><span data-stu-id="175af-110">This parameter contains any errors that are returned.</span></span> <span data-ttu-id="175af-111">Если возвращаются несколько ошибок, перечисление семейство **Errors** их поиск.</span><span class="sxs-lookup"><span data-stu-id="175af-111">If multiple errors are returned, enumerate the **Errors** collection to find them.</span></span>

  - <span data-ttu-id="175af-112">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="175af-112">*adStatus*</span></span>

  - [<span data-ttu-id="175af-113">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="175af-113">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="175af-114">Прежде чем возвращает это событие, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="175af-114">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="175af-115">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="175af-115">*pConnection*</span></span>

  - <span data-ttu-id="175af-116">Объект [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="175af-116">A [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="175af-117">Подключение, для которого произошло предупреждение.</span><span class="sxs-lookup"><span data-stu-id="175af-117">The connection for which the warning occurred.</span></span> <span data-ttu-id="175af-118">К примеру, можно предупреждений при открытии **подключения** объекта или выполнения [команды](command-object-ado.md) для **подключения**.</span><span class="sxs-lookup"><span data-stu-id="175af-118">For example, warnings can occur when opening a **Connection** object or executing a [Command](command-object-ado.md) on a **Connection**.</span></span>

