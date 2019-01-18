---
title: Типы событий (Справочник по для настольных баз данных Access)
TOCTitle: Types of Events
ms:assetid: 94660fc1-65c3-1d21-c451-f3898014e0b6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249660(v=office.15)
ms:contentKeyID: 48546414
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3bcf631ffc6c9b4b847af3f973114d6b271d26f5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718142"
---
# <a name="types-of-events"></a><span data-ttu-id="a26ce-102">Типы событий</span><span class="sxs-lookup"><span data-stu-id="a26ce-102">Types of events</span></span>


<span data-ttu-id="a26ce-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a26ce-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="a26ce-104">Существует два основных типа событий.</span><span class="sxs-lookup"><span data-stu-id="a26ce-104">There are two basic types of events.</span></span> <span data-ttu-id="a26ce-105">«Будет события,» вызываемые до начала операции, обычно включает «Будет» в именах — например, **WillChangeRecordset** или **WillConnect**.</span><span class="sxs-lookup"><span data-stu-id="a26ce-105">"Will Events," which are called before an operation starts, usually include "Will" in their names — for example, **WillChangeRecordset** or **WillConnect**.</span></span> <span data-ttu-id="a26ce-106">События, которые вызываются после выполнения события, обычно включают «Полная» в именах — например, **RecordChangeComplete** или **ConnectComplete**.</span><span class="sxs-lookup"><span data-stu-id="a26ce-106">Events that are called after an event has been completed usually include "Complete" in their names — for example, **RecordChangeComplete** or **ConnectComplete**.</span></span> <span data-ttu-id="a26ce-107">Существуют исключения, например **InfoMessage** —, но это происходит после завершения операции.</span><span class="sxs-lookup"><span data-stu-id="a26ce-107">Exceptions exist — such as **InfoMessage** — but these occur after the associated operation has completed.</span></span>

## <a name="will-events"></a><span data-ttu-id="a26ce-108">Будет событий</span><span class="sxs-lookup"><span data-stu-id="a26ce-108">Will Events</span></span>

<span data-ttu-id="a26ce-109">Обработчики событий вызывается перед началом операции предлагают возможность проверить или изменить параметры операции и отменить операцию или разрешить его завершения.</span><span class="sxs-lookup"><span data-stu-id="a26ce-109">Event handlers called before the operation starts offer you the opportunity to examine or modify the operation parameters, and then either cancel the operation or allow it to complete.</span></span> <span data-ttu-id="a26ce-110">Эти процедуры обработчика событий обычно есть имена формы \**будет*события \*\*\*.</span><span class="sxs-lookup"><span data-stu-id="a26ce-110">These event-handler routines usually have names of the form \**Will*Event\*\*\*.</span></span>

## <a name="complete-events"></a><span data-ttu-id="a26ce-111">Завершить событий</span><span class="sxs-lookup"><span data-stu-id="a26ce-111">Complete Events</span></span>

<span data-ttu-id="a26ce-112">Обработчики событий, вызывается после завершения операции может уведомлять приложение, которое предполагает операции.</span><span class="sxs-lookup"><span data-stu-id="a26ce-112">Event handlers called after an operation completes can notify your application that an operation has concluded.</span></span> <span data-ttu-id="a26ce-113">Такой обработчик событий также уведомления, когда обработчик события будет показано, как отменить ожидающие операции.</span><span class="sxs-lookup"><span data-stu-id="a26ce-113">Such an event handler is also notified when a Will event handler cancels a pending operation.</span></span> <span data-ttu-id="a26ce-114">Эти процедуры обработчика событий обычно есть имена формы \***событий \* полная**.</span><span class="sxs-lookup"><span data-stu-id="a26ce-114">These event-handler routines usually have names of the form \***Event\*Complete**.</span></span>

<span data-ttu-id="a26ce-115">Будет и завершения события обычно используются в пары.</span><span class="sxs-lookup"><span data-stu-id="a26ce-115">Will and Complete events are typically used in pairs.</span></span>

## <a name="other-events"></a><span data-ttu-id="a26ce-116">Другие события</span><span class="sxs-lookup"><span data-stu-id="a26ce-116">Other Events</span></span>

<span data-ttu-id="a26ce-117">Обработчики событий — то есть, события, чьи имена не формы **будет \* события**\* или \***событий \* полная —** вызываются только после завершения операции.</span><span class="sxs-lookup"><span data-stu-id="a26ce-117">The other event handlers — that is, events whose names are not of the form **Will\*Event**\* or \***Event\*Complete —** are called only after an operation completes.</span></span> <span data-ttu-id="a26ce-118">Эти события, **Отключение**, **EndOfRecordset**и **InfoMessage**.</span><span class="sxs-lookup"><span data-stu-id="a26ce-118">These events are **Disconnect**, **EndOfRecordset**, and **InfoMessage**.</span></span>

