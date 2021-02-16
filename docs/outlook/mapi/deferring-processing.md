---
title: Отложенная обработка
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
# <a name="deferring-processing"></a><span data-ttu-id="daab0-103">Отложенная обработка</span><span class="sxs-lookup"><span data-stu-id="daab0-103">Deferring Processing</span></span>

  
  
<span data-ttu-id="daab0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="daab0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="daab0-105">Передав флаг MAPI_DEFERRED_ERRORS методу, насколько это возможно.</span><span class="sxs-lookup"><span data-stu-id="daab0-105">Pass the MAPI_DEFERRED_ERRORS flag to method calls as much as possible.</span></span> <span data-ttu-id="daab0-106">Многие вызовы метода MAPI были оптимизированы для принятие этого флага, в результате чего поставщик либо откладывает запрашиваемую задачу, пока не будет выполнено несколько задач одновременно, либо вы больше не сможете дождаться результатов.</span><span class="sxs-lookup"><span data-stu-id="daab0-106">Many of the MAPI method calls have been optimized to accept this flag, causing the provider to either postpone the requested task until multiple tasks can be performed at once or you can wait no longer for the results.</span></span>
  
<span data-ttu-id="daab0-107">Например, если вы передаете MAPI_DEFERRED_ERRORS в [IMsgStore::OpenEntry](imsgstore-openentry.md) для открытия папки, открытие папки и возможного удаленного вызова можно отложить до вызова метода **GetHierarchyTable** или **GetProps** папки.</span><span class="sxs-lookup"><span data-stu-id="daab0-107">For example, if you pass MAPI_DEFERRED_ERRORS to [IMsgStore::OpenEntry](imsgstore-openentry.md) to open a folder, the opening of the folder and a possible remote call can be postponed until you make another call such as a call to the folder's **GetHierarchyTable** or **GetProps** methods.</span></span> <span data-ttu-id="daab0-108">Как **GetHierarchyTable,** так и **GetProps** требуют возврата данных от поставщика услуг, задачу, которую необходимо выполнить немедленно.</span><span class="sxs-lookup"><span data-stu-id="daab0-108">Both **GetHierarchyTable** and **GetProps** require the return of data from the service provider, a task that must be performed immediately.</span></span> 
  
<span data-ttu-id="daab0-109">Еще один способ отложить обработку — просто не делать вызов.</span><span class="sxs-lookup"><span data-stu-id="daab0-109">Another way to defer processing is simply not to make a call.</span></span> <span data-ttu-id="daab0-110">Зная пользователя и когда пользователь может воспринимать сток ресурсов или время обработки, вы можете определить, когда имеет смысл делать вызовы.</span><span class="sxs-lookup"><span data-stu-id="daab0-110">By being aware of the user and when the user can perceive a drain on resources or processing time, you can determine when it makes sense to make calls.</span></span> <span data-ttu-id="daab0-111">Существует возможность повысить производительность путем выполнения вызовов одновременно, когда пользователь не заметит или вообще не делает их.</span><span class="sxs-lookup"><span data-stu-id="daab0-111">There is an opportunity to improve performance by making calls either at a time when the user will not notice or by not making them at all.</span></span>
  
<span data-ttu-id="daab0-112">Например, рассмотрим ситуацию, когда вы получаете несколько уведомлений в секунду из большого количества сообщений в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="daab0-112">For example, consider the situation when you are receiving more than one notification per second from a message store that is moving a great number of messages.</span></span> <span data-ttu-id="daab0-113">Отображается индикатор хода выполнения, который указывает процент завершения операции.</span><span class="sxs-lookup"><span data-stu-id="daab0-113">A progress indicator is displayed to indicate the percentage of the operation's completion.</span></span> <span data-ttu-id="daab0-114">Как правило, пользователи не будут воспринимать эту операцию как медленную до тех пор, пока не пройдет несколько секунд.</span><span class="sxs-lookup"><span data-stu-id="daab0-114">Users typically will not perceive this operation to be slow until a few seconds have passed.</span></span> <span data-ttu-id="daab0-115">Поэтому при обновлении индикатора хода выполнения не внося никаких изменений по крайней мере через четыре секунды после начала операции перемещения.</span><span class="sxs-lookup"><span data-stu-id="daab0-115">Therefore, if you are updating the progress indicator, do not make any changes until at least four seconds after the initiation of the move operation.</span></span> <span data-ttu-id="daab0-116">Это экономит время в распространенных случаях, когда операция происходит быстро и своевременно информирует пользователей о медленной операции.</span><span class="sxs-lookup"><span data-stu-id="daab0-116">This will save time in the common cases when the operation is fast and inform users in a timely manner when the operation is slow.</span></span>
  

