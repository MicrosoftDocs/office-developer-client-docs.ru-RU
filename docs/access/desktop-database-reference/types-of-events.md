---
title: Типы событий (Справочник по базам данных Access на компьютере)
TOCTitle: Types of Events
ms:assetid: 94660fc1-65c3-1d21-c451-f3898014e0b6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249660(v=office.15)
ms:contentKeyID: 48546414
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3bcf631ffc6c9b4b847af3f973114d6b271d26f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314156"
---
# <a name="types-of-events"></a><span data-ttu-id="c08a1-102">Типы событий</span><span class="sxs-lookup"><span data-stu-id="c08a1-102">Types of events</span></span>


<span data-ttu-id="c08a1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c08a1-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="c08a1-104">Существует два основных типа событий.</span><span class="sxs-lookup"><span data-stu-id="c08a1-104">There are two basic types of events.</span></span> <span data-ttu-id="c08a1-105">"События будут вызываться до начала операции, как правило, включают" будет "в своих именах, например **события willchangerecordset** или **событие willconnect**.</span><span class="sxs-lookup"><span data-stu-id="c08a1-105">"Will Events," which are called before an operation starts, usually include "Will" in their names — for example, **WillChangeRecordset** or **WillConnect**.</span></span> <span data-ttu-id="c08a1-106">События, которые вызываются после завершения события, обычно включают слово "завершено" в своих именах, например **RecordChangeComplete** или **события connectcomplete**.</span><span class="sxs-lookup"><span data-stu-id="c08a1-106">Events that are called after an event has been completed usually include "Complete" in their names — for example, **RecordChangeComplete** or **ConnectComplete**.</span></span> <span data-ttu-id="c08a1-107">Существуют исключения, такие как **InfoMessage** , но они происходят после завершения связанной операции.</span><span class="sxs-lookup"><span data-stu-id="c08a1-107">Exceptions exist — such as **InfoMessage** — but these occur after the associated operation has completed.</span></span>

## <a name="will-events"></a><span data-ttu-id="c08a1-108">События будут</span><span class="sxs-lookup"><span data-stu-id="c08a1-108">Will Events</span></span>

<span data-ttu-id="c08a1-109">Обработчики событий, вызванные до начала операции, предоставляют возможность проверить или изменить параметры операции, а затем либо отменить операцию, либо разрешить ее выполнение.</span><span class="sxs-lookup"><span data-stu-id="c08a1-109">Event handlers called before the operation starts offer you the opportunity to examine or modify the operation parameters, and then either cancel the operation or allow it to complete.</span></span> <span data-ttu-id="c08a1-110">Эти процедуры обработчиков событий, как правило, имеют имена для формы\*\*\* — событие \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="c08a1-110">These event-handler routines usually have names of the form \**Will*Event\*\*\*.</span></span>

## <a name="complete-events"></a><span data-ttu-id="c08a1-111">События завершения</span><span class="sxs-lookup"><span data-stu-id="c08a1-111">Complete Events</span></span>

<span data-ttu-id="c08a1-112">Обработчики событий, вызванные после завершения операции, могут уведомлять приложение о том, что операция завершена.</span><span class="sxs-lookup"><span data-stu-id="c08a1-112">Event handlers called after an operation completes can notify your application that an operation has concluded.</span></span> <span data-ttu-id="c08a1-113">Такой обработчик событий также уведомляется, когда обработчик событий будет отменять отложенную операцию.</span><span class="sxs-lookup"><span data-stu-id="c08a1-113">Such an event handler is also notified when a Will event handler cancels a pending operation.</span></span> <span data-ttu-id="c08a1-114">Эти процедуры обработчиков событий, как правило, имеют имена вида \***event \* Complete**.</span><span class="sxs-lookup"><span data-stu-id="c08a1-114">These event-handler routines usually have names of the form \***Event\*Complete**.</span></span>

<span data-ttu-id="c08a1-115">События "будет" и "Готово" обычно используются парами.</span><span class="sxs-lookup"><span data-stu-id="c08a1-115">Will and Complete events are typically used in pairs.</span></span>

## <a name="other-events"></a><span data-ttu-id="c08a1-116">Другие события</span><span class="sxs-lookup"><span data-stu-id="c08a1-116">Other Events</span></span>

<span data-ttu-id="c08a1-117">Другие обработчики событий, то есть события, имена которых не являются формами \*\*\* event\*\*\* и \***Complete,** вызываются только после завершения операции.</span><span class="sxs-lookup"><span data-stu-id="c08a1-117">The other event handlers — that is, events whose names are not of the form **Will\*Event**\* or \***Event\*Complete —** are called only after an operation completes.</span></span> <span data-ttu-id="c08a1-118">Эти события отКлючаются, **событие endofrecordset**и **InfoMessage**. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c08a1-118">These events are **Disconnect**, **EndOfRecordset**, and **InfoMessage**.</span></span>

