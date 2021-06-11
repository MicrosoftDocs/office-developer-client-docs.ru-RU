---
title: Отсрочка обработки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2d3fbf8f7a725f121579066001715fb0bc6beba0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430933"
---
# <a name="deferring-processing"></a><span data-ttu-id="464c7-103">Отсрочка обработки</span><span class="sxs-lookup"><span data-stu-id="464c7-103">Deferring Processing</span></span>

  
  
<span data-ttu-id="464c7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="464c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="464c7-105">Передай флаг MAPI_DEFERRED_ERRORS методу как можно больше вызовов.</span><span class="sxs-lookup"><span data-stu-id="464c7-105">Pass the MAPI_DEFERRED_ERRORS flag to method calls as much as possible.</span></span> <span data-ttu-id="464c7-106">Многие вызовы метода MAPI были оптимизированы для того, чтобы принять этот флаг, в результате чего поставщик либо откладывает запрашиваемую задачу, пока не будет выполнено сразу несколько задач, либо вы не сможете дождаться результатов.</span><span class="sxs-lookup"><span data-stu-id="464c7-106">Many of the MAPI method calls have been optimized to accept this flag, causing the provider to either postpone the requested task until multiple tasks can be performed at once or you can wait no longer for the results.</span></span>
  
<span data-ttu-id="464c7-107">Например, если вы MAPI_DEFERRED_ERRORS [iMsgStore::OpenEntry](imsgstore-openentry.md) для открытия папки, открытие папки и возможный удаленный вызов могут быть отложены до тех пор, пока вы не сделаете еще один вызов, например вызов в **методы GetHierarchyTable** папки или **GetProps.**</span><span class="sxs-lookup"><span data-stu-id="464c7-107">For example, if you pass MAPI_DEFERRED_ERRORS to [IMsgStore::OpenEntry](imsgstore-openentry.md) to open a folder, the opening of the folder and a possible remote call can be postponed until you make another call such as a call to the folder's **GetHierarchyTable** or **GetProps** methods.</span></span> <span data-ttu-id="464c7-108">Как **GetHierarchyTable,** так и **GetProps** требуют возврата данных от поставщика услуг, задачу, которую необходимо выполнить немедленно.</span><span class="sxs-lookup"><span data-stu-id="464c7-108">Both **GetHierarchyTable** and **GetProps** require the return of data from the service provider, a task that must be performed immediately.</span></span> 
  
<span data-ttu-id="464c7-109">Другой способ отложить обработку — просто не делать вызов.</span><span class="sxs-lookup"><span data-stu-id="464c7-109">Another way to defer processing is simply not to make a call.</span></span> <span data-ttu-id="464c7-110">Будучи в курсе пользователя и когда пользователь может воспринимать утечку ресурсов или время обработки, вы можете определить, когда имеет смысл делать вызовы.</span><span class="sxs-lookup"><span data-stu-id="464c7-110">By being aware of the user and when the user can perceive a drain on resources or processing time, you can determine when it makes sense to make calls.</span></span> <span data-ttu-id="464c7-111">Существует возможность повысить производительность, делая вызовы либо в то время, когда пользователь не заметит или не делает их вообще.</span><span class="sxs-lookup"><span data-stu-id="464c7-111">There is an opportunity to improve performance by making calls either at a time when the user will not notice or by not making them at all.</span></span>
  
<span data-ttu-id="464c7-112">Например, рассмотрим ситуацию, когда вы получаете более одного уведомления в секунду из магазина сообщений, который перемещает большое количество сообщений.</span><span class="sxs-lookup"><span data-stu-id="464c7-112">For example, consider the situation when you are receiving more than one notification per second from a message store that is moving a great number of messages.</span></span> <span data-ttu-id="464c7-113">Отображается индикатор прогресса, который указывает процент завершения операции.</span><span class="sxs-lookup"><span data-stu-id="464c7-113">A progress indicator is displayed to indicate the percentage of the operation's completion.</span></span> <span data-ttu-id="464c7-114">Обычно пользователи не будут воспринимать эту операцию медленно, пока не пройдет несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="464c7-114">Users typically will not perceive this operation to be slow until a few seconds have passed.</span></span> <span data-ttu-id="464c7-115">Поэтому, если вы обновляете индикатор прогресса, не внося изменений по крайней мере через четыре секунды после начала операции перемещения.</span><span class="sxs-lookup"><span data-stu-id="464c7-115">Therefore, if you are updating the progress indicator, do not make any changes until at least four seconds after the initiation of the move operation.</span></span> <span data-ttu-id="464c7-116">Это позволит сэкономить время в распространенных случаях, когда операция будет быстрой и своевременно информировать пользователей, когда операция медленна.</span><span class="sxs-lookup"><span data-stu-id="464c7-116">This will save time in the common cases when the operation is fast and inform users in a timely manner when the operation is slow.</span></span>
  

