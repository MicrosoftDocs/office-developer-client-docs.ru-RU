---
title: IMAPIViewContextGetViewStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetViewStatus
api_type:
- COM
ms.assetid: 2e5ec914-7171-41ce-a6fe-78dd80ac32ff
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bb8699746b3f4207ee70edd4e56d0ec6041beac2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429020"
---
# <a name="imapiviewcontextgetviewstatus"></a><span data-ttu-id="98325-103">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="98325-103">IMAPIViewContext::GetViewStatus</span></span>

  
  
<span data-ttu-id="98325-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98325-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98325-105">Извлекает текущее состояние просмотра.</span><span class="sxs-lookup"><span data-stu-id="98325-105">Retrieves the current viewer status.</span></span> 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="98325-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="98325-106">Parameters</span></span>

 <span data-ttu-id="98325-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="98325-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="98325-108">[вышел] Указатель на битмаску флагов, обеспечивающих состояние зрителя.</span><span class="sxs-lookup"><span data-stu-id="98325-108">[out] Pointer to a bitmask of flags providing the status of the viewer.</span></span> <span data-ttu-id="98325-109">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="98325-109">The following flags can be set:</span></span>
    
<span data-ttu-id="98325-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="98325-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="98325-111">Существует следующее или предыдущее сообщение в другой категории.</span><span class="sxs-lookup"><span data-stu-id="98325-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="98325-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="98325-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="98325-113">Форма позволяет удалять сообщения.</span><span class="sxs-lookup"><span data-stu-id="98325-113">The form allows messages to be removed.</span></span> 
    
<span data-ttu-id="98325-114">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="98325-114">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="98325-115">В форме должен отображаться пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="98325-115">The form should display a user interface.</span></span> <span data-ttu-id="98325-116">Если этот флаг не установлен, форма должна подавлять отображение пользовательского интерфейса даже в ответ на глагол, который обычно вызывает отображение пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="98325-116">If this flag is not set, the form should suppress displaying a user interface even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="98325-117">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="98325-117">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="98325-118">Форма является модальной для зрителя.</span><span class="sxs-lookup"><span data-stu-id="98325-118">The form is modal to the viewer.</span></span> 
    
<span data-ttu-id="98325-119">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="98325-119">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="98325-120">В представлении есть следующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="98325-120">There is a next message in the view.</span></span> 
    
<span data-ttu-id="98325-121">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="98325-121">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="98325-122">В представлении имеется предыдущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="98325-122">There is a previous message in the view.</span></span> 
    
<span data-ttu-id="98325-123">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="98325-123">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="98325-124">Сообщение должно быть открыто в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="98325-124">The message is to be opened in read-only mode.</span></span> <span data-ttu-id="98325-125">Операции удаления, отправки и перемещения должны быть отключены.</span><span class="sxs-lookup"><span data-stu-id="98325-125">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="98325-126">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="98325-126">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="98325-127">В представлении имеется следующее или предыдущее непрочитанные сообщения.</span><span class="sxs-lookup"><span data-stu-id="98325-127">There is a next or previous unread message in the view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="98325-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98325-128">Return value</span></span>

<span data-ttu-id="98325-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="98325-129">S_OK</span></span> 
  
> <span data-ttu-id="98325-130">Состояние зрителя было успешно возвращено.</span><span class="sxs-lookup"><span data-stu-id="98325-130">The viewer's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="98325-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="98325-131">Remarks</span></span>

