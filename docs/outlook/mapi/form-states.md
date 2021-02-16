---
title: Состояния форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 61d20ff7010151a82c53cafc69270e6925796a5c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429168"
---
# <a name="form-states"></a><span data-ttu-id="8e4d2-103">Состояния форм</span><span class="sxs-lookup"><span data-stu-id="8e4d2-103">Form states</span></span>

<span data-ttu-id="8e4d2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e4d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e4d2-105">Объекты форм могут быть в одном из пяти различных состояниях в зависимости от того, какие методы были вызваны в них и произошли ли ошибки при выполнении этих методов.</span><span class="sxs-lookup"><span data-stu-id="8e4d2-105">Form objects can be in one of five distinct states, depending on what methods have been called in them and whether any errors have occurred in performing those methods.</span></span> <span data-ttu-id="8e4d2-106">Состояния описаны в следующих темах:</span><span class="sxs-lookup"><span data-stu-id="8e4d2-106">The states are described in the following topics:</span></span>
  
- [<span data-ttu-id="8e4d2-107">Неинициализированное состояние</span><span class="sxs-lookup"><span data-stu-id="8e4d2-107">Uninitialized State</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="8e4d2-108">Нормальное состояние</span><span class="sxs-lookup"><span data-stu-id="8e4d2-108">Normal State</span></span>](normal-state.md)
    
- [<span data-ttu-id="8e4d2-109">Состояние NoScribble</span><span class="sxs-lookup"><span data-stu-id="8e4d2-109">NoScribble State</span></span>](noscribble-state.md)
    
- [<span data-ttu-id="8e4d2-110">Состояние HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="8e4d2-110">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="8e4d2-111">HandsOffFromNormal State</span><span class="sxs-lookup"><span data-stu-id="8e4d2-111">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="8e4d2-112">Состояния в основном связаны со статусом данных в объекте формы.</span><span class="sxs-lookup"><span data-stu-id="8e4d2-112">The states primarily relate to the status of the data in the form object.</span></span> <span data-ttu-id="8e4d2-113">Различные состояния отражают, нужно ли сохранять данные, должен ли объект формы вносить изменения в данные и в какой момент сохранять данные, в которые находится форма.</span><span class="sxs-lookup"><span data-stu-id="8e4d2-113">The different states reflect whether the data needs to be saved, whether the form object should allow modifications to the data, and what point in the process of saving the data the form is in.</span></span> <span data-ttu-id="8e4d2-114">Поэтому состояния форм и переходы между ними имеют большее отношения с реализацией [IPersistMessage на](ipersistmessageiunknown.md) сервере форм: методы интерфейса IUnknown, чем любые другие.</span><span class="sxs-lookup"><span data-stu-id="8e4d2-114">As such, the form states and transitions between them have more to do with your form server's implementation of [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interface methods than any other.</span></span> <span data-ttu-id="8e4d2-115">Знание этих состояния очень полезно для правильной реализации интерфейсов форм MAPI, которые должен реализовать сервер форм.</span><span class="sxs-lookup"><span data-stu-id="8e4d2-115">Knowledge of these states is very useful for proper implementation of the MAPI form interfaces that your form server must implement.</span></span> 
  
<span data-ttu-id="8e4d2-116">В темах этого раздела описываются различные состояния, а также разрешенные действия, которые приводят к переходу на другие состояния.</span><span class="sxs-lookup"><span data-stu-id="8e4d2-116">The topics in this section describe the various states, along with the allowed actions that cause transitions to other states.</span></span> <span data-ttu-id="8e4d2-117">Любые переходы, не указанные в темах, не разрешены.</span><span class="sxs-lookup"><span data-stu-id="8e4d2-117">Any transitions not listed in the topics are not allowed.</span></span> <span data-ttu-id="8e4d2-118">Если объекты формы делают неопредустановимые переходы между состояниями, они не будут вести себя так, как ожидают клиенты обмена сообщениями, и это может привести к непредсказуемому поведению клиента или объекта формы.</span><span class="sxs-lookup"><span data-stu-id="8e4d2-118">If your form objects make disallowed transitions between states, they will not behave in the ways that messaging clients expect and could cause unpredictable client or form object behavior.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8e4d2-119">Некоторые переходы состояния зависят от сведений из предыдущих.</span><span class="sxs-lookup"><span data-stu-id="8e4d2-119">Some state transitions depend on information from previous states.</span></span> <span data-ttu-id="8e4d2-120">Скорее всего, серверу форм придется реализовать флаг в своих объектах формы, чтобы указать, были ли изменены значения свойств сообщения для упрощения последующих изменений состояния.</span><span class="sxs-lookup"><span data-stu-id="8e4d2-120">Your form server will most likely have to implement a flag in its form objects to indicate whether the values of the message's properties have been changed to facilitate later state changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8e4d2-121">См. также</span><span class="sxs-lookup"><span data-stu-id="8e4d2-121">See also</span></span>

- [<span data-ttu-id="8e4d2-122">Разработка серверов форм MAPI</span><span class="sxs-lookup"><span data-stu-id="8e4d2-122">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

