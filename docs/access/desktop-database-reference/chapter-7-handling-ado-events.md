---
title: 'Глава 7: Обработка событий ADO'
TOCTitle: 'Chapter 7: Handling ADO Events'
ms:assetid: 22924fe2-d00d-8a0c-52f5-2dc6039537ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249004(v=office.15)
ms:contentKeyID: 48543709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 816dd98e5e4c21f3159edf18b5687b2b0578e399
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860842"
---
# <a name="chapter-7-handling-ado-events"></a><span data-ttu-id="faaf8-102">Глава 7: Обработка событий ADO</span><span class="sxs-lookup"><span data-stu-id="faaf8-102">Chapter 7: Handling ADO Events</span></span>


<span data-ttu-id="faaf8-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="faaf8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="faaf8-104">Модель событий ADO поддерживает некоторые операции ADO синхронная и асинхронная, заключать *событий*или уведомлений, до начала операции или после его завершения.</span><span class="sxs-lookup"><span data-stu-id="faaf8-104">The ADO event model supports certain synchronous and asynchronous ADO operations that issue *events*, or notifications, before the operation starts or after it completes.</span></span> <span data-ttu-id="faaf8-105">Событие — вызов процедуры обработчика событий, которые определены в приложении.</span><span class="sxs-lookup"><span data-stu-id="faaf8-105">An event is actually a call to an event-handler routine that you define in your application.</span></span>

<span data-ttu-id="faaf8-106">Если предоставляет функции обработчика или процедуры для группы события, произошедшие до начала операции, вы можете проверить или изменить параметры, которые были переданы операции.</span><span class="sxs-lookup"><span data-stu-id="faaf8-106">If you provide handler functions or procedures for the group of events that occur before the operation starts, you can examine or modify the parameters that were passed to the operation.</span></span> <span data-ttu-id="faaf8-107">Так как он не был выполнен еще, можно отменить операцию или разрешить его завершения.</span><span class="sxs-lookup"><span data-stu-id="faaf8-107">Because it has not been executed yet, you can either cancel the operation or allow it to complete.</span></span>

<span data-ttu-id="faaf8-108">Группа события, происходящие после завершения операции, особенно важно при использовании ADO асинхронно.</span><span class="sxs-lookup"><span data-stu-id="faaf8-108">The group of events that occur after an operation completes are especially important if you use ADO asynchronously.</span></span> <span data-ttu-id="faaf8-109">Например приложение, которое запускает операцию асинхронного [Recordset.Open](open-method-ado-recordset.md) уведомление по событие завершения выполнения при завершает операцию.</span><span class="sxs-lookup"><span data-stu-id="faaf8-109">For example, an application that starts an asynchronous [Recordset.Open](open-method-ado-recordset.md) operation is notified by an execution complete event when the operation concludes.</span></span>

<span data-ttu-id="faaf8-110">С помощью модели событий ADO добавляет определенная дополнительная нагрузка на приложение, но обеспечивает гораздо большее число гибкость, чем другие методы работы с асинхронной операции, такие как мониторинг [состояния](state-property-ado.md) свойства объекта с помощью цикла.</span><span class="sxs-lookup"><span data-stu-id="faaf8-110">Using the ADO event model adds some overhead to your application but provides far more flexibility than other methods of dealing with asynchronous operations, such as monitoring the [State](state-property-ado.md) property of an object with a loop.</span></span>

<span data-ttu-id="faaf8-111">В этой главе рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="faaf8-111">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="faaf8-112">Сводка по обработчикам событий ADO</span><span class="sxs-lookup"><span data-stu-id="faaf8-112">ADO Event Handler Summary</span></span>](ado-event-handler-summary.md)

- [<span data-ttu-id="faaf8-113">Типы событий</span><span class="sxs-lookup"><span data-stu-id="faaf8-113">Types of Events</span></span>](types-of-events.md)

- [<span data-ttu-id="faaf8-114">Параметры событий</span><span class="sxs-lookup"><span data-stu-id="faaf8-114">Event Parameters</span></span>](event-parameters.md)

- [<span data-ttu-id="faaf8-115">Как обработчики событий совместно действуют</span><span class="sxs-lookup"><span data-stu-id="faaf8-115">How Event Handlers Work Together</span></span>](how-event-handlers-work-together.md)

- [<span data-ttu-id="faaf8-116">ADO Event Instantiation by Language (ADO)</span><span class="sxs-lookup"><span data-stu-id="faaf8-116">ADO Event Instantiation by Language (ADO)</span></span>](ado-event-instantiation-by-language-ado.md)