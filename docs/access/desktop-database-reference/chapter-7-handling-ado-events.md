---
title: 'Chapter 7: Handling ADO Events'
TOCTitle: 'Chapter 7: Handling ADO Events'
ms:assetid: 22924fe2-d00d-8a0c-52f5-2dc6039537ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249004(v=office.15)
ms:contentKeyID: 48543709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d85532c93c6d175b90f957d7831b71a460ba5b6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482434"
---
# <a name="chapter-7-handling-ado-events"></a><span data-ttu-id="33a2f-102">Chapter 7: Handling ADO Events</span><span class="sxs-lookup"><span data-stu-id="33a2f-102">Chapter 7: Handling ADO Events</span></span>


<span data-ttu-id="33a2f-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="33a2f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="33a2f-104">Модель событий ADO поддерживает некоторые операции ADO синхронная и асинхронная, заключать *событий*или уведомлений, до начала операции или после его завершения.</span><span class="sxs-lookup"><span data-stu-id="33a2f-104">The ADO event model supports certain synchronous and asynchronous ADO operations that issue *events*, or notifications, before the operation starts or after it completes.</span></span> <span data-ttu-id="33a2f-105">Событие — вызов процедуры обработчика событий, которые определены в приложении.</span><span class="sxs-lookup"><span data-stu-id="33a2f-105">An event is actually a call to an event-handler routine that you define in your application.</span></span>

<span data-ttu-id="33a2f-106">Если предоставляет функции обработчика или процедуры для группы события, произошедшие до начала операции, вы можете проверить или изменить параметры, которые были переданы операции.</span><span class="sxs-lookup"><span data-stu-id="33a2f-106">If you provide handler functions or procedures for the group of events that occur before the operation starts, you can examine or modify the parameters that were passed to the operation.</span></span> <span data-ttu-id="33a2f-107">Так как он не был выполнен еще, можно отменить операцию или разрешить его завершения.</span><span class="sxs-lookup"><span data-stu-id="33a2f-107">Because it has not been executed yet, you can either cancel the operation or allow it to complete.</span></span>

<span data-ttu-id="33a2f-108">Группа события, происходящие после завершения операции, особенно важно при использовании ADO асинхронно.</span><span class="sxs-lookup"><span data-stu-id="33a2f-108">The group of events that occur after an operation completes are especially important if you use ADO asynchronously.</span></span> <span data-ttu-id="33a2f-109">Например приложение, которое запускает операцию асинхронного [Recordset.Open](open-method-ado-recordset.md) уведомление по событие завершения выполнения при завершает операцию.</span><span class="sxs-lookup"><span data-stu-id="33a2f-109">For example, an application that starts an asynchronous [Recordset.Open](open-method-ado-recordset.md) operation is notified by an execution complete event when the operation concludes.</span></span>

<span data-ttu-id="33a2f-110">С помощью модели событий ADO добавляет определенная дополнительная нагрузка на приложение, но обеспечивает гораздо большее число гибкость, чем другие методы работы с асинхронной операции, такие как мониторинг [состояния](state-property-ado.md) свойства объекта с помощью цикла.</span><span class="sxs-lookup"><span data-stu-id="33a2f-110">Using the ADO event model adds some overhead to your application but provides far more flexibility than other methods of dealing with asynchronous operations, such as monitoring the [State](state-property-ado.md) property of an object with a loop.</span></span>

