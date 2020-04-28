---
title: Глава 7. Обработка событий ADO
TOCTitle: 'Chapter 7: Handling ADO events'
ms:assetid: 22924fe2-d00d-8a0c-52f5-2dc6039537ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249004(v=office.15)
ms:contentKeyID: 48543709
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e7357cc60a3bddbf96c2abae39fecfb7107025e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296404"
---
# <a name="chapter-7-handling-ado-events"></a><span data-ttu-id="276a3-102">Глава 7. Обработка событий ADO</span><span class="sxs-lookup"><span data-stu-id="276a3-102">Chapter 7: Handling ADO events</span></span>

<span data-ttu-id="276a3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="276a3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="276a3-104">Модель событий ADO поддерживает определенные синхронные и асинхронные операции ADO, которые выдают *события*или уведомления, прежде чем операция начнется или после ее завершения.</span><span class="sxs-lookup"><span data-stu-id="276a3-104">The ADO event model supports certain synchronous and asynchronous ADO operations that issue *events*, or notifications, before the operation starts or after it completes.</span></span> <span data-ttu-id="276a3-105">Событие фактически является вызовом процедуры обработчика событий, определенной в приложении.</span><span class="sxs-lookup"><span data-stu-id="276a3-105">An event is actually a call to an event-handler routine that you define in your application.</span></span>

<span data-ttu-id="276a3-106">Если вы предоставляете функции или процедуры обработчика для группы событий, которые происходят до начала операции, вы можете проверить или изменить параметры, которые были переданы в операцию.</span><span class="sxs-lookup"><span data-stu-id="276a3-106">If you provide handler functions or procedures for the group of events that occur before the operation starts, you can examine or modify the parameters that were passed to the operation.</span></span> <span data-ttu-id="276a3-107">Так как он еще не был выполнен, вы можете отменить операцию или разрешить ее выполнение.</span><span class="sxs-lookup"><span data-stu-id="276a3-107">Because it has not been executed yet, you can either cancel the operation or allow it to complete.</span></span>

<span data-ttu-id="276a3-108">Группа событий, возникающих после завершения операции, особенно важна, если вы используете ADO асинхронно.</span><span class="sxs-lookup"><span data-stu-id="276a3-108">The group of events that occur after an operation completes are especially important if you use ADO asynchronously.</span></span> <span data-ttu-id="276a3-109">Например, приложение, запускающее асинхронный [набор записей. операция открытия](open-method-ado-recordset.md) получает уведомление о завершении выполнения операции, когда завершается операция.</span><span class="sxs-lookup"><span data-stu-id="276a3-109">For example, an application that starts an asynchronous [Recordset.Open](open-method-ado-recordset.md) operation is notified by an execution complete event when the operation concludes.</span></span>

<span data-ttu-id="276a3-110">С помощью модели событий ADO к приложению добавляется дополнительная нагрузка, но обеспечивается гораздо большую гибкость, чем другие методы работы с асинхронными операциями, например отслеживание свойства [State](state-property-ado.md) объекта с циклом.</span><span class="sxs-lookup"><span data-stu-id="276a3-110">Using the ADO event model adds some overhead to your application but provides far more flexibility than other methods of dealing with asynchronous operations, such as monitoring the [State](state-property-ado.md) property of an object with a loop.</span></span>

<span data-ttu-id="276a3-111">В этой главе рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="276a3-111">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="276a3-112">Сводка по обработчикам событий ADO</span><span class="sxs-lookup"><span data-stu-id="276a3-112">ADO event handler summary</span></span>](ado-event-handler-summary.md)
- [<span data-ttu-id="276a3-113">Типы событий</span><span class="sxs-lookup"><span data-stu-id="276a3-113">Types of events</span></span>](types-of-events.md)
- [<span data-ttu-id="276a3-114">Параметры событий</span><span class="sxs-lookup"><span data-stu-id="276a3-114">Event parameters</span></span>](event-parameters.md)
- [<span data-ttu-id="276a3-115">Взаимодействие обработчиков событий</span><span class="sxs-lookup"><span data-stu-id="276a3-115">How event handlers work together</span></span>](how-event-handlers-work-together.md)
- [<span data-ttu-id="276a3-116">Создание экземпляра события ADO по языку (ADO)</span><span class="sxs-lookup"><span data-stu-id="276a3-116">ADO event instantiation by language (ADO)</span></span>](ado-event-instantiation-by-language-ado.md)
