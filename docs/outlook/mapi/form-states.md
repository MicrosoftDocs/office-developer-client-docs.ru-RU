---
title: Состояния формы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dfc9fbf1-90d4-4756-92d9-032ac56a9c50
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 969aca6fd37f237a607df36cc58f249828449e27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808503"
---
# <a name="form-states"></a><span data-ttu-id="06028-103">Состояния формы</span><span class="sxs-lookup"><span data-stu-id="06028-103">Form states</span></span>

<span data-ttu-id="06028-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="06028-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="06028-105">Объекты формы может быть в одном из пяти различных состояний, в зависимости от того, какие методы вызова в них и ли наличие ошибок при выполнении этих методов.</span><span class="sxs-lookup"><span data-stu-id="06028-105">Form objects can be in one of five distinct states, depending on what methods have been called in them and whether any errors have occurred in performing those methods.</span></span> <span data-ttu-id="06028-106">В следующих разделах описаны состояния.</span><span class="sxs-lookup"><span data-stu-id="06028-106">The states are described in the following topics:</span></span>
  
- [<span data-ttu-id="06028-107">Неинициализированная переменная состояния</span><span class="sxs-lookup"><span data-stu-id="06028-107">Uninitialized State</span></span>](uninitialized-state.md)
    
- [<span data-ttu-id="06028-108">Состояние Normal</span><span class="sxs-lookup"><span data-stu-id="06028-108">Normal State</span></span>](normal-state.md)
    
- [<span data-ttu-id="06028-109">Состояние NoScribble</span><span class="sxs-lookup"><span data-stu-id="06028-109">NoScribble State</span></span>](noscribble-state.md)
    
- [<span data-ttu-id="06028-110">Состояние HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="06028-110">HandsOffAfterSave State</span></span>](handsoffaftersave-state.md)
    
- [<span data-ttu-id="06028-111">Состояние HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="06028-111">HandsOffFromNormal State</span></span>](handsofffromnormal-state.md)
    
<span data-ttu-id="06028-112">Состояния главным образом относятся состояние данных в объекте формы.</span><span class="sxs-lookup"><span data-stu-id="06028-112">The states primarily relate to the status of the data in the form object.</span></span> <span data-ttu-id="06028-113">Различные состояния отражают ли данные необходимо сохранить, является ли объект формы, должна поддерживать изменения данных и какой момент в процессе сохранения данных, которые форма находится в.</span><span class="sxs-lookup"><span data-stu-id="06028-113">The different states reflect whether the data needs to be saved, whether the form object should allow modifications to the data, and what point in the process of saving the data the form is in.</span></span> <span data-ttu-id="06028-114">Таким образом, форма состояния и переходы между ними имеют с реализацией сервера форм [IPersistMessage: IUnknown](ipersistmessageiunknown.md) интерфейс методов, чем другие.</span><span class="sxs-lookup"><span data-stu-id="06028-114">As such, the form states and transitions between them have more to do with your form server's implementation of [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interface methods than any other.</span></span> <span data-ttu-id="06028-115">Знаний из следующих состояний очень полезен для правильной реализации интерфейсов формы MAPI, которые необходимо реализовать сервер формы.</span><span class="sxs-lookup"><span data-stu-id="06028-115">Knowledge of these states is very useful for proper implementation of the MAPI form interfaces that your form server must implement.</span></span> 
  
<span data-ttu-id="06028-116">В этом разделе описываются различные состояния, а также разрешенные действия, которые вызывают преобразований в другие состояния.</span><span class="sxs-lookup"><span data-stu-id="06028-116">The topics in this section describe the various states, along with the allowed actions that cause transitions to other states.</span></span> <span data-ttu-id="06028-117">Любые переходы, не указанные в разделах не разрешены.</span><span class="sxs-lookup"><span data-stu-id="06028-117">Any transitions not listed in the topics are not allowed.</span></span> <span data-ttu-id="06028-118">Если объекты формы внесены недопустимые переходы между состояниями, они вести себя способами, что клиенты обмена сообщениями согласно прогнозу и может привести к непредвиденному поведению объекта клиента или формы.</span><span class="sxs-lookup"><span data-stu-id="06028-118">If your form objects make disallowed transitions between states, they will not behave in the ways that messaging clients expect and could cause unpredictable client or form object behavior.</span></span>
  
> [!NOTE]
> <span data-ttu-id="06028-119">Некоторые переходы между состояниями зависят от данные из предыдущих состояний.</span><span class="sxs-lookup"><span data-stu-id="06028-119">Some state transitions depend on information from previous states.</span></span> <span data-ttu-id="06028-120">Сервер форм вероятнее всего необходимо реализовать флаг в его объекты формы для указания того, были ли изменены значения свойств сообщений для облегчения более поздние изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="06028-120">Your form server will most likely have to implement a flag in its form objects to indicate whether the values of the message's properties have been changed to facilitate later state changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="06028-121">См. также</span><span class="sxs-lookup"><span data-stu-id="06028-121">See also</span></span>

- [<span data-ttu-id="06028-122">Разработка серверов формы MAPI</span><span class="sxs-lookup"><span data-stu-id="06028-122">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

