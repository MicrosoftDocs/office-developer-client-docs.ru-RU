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
ms.openlocfilehash: 8f26fc6a51c3abdb4d4d009183fa8263ce97b261
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808258"
---
# <a name="deferring-processing"></a><span data-ttu-id="1cf8d-103">Откладывание обработки</span><span class="sxs-lookup"><span data-stu-id="1cf8d-103">Deferring Processing</span></span>

  
  
<span data-ttu-id="1cf8d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1cf8d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1cf8d-105">Передайте флаг MAPI_DEFERRED_ERRORS вызовы методов насколько это возможно.</span><span class="sxs-lookup"><span data-stu-id="1cf8d-105">Pass the MAPI_DEFERRED_ERRORS flag to method calls as much as possible.</span></span> <span data-ttu-id="1cf8d-106">Многие из вызовы методов интерфейса MAPI оптимизированные для принятия этот флаг, вызывающие поставщика либо откладывать запрошенную задачу до нескольких задач, которые могут выполняться одновременно или можно подождать больше не результаты.</span><span class="sxs-lookup"><span data-stu-id="1cf8d-106">Many of the MAPI method calls have been optimized to accept this flag, causing the provider to either postpone the requested task until multiple tasks can be performed at once or you can wait no longer for the results.</span></span>
  
<span data-ttu-id="1cf8d-107">К примеру Если передать MAPI_DEFERRED_ERRORS [IMsgStore::OpenEntry](imsgstore-openentry.md) , чтобы открыть папку, открывать папки и возможные удаленного вызова можно отложена, пока сделайте другой вызов, такие как звонок в папку **GetHierarchyTable** или ** GetProps** методы.</span><span class="sxs-lookup"><span data-stu-id="1cf8d-107">For example, if you pass MAPI_DEFERRED_ERRORS to [IMsgStore::OpenEntry](imsgstore-openentry.md) to open a folder, the opening of the folder and a possible remote call can be postponed until you make another call such as a call to the folder's **GetHierarchyTable** or **GetProps** methods.</span></span> <span data-ttu-id="1cf8d-108">**GetHierarchyTable** и **GetProps** требуется возврат данных от поставщика услуг, задача, которая должна быть выполнена немедленно.</span><span class="sxs-lookup"><span data-stu-id="1cf8d-108">Both **GetHierarchyTable** and **GetProps** require the return of data from the service provider, a task that must be performed immediately.</span></span> 
  
<span data-ttu-id="1cf8d-109">Другой способ отложить обработку — просто не звонок.</span><span class="sxs-lookup"><span data-stu-id="1cf8d-109">Another way to defer processing is simply not to make a call.</span></span> <span data-ttu-id="1cf8d-110">Знание пользователя и когда пользователь воспринимает затрат на ресурсы или время обработки, можно определить, если это имеет смысл выполнять вызовы.</span><span class="sxs-lookup"><span data-stu-id="1cf8d-110">By being aware of the user and when the user can perceive a drain on resources or processing time, you can determine when it makes sense to make calls.</span></span> <span data-ttu-id="1cf8d-111">Существует возможность повышения производительности путем вызова либо во время, когда пользователь не заметить, или, не делая их вообще.</span><span class="sxs-lookup"><span data-stu-id="1cf8d-111">There is an opportunity to improve performance by making calls either at a time when the user will not notice or by not making them at all.</span></span>
  
<span data-ttu-id="1cf8d-112">Например рассмотрим ситуацию при получении нескольких уведомлений в секунду в магазине сообщения, переместить большого числа сообщений.</span><span class="sxs-lookup"><span data-stu-id="1cf8d-112">For example, consider the situation when you are receiving more than one notification per second from a message store that is moving a great number of messages.</span></span> <span data-ttu-id="1cf8d-113">Чтобы указать процент выполнения операции отображается индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="1cf8d-113">A progress indicator is displayed to indicate the percentage of the operation's completion.</span></span> <span data-ttu-id="1cf8d-114">Обычно пользователи будут не воспринимают эту операцию, чтобы быть медленным, пока не несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="1cf8d-114">Users typically will not perceive this operation to be slow until a few seconds have passed.</span></span> <span data-ttu-id="1cf8d-115">Таким образом при выполнении обновления индикатор хода выполнения, не вносите никаких изменений до по крайней мере четыре секунд после запуска операции перемещения.</span><span class="sxs-lookup"><span data-stu-id="1cf8d-115">Therefore, if you are updating the progress indicator, do not make any changes until at least four seconds after the initiation of the move operation.</span></span> <span data-ttu-id="1cf8d-116">Это экономия времени в общем случае при быстром операции и информирование пользователей своевременно при слишком медленно.</span><span class="sxs-lookup"><span data-stu-id="1cf8d-116">This will save time in the common cases when the operation is fast and inform users in a timely manner when the operation is slow.</span></span>
  

