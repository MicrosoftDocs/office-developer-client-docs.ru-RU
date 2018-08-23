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
ms.openlocfilehash: e32157f41632b782fbacf87e0411c18d167b4279
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576682"
---
# <a name="imapiformadvisesinkonchange"></a><span data-ttu-id="f2a6d-103">IMAPIFormAdviseSink::OnChange</span><span class="sxs-lookup"><span data-stu-id="f2a6d-103">IMAPIFormAdviseSink::OnChange</span></span>

  
  
<span data-ttu-id="f2a6d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2a6d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2a6d-105">Указывает, было изменено в состояние просмотра формы.</span><span class="sxs-lookup"><span data-stu-id="f2a6d-105">Indicates that a change has occurred in the status of the form viewer.</span></span> 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a><span data-ttu-id="f2a6d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2a6d-106">Parameters</span></span>

 <span data-ttu-id="f2a6d-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="f2a6d-107">_ulDir_</span></span>
  
> <span data-ttu-id="f2a6d-108">[in] Битовая маска флаги, который предоставляет сведения об изменениях, выполненной в средстве просмотра и ожидаемых ответа в форме.</span><span class="sxs-lookup"><span data-stu-id="f2a6d-108">[in] A bitmask of flags that provides information about the change that has occurred in the viewer and the expected response in the form.</span></span> <span data-ttu-id="f2a6d-109">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="f2a6d-109">The following flags can be set:</span></span>
    
<span data-ttu-id="f2a6d-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="f2a6d-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="f2a6d-111">Имеется следующий или предыдущий сообщение в другой категории.</span><span class="sxs-lookup"><span data-stu-id="f2a6d-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="f2a6d-112">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="f2a6d-112">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="f2a6d-113">Форма должна пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f2a6d-113">The form should display a user interface.</span></span> <span data-ttu-id="f2a6d-114">Если этот флаг не установлен, форма следует отключать отображение пользовательского интерфейса, даже в ответ на команду, которая обычно приводит пользовательского интерфейса для отображения.</span><span class="sxs-lookup"><span data-stu-id="f2a6d-114">If this flag is not set, the form should suppress displaying a user interface, even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="f2a6d-115">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="f2a6d-115">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="f2a6d-116">Форма является модальным для просмотра формы.</span><span class="sxs-lookup"><span data-stu-id="f2a6d-116">The form is to be modal to the form viewer.</span></span> 
    
<span data-ttu-id="f2a6d-117">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="f2a6d-117">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="f2a6d-118">В средстве просмотра формы существует следующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="f2a6d-118">There is a next message in the form viewer.</span></span> 
    
<span data-ttu-id="f2a6d-119">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="f2a6d-119">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="f2a6d-120">В средстве просмотра формы существует предыдущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="f2a6d-120">There is a previous message in the form viewer.</span></span> 
    
<span data-ttu-id="f2a6d-121">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="f2a6d-121">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="f2a6d-122">Удаление, отправка и переместите операции должны быть отключены.</span><span class="sxs-lookup"><span data-stu-id="f2a6d-122">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="f2a6d-123">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="f2a6d-123">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="f2a6d-124">В средстве просмотра формы имеется следующий или предыдущий непрочитанные сообщения.</span><span class="sxs-lookup"><span data-stu-id="f2a6d-124">There is a next or previous unread message in the form viewer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f2a6d-125">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="f2a6d-125">Return value</span></span>

<span data-ttu-id="f2a6d-126">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="f2a6d-126">S_OK</span></span> 
  
> <span data-ttu-id="f2a6d-127">Уведомление успешно.</span><span class="sxs-lookup"><span data-stu-id="f2a6d-127">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f2a6d-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="f2a6d-128">Remarks</span></span>

<span data-ttu-id="f2a6d-129">Средства просмотра форм вызовите метод **IMAPIFormAdviseSink::OnChange** для уведомления формы об изменении состояния средство просмотра.</span><span class="sxs-lookup"><span data-stu-id="f2a6d-129">Form viewers call the **IMAPIFormAdviseSink::OnChange** method to notify the form about a change in a viewer's status.</span></span> <span data-ttu-id="f2a6d-130">Как правило только изменения задание или снять VCSTATUS_NEXT или VCSTATUS_PREVIOUS флаг, в зависимости от наличия или отсутствия следующий или предыдущий сообщения в средстве просмотра.</span><span class="sxs-lookup"><span data-stu-id="f2a6d-130">Usually, the only change is setting or clearing the VCSTATUS_NEXT or VCSTATUS_PREVIOUS flag based on the presence or absence of a next or previous message in the viewer.</span></span> <span data-ttu-id="f2a6d-131">Соответственно объект формы затем включает или отключает следующий или предыдущий действия, которые он поддерживает.</span><span class="sxs-lookup"><span data-stu-id="f2a6d-131">Accordingly, the form object then enables or disables any next or previous actions it supports.</span></span> 
  
<span data-ttu-id="f2a6d-132">Параметры VCSTATUS_MODAL и VCSTATUS_INTERACTIVE не может изменить в контекст представления после его создания.</span><span class="sxs-lookup"><span data-stu-id="f2a6d-132">The settings of VCSTATUS_MODAL and VCSTATUS_INTERACTIVE cannot change in a view context after it has been created.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f2a6d-133">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="f2a6d-133">Notes to implementers</span></span>

<span data-ttu-id="f2a6d-134">Реализации этого метода полностью зависит от особенностей формы.</span><span class="sxs-lookup"><span data-stu-id="f2a6d-134">The specific implementation of this method is completely dependent on the specifics of the form.</span></span> <span data-ttu-id="f2a6d-135">Большинство объектов формы используйте этот метод для изменения их пользовательского интерфейса (например, чтобы включить или отключить команды меню или кнопки в соответствии с параметр flags состояние просмотра).</span><span class="sxs-lookup"><span data-stu-id="f2a6d-135">Most form objects use this method to change their user interface (for example, to enable or disable menu commands or buttons to match the viewer status flags parameter).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f2a6d-136">См. также</span><span class="sxs-lookup"><span data-stu-id="f2a6d-136">See also</span></span>



[<span data-ttu-id="f2a6d-137">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="f2a6d-137">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="f2a6d-138">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f2a6d-138">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)

