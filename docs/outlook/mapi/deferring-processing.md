---
title: Откладывание обработки
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
# <a name="deferring-processing"></a><span data-ttu-id="814f5-103">Откладывание обработки</span><span class="sxs-lookup"><span data-stu-id="814f5-103">Deferring Processing</span></span>

  
  
<span data-ttu-id="814f5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="814f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="814f5-105">Передайте MAPI_DEFERRED_ERRORSный флаг вызовам методов максимально возможной.</span><span class="sxs-lookup"><span data-stu-id="814f5-105">Pass the MAPI_DEFERRED_ERRORS flag to method calls as much as possible.</span></span> <span data-ttu-id="814f5-106">Многие из вызовов метода MAPI были оптимизированы для принятия этого флага, что приводит к тому, что поставщик откладывает запрошенную задачу до тех пор, пока не сможете выполнить несколько задач одновременно или подождать, пока не будет достигнуто больше результатов.</span><span class="sxs-lookup"><span data-stu-id="814f5-106">Many of the MAPI method calls have been optimized to accept this flag, causing the provider to either postpone the requested task until multiple tasks can be performed at once or you can wait no longer for the results.</span></span>
  
<span data-ttu-id="814f5-107">Например, если вы передаете MAPI_DEFERRED_ERRORS [IMsgStore:: OpenEntry](imsgstore-openentry.md) для открытия папки, открытие папки и возможного удаленного вызова можно отложить, пока не будет вызван другой вызов, такой как вызов методов **жесиерарчитабле** и **PROPS** папки.</span><span class="sxs-lookup"><span data-stu-id="814f5-107">For example, if you pass MAPI_DEFERRED_ERRORS to [IMsgStore::OpenEntry](imsgstore-openentry.md) to open a folder, the opening of the folder and a possible remote call can be postponed until you make another call such as a call to the folder's **GetHierarchyTable** or **GetProps** methods.</span></span> <span data-ttu-id="814f5-108">Как **жесиерарчитабле** , так и **PROPS** требуют возврата данных от поставщика услуг — задачи, которую необходимо выполнить немедленно.</span><span class="sxs-lookup"><span data-stu-id="814f5-108">Both **GetHierarchyTable** and **GetProps** require the return of data from the service provider, a task that must be performed immediately.</span></span> 
  
<span data-ttu-id="814f5-109">Другой способ отложить обработку — просто не совершать вызов.</span><span class="sxs-lookup"><span data-stu-id="814f5-109">Another way to defer processing is simply not to make a call.</span></span> <span data-ttu-id="814f5-110">С учетом пользователя и когда пользователь может воспринимать сток ресурсов или время обработки, вы можете определить, когда имеет смысл совершить звонки.</span><span class="sxs-lookup"><span data-stu-id="814f5-110">By being aware of the user and when the user can perceive a drain on resources or processing time, you can determine when it makes sense to make calls.</span></span> <span data-ttu-id="814f5-111">Вы можете увеличить производительность, выполнив звонки в любое время, когда пользователь не будет уведомлен или не сделает их вообще.</span><span class="sxs-lookup"><span data-stu-id="814f5-111">There is an opportunity to improve performance by making calls either at a time when the user will not notice or by not making them at all.</span></span>
  
<span data-ttu-id="814f5-112">Например, рассмотрим ситуацию, когда вы получаете более одного уведомления в секунду из хранилища сообщений, которое перемещает очень много сообщений.</span><span class="sxs-lookup"><span data-stu-id="814f5-112">For example, consider the situation when you are receiving more than one notification per second from a message store that is moving a great number of messages.</span></span> <span data-ttu-id="814f5-113">Отображается индикатор выполнения, указывающий процент завершения операции.</span><span class="sxs-lookup"><span data-stu-id="814f5-113">A progress indicator is displayed to indicate the percentage of the operation's completion.</span></span> <span data-ttu-id="814f5-114">Обычно пользователи не будут воспринимать эту операцию до тех пор, пока не будет пройдено несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="814f5-114">Users typically will not perceive this operation to be slow until a few seconds have passed.</span></span> <span data-ttu-id="814f5-115">Таким образом, если вы обновляете индикатор хода выполнения, не вносите никаких изменений в течение не менее четырех секунд после запуска операции перемещения.</span><span class="sxs-lookup"><span data-stu-id="814f5-115">Therefore, if you are updating the progress indicator, do not make any changes until at least four seconds after the initiation of the move operation.</span></span> <span data-ttu-id="814f5-116">Это экономит время в общих случаях, когда операция выполняется быстро и своевременно проинформирует пользователей о медленной работе.</span><span class="sxs-lookup"><span data-stu-id="814f5-116">This will save time in the common cases when the operation is fast and inform users in a timely manner when the operation is slow.</span></span>
  

