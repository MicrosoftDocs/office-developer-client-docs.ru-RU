---
title: IMAPIFormAdviseSinkOnChange
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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431899"
---
# <a name="imapiformadvisesinkonchange"></a><span data-ttu-id="f20b0-103">IMAPIFormAdviseSink::OnChange</span><span class="sxs-lookup"><span data-stu-id="f20b0-103">IMAPIFormAdviseSink::OnChange</span></span>

  
  
<span data-ttu-id="f20b0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f20b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f20b0-105">Указывает, что в состоянии просмотра формы произошли изменения.</span><span class="sxs-lookup"><span data-stu-id="f20b0-105">Indicates that a change has occurred in the status of the form viewer.</span></span> 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a><span data-ttu-id="f20b0-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="f20b0-106">Parameters</span></span>

 <span data-ttu-id="f20b0-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="f20b0-107">_ulDir_</span></span>
  
> <span data-ttu-id="f20b0-108">[in] Битмашка флагов, которая содержит сведения об изменениях, произошедших в зрительском окне, и ожидаемом отклике в форме.</span><span class="sxs-lookup"><span data-stu-id="f20b0-108">[in] A bitmask of flags that provides information about the change that has occurred in the viewer and the expected response in the form.</span></span> <span data-ttu-id="f20b0-109">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="f20b0-109">The following flags can be set:</span></span>
    
<span data-ttu-id="f20b0-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="f20b0-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="f20b0-111">Существует следующее или предыдущее сообщение в другой категории.</span><span class="sxs-lookup"><span data-stu-id="f20b0-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="f20b0-112">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="f20b0-112">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="f20b0-113">В форме должен отображаться пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="f20b0-113">The form should display a user interface.</span></span> <span data-ttu-id="f20b0-114">Если этот флаг не установлен, форма должна подавлять отображение пользовательского интерфейса даже в ответ на глагол, который обычно вызывает отображение пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f20b0-114">If this flag is not set, the form should suppress displaying a user interface, even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="f20b0-115">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="f20b0-115">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="f20b0-116">Форма должна быть модальной для просмотра формы.</span><span class="sxs-lookup"><span data-stu-id="f20b0-116">The form is to be modal to the form viewer.</span></span> 
    
<span data-ttu-id="f20b0-117">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="f20b0-117">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="f20b0-118">В представлении формы есть следующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="f20b0-118">There is a next message in the form viewer.</span></span> 
    
<span data-ttu-id="f20b0-119">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="f20b0-119">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="f20b0-120">В представлении формы имеется предыдущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="f20b0-120">There is a previous message in the form viewer.</span></span> 
    
<span data-ttu-id="f20b0-121">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="f20b0-121">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="f20b0-122">Операции удаления, отправки и перемещения должны быть отключены.</span><span class="sxs-lookup"><span data-stu-id="f20b0-122">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="f20b0-123">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="f20b0-123">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="f20b0-124">В представлении формы имеется следующее или предыдущее непрочитанные сообщения.</span><span class="sxs-lookup"><span data-stu-id="f20b0-124">There is a next or previous unread message in the form viewer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f20b0-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f20b0-125">Return value</span></span>

<span data-ttu-id="f20b0-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="f20b0-126">S_OK</span></span> 
  
> <span data-ttu-id="f20b0-127">Уведомление было успешным.</span><span class="sxs-lookup"><span data-stu-id="f20b0-127">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f20b0-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="f20b0-128">Remarks</span></span>

<span data-ttu-id="f20b0-129">Зрители формы звонят по методу **IMAPIFormAdviseSink::OnChange,** чтобы уведомить форму об изменении состояния пользователя.</span><span class="sxs-lookup"><span data-stu-id="f20b0-129">Form viewers call the **IMAPIFormAdviseSink::OnChange** method to notify the form about a change in a viewer's status.</span></span> <span data-ttu-id="f20b0-130">Обычно единственным изменением является установка или очистка флага VCSTATUS_NEXT или VCSTATUS_PREVIOUS в зависимости от наличия или отсутствия следующего или предыдущего сообщения в зрителье.</span><span class="sxs-lookup"><span data-stu-id="f20b0-130">Usually, the only change is setting or clearing the VCSTATUS_NEXT or VCSTATUS_PREVIOUS flag based on the presence or absence of a next or previous message in the viewer.</span></span> <span data-ttu-id="f20b0-131">Соответственно, объект формы включает или отключает любые последующие или предыдущие действия, которые он поддерживает.</span><span class="sxs-lookup"><span data-stu-id="f20b0-131">Accordingly, the form object then enables or disables any next or previous actions it supports.</span></span> 
  
<span data-ttu-id="f20b0-132">Параметры VCSTATUS_MODAL и VCSTATUS_INTERACTIVE не могут измениться в контексте представления после создания.</span><span class="sxs-lookup"><span data-stu-id="f20b0-132">The settings of VCSTATUS_MODAL and VCSTATUS_INTERACTIVE cannot change in a view context after it has been created.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f20b0-133">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="f20b0-133">Notes to implementers</span></span>

<span data-ttu-id="f20b0-134">Конкретная реализация этого метода полностью зависит от специфики формы.</span><span class="sxs-lookup"><span data-stu-id="f20b0-134">The specific implementation of this method is completely dependent on the specifics of the form.</span></span> <span data-ttu-id="f20b0-135">Большинство объектов формы используют этот метод для изменения пользовательского интерфейса (например, для включения или отключения команд или кнопок меню, чтобы соответствовать параметру флагов состояния просмотра).</span><span class="sxs-lookup"><span data-stu-id="f20b0-135">Most form objects use this method to change their user interface (for example, to enable or disable menu commands or buttons to match the viewer status flags parameter).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f20b0-136">См. также</span><span class="sxs-lookup"><span data-stu-id="f20b0-136">See also</span></span>



[<span data-ttu-id="f20b0-137">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="f20b0-137">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="f20b0-138">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f20b0-138">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)

