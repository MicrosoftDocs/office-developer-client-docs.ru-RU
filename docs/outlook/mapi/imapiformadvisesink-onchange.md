---
title: Имапиформадвисесинкончанже
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnChange
api_type:
- COM
ms.assetid: d700b40f-e5b2-4d37-bf1f-8fd3dfa0dda5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 02663570e3173bbd696af732e71f060d9dee49bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286630"
---
# <a name="imapiformadvisesinkonchange"></a><span data-ttu-id="2dcc7-103">IMAPIFormAdviseSink::OnChange</span><span class="sxs-lookup"><span data-stu-id="2dcc7-103">IMAPIFormAdviseSink::OnChange</span></span>

  
  
<span data-ttu-id="2dcc7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2dcc7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2dcc7-105">Указывает, что в состоянии средства просмотра форм произошло изменение.</span><span class="sxs-lookup"><span data-stu-id="2dcc7-105">Indicates that a change has occurred in the status of the form viewer.</span></span> 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a><span data-ttu-id="2dcc7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2dcc7-106">Parameters</span></span>

 <span data-ttu-id="2dcc7-107">_Улдир_</span><span class="sxs-lookup"><span data-stu-id="2dcc7-107">_ulDir_</span></span>
  
> <span data-ttu-id="2dcc7-108">возврата Битовая маска флагов, которая предоставляет сведения об изменениях, произошедших в средстве просмотра, и ожидаемом ответе в форме.</span><span class="sxs-lookup"><span data-stu-id="2dcc7-108">[in] A bitmask of flags that provides information about the change that has occurred in the viewer and the expected response in the form.</span></span> <span data-ttu-id="2dcc7-109">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="2dcc7-109">The following flags can be set:</span></span>
    
<span data-ttu-id="2dcc7-110">ВКСТАТУС_КАТЕГОРИ</span><span class="sxs-lookup"><span data-stu-id="2dcc7-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="2dcc7-111">В другой категории есть следующее или предыдущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="2dcc7-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="2dcc7-112">ВКСТАТУС_ИНТЕРАКТИВЕ</span><span class="sxs-lookup"><span data-stu-id="2dcc7-112">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="2dcc7-113">Форма должна отображать пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2dcc7-113">The form should display a user interface.</span></span> <span data-ttu-id="2dcc7-114">Если этот флаг не установлен, форма должна подавлять отображение пользовательского интерфейса даже в ответ на команду, которая обычно вызывает отображение пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2dcc7-114">If this flag is not set, the form should suppress displaying a user interface, even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="2dcc7-115">ВКСТАТУС_МОДАЛ</span><span class="sxs-lookup"><span data-stu-id="2dcc7-115">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="2dcc7-116">Форма является модальной в средстве просмотра форм.</span><span class="sxs-lookup"><span data-stu-id="2dcc7-116">The form is to be modal to the form viewer.</span></span> 
    
<span data-ttu-id="2dcc7-117">ВКСТАТУС_НЕКСТ</span><span class="sxs-lookup"><span data-stu-id="2dcc7-117">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="2dcc7-118">В средстве просмотра форм появляется следующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="2dcc7-118">There is a next message in the form viewer.</span></span> 
    
<span data-ttu-id="2dcc7-119">ВКСТАТУС_ПРЕВ</span><span class="sxs-lookup"><span data-stu-id="2dcc7-119">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="2dcc7-120">В средстве просмотра форм существует предыдущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="2dcc7-120">There is a previous message in the form viewer.</span></span> 
    
<span data-ttu-id="2dcc7-121">ВКСТАТУС_РЕАДОНЛИ</span><span class="sxs-lookup"><span data-stu-id="2dcc7-121">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="2dcc7-122">Операции удаления, отсылки и перемещения следует отключить.</span><span class="sxs-lookup"><span data-stu-id="2dcc7-122">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="2dcc7-123">ВКСТАТУС_УНРЕАД</span><span class="sxs-lookup"><span data-stu-id="2dcc7-123">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="2dcc7-124">В средстве просмотра форм находится следующее или предыдущее непрочитанное сообщение.</span><span class="sxs-lookup"><span data-stu-id="2dcc7-124">There is a next or previous unread message in the form viewer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2dcc7-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2dcc7-125">Return value</span></span>

<span data-ttu-id="2dcc7-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="2dcc7-126">S_OK</span></span> 
  
> <span data-ttu-id="2dcc7-127">Уведомление успешно установлено.</span><span class="sxs-lookup"><span data-stu-id="2dcc7-127">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2dcc7-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="2dcc7-128">Remarks</span></span>

<span data-ttu-id="2dcc7-129">Средства просмотра форм вызывают метод **имапиформадвисесинк:: OnChange** , чтобы уведомить форму об изменении состояния средства просмотра.</span><span class="sxs-lookup"><span data-stu-id="2dcc7-129">Form viewers call the **IMAPIFormAdviseSink::OnChange** method to notify the form about a change in a viewer's status.</span></span> <span data-ttu-id="2dcc7-130">Как правило, единственным изменением является установка или снятие флага ВКСТАТУС_НЕКСТ или ВКСТАТУС_ПРЕВИАУС на основе присутствия или отсутствия следующего или предыдущего сообщения в средстве просмотра.</span><span class="sxs-lookup"><span data-stu-id="2dcc7-130">Usually, the only change is setting or clearing the VCSTATUS_NEXT or VCSTATUS_PREVIOUS flag based on the presence or absence of a next or previous message in the viewer.</span></span> <span data-ttu-id="2dcc7-131">Соответственно, объект Form позволяет включать или отключать все следующие или предыдущие действия, которые она поддерживает.</span><span class="sxs-lookup"><span data-stu-id="2dcc7-131">Accordingly, the form object then enables or disables any next or previous actions it supports.</span></span> 
  
<span data-ttu-id="2dcc7-132">Параметры ВКСТАТУС_МОДАЛ и ВКСТАТУС_ИНТЕРАКТИВЕ не могут измениться в контексте представления после его создания.</span><span class="sxs-lookup"><span data-stu-id="2dcc7-132">The settings of VCSTATUS_MODAL and VCSTATUS_INTERACTIVE cannot change in a view context after it has been created.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2dcc7-133">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="2dcc7-133">Notes to implementers</span></span>

<span data-ttu-id="2dcc7-134">Конкретная реализация этого метода полностью зависит от конкретных характеров формы.</span><span class="sxs-lookup"><span data-stu-id="2dcc7-134">The specific implementation of this method is completely dependent on the specifics of the form.</span></span> <span data-ttu-id="2dcc7-135">Большинство объектов форм этот метод используется для изменения пользовательского интерфейса (например, для включения или отключения команд меню или кнопок в соответствии с параметром флагов состояния средства просмотра).</span><span class="sxs-lookup"><span data-stu-id="2dcc7-135">Most form objects use this method to change their user interface (for example, to enable or disable menu commands or buttons to match the viewer status flags parameter).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2dcc7-136">См. также</span><span class="sxs-lookup"><span data-stu-id="2dcc7-136">See also</span></span>



[<span data-ttu-id="2dcc7-137">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="2dcc7-137">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="2dcc7-138">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2dcc7-138">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)