<span data-ttu-id="98325-132">Объекты формы называют метод **IMAPIViewContext::GetViewStatus,** чтобы определить, активируется ли больше сообщений в представлении формы в обоих или обоих направлениях, в том  направлении, в котором команда **Next** активирует сообщения, в том направлении, в котором предыдущая команда активирует сообщения, или в обоих направлениях.</span><span class="sxs-lookup"><span data-stu-id="98325-132">Form objects call the **IMAPIViewContext::GetViewStatus** method to determine whether there are more messages to be activated in a form view in either or both directions that is, in the direction in which a **Next** command activates messages, in the direction in which a **Previous** command activates messages, or in both directions.</span></span> <span data-ttu-id="98325-133">Значение, на которые указывает параметр _lpulStatus,_ используется для определения допустимости флагов VCSTATUS_NEXT и VCSTATUS_PREV [для IMAPIViewContext::ActivateNext.](imapiviewcontext-activatenext.md)</span><span class="sxs-lookup"><span data-stu-id="98325-133">The value pointed to by the  _lpulStatus_ parameter is used to determine whether the VCSTATUS_NEXT and VCSTATUS_PREV flags are valid for [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md).</span></span> <span data-ttu-id="98325-134">Если флаг VCSTATUS_DELETE, но не флаг VCSTATUS_READONLY, сообщение можно удалить с помощью метода [IMAPIMessageSite::D eleteMessage.](imapimessagesite-deletemessage.md)</span><span class="sxs-lookup"><span data-stu-id="98325-134">If the VCSTATUS_DELETE flag is set, but not the VCSTATUS_READONLY flag, then the message can be deleted using the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) method.</span></span> 
  
<span data-ttu-id="98325-135">Как правило, формы отключать команды меню и кнопки, если они не допустимы для контекста просмотра.</span><span class="sxs-lookup"><span data-stu-id="98325-135">Typically, forms disable menu commands and buttons if they are not valid for the viewer's context.</span></span> <span data-ttu-id="98325-136">Зритель может предупредить форму об изменении состояния, назвав метод [IMAPIFormAdviseSink::OnChange.](imapiformadvisesink-onchange.md)</span><span class="sxs-lookup"><span data-stu-id="98325-136">A viewer can alert a form to a change in status by calling its [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) method.</span></span> 
  
<span data-ttu-id="98325-137">Флаг VCSTATUS_MODAL, если форма должна быть модальной в окне, ручка которого передается в более ранний вызов [IMAPIForm::D oVerb.](imapiform-doverb.md)</span><span class="sxs-lookup"><span data-stu-id="98325-137">The VCSTATUS_MODAL flag is set if the form must be modal to the window whose handle is passed in the earlier [IMAPIForm::DoVerb](imapiform-doverb.md) call.</span></span> <span data-ttu-id="98325-138">Если VCSTATUS_MODAL, форма может использовать поток, на котором был выполнен вызов **DoVerb** до закрытия формы.</span><span class="sxs-lookup"><span data-stu-id="98325-138">If VCSTATUS_MODAL is set, the form can use the thread on which the **DoVerb** call was made until the form closes.</span></span> <span data-ttu-id="98325-139">Если VCSTATUS_MODAL не заданной, форма не должна быть модальной для этого окна и не должна использовать поток.</span><span class="sxs-lookup"><span data-stu-id="98325-139">If VCSTATUS_MODAL is not set, the form should not be modal to this window and must not use the thread.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="98325-140">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="98325-140">MFCMAPI reference</span></span>

<span data-ttu-id="98325-141">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="98325-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="98325-142">**Файл**</span><span class="sxs-lookup"><span data-stu-id="98325-142">**File**</span></span>|<span data-ttu-id="98325-143">**Функция**</span><span class="sxs-lookup"><span data-stu-id="98325-143">**Function**</span></span>|<span data-ttu-id="98325-144">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="98325-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="98325-145">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="98325-145">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="98325-146">CMyMAPIFormViewer::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="98325-146">CMyMAPIFormViewer::GetViewStatus</span></span>  <br/> |<span data-ttu-id="98325-147">MFCMAPI реализует метод **IMAPIViewContext::GetViewStatus** в этой функции.</span><span class="sxs-lookup"><span data-stu-id="98325-147">MFCMAPI implements the **IMAPIViewContext::GetViewStatus** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="98325-148">См. также</span><span class="sxs-lookup"><span data-stu-id="98325-148">See also</span></span>



[<span data-ttu-id="98325-149">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="98325-149">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="98325-150">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="98325-150">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)


[<span data-ttu-id="98325-151">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="98325-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

