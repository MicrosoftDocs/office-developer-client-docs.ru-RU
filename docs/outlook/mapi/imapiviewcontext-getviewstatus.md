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
ms.openlocfilehash: fb543f4188578483333614cb5768f903c9f243d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809278"
---
# <a name="imapiviewcontextgetviewstatus"></a><span data-ttu-id="47d15-103">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="47d15-103">IMAPIViewContext::GetViewStatus</span></span>

  
  
<span data-ttu-id="47d15-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="47d15-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="47d15-105">Извлекает текущее состояние просмотра.</span><span class="sxs-lookup"><span data-stu-id="47d15-105">Retrieves the current viewer status.</span></span> 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="47d15-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="47d15-106">Parameters</span></span>

 <span data-ttu-id="47d15-107">_lpulStatus_</span><span class="sxs-lookup"><span data-stu-id="47d15-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="47d15-108">[out] Указатель на битовой маски флагов, предоставляя состояние просмотра.</span><span class="sxs-lookup"><span data-stu-id="47d15-108">[out] Pointer to a bitmask of flags providing the status of the viewer.</span></span> <span data-ttu-id="47d15-109">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="47d15-109">The following flags can be set:</span></span>
    
<span data-ttu-id="47d15-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="47d15-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="47d15-111">Имеется следующий или предыдущий сообщение в другой категории.</span><span class="sxs-lookup"><span data-stu-id="47d15-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="47d15-112">VCSTATUS_DELETE</span><span class="sxs-lookup"><span data-stu-id="47d15-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="47d15-113">Форма позволяет удалить сообщения.</span><span class="sxs-lookup"><span data-stu-id="47d15-113">The form allows messages to be removed.</span></span> 
    
<span data-ttu-id="47d15-114">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="47d15-114">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="47d15-115">Форма должна пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="47d15-115">The form should display a user interface.</span></span> <span data-ttu-id="47d15-116">Если этот флаг не установлен, форма следует отключать отображение даже в ответ на команду, которая обычно вызывает пользовательский интерфейс для отображения пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="47d15-116">If this flag is not set, the form should suppress displaying a user interface even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="47d15-117">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="47d15-117">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="47d15-118">Форма является модальным для просмотра.</span><span class="sxs-lookup"><span data-stu-id="47d15-118">The form is modal to the viewer.</span></span> 
    
<span data-ttu-id="47d15-119">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="47d15-119">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="47d15-120">В представлении имеется следующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="47d15-120">There is a next message in the view.</span></span> 
    
<span data-ttu-id="47d15-121">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="47d15-121">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="47d15-122">Существует предыдущее сообщение в представлении.</span><span class="sxs-lookup"><span data-stu-id="47d15-122">There is a previous message in the view.</span></span> 
    
<span data-ttu-id="47d15-123">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="47d15-123">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="47d15-124">Сообщение является открываются в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="47d15-124">The message is to be opened in read-only mode.</span></span> <span data-ttu-id="47d15-125">Удаление, отправка и переместите операции должны быть отключены.</span><span class="sxs-lookup"><span data-stu-id="47d15-125">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="47d15-126">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="47d15-126">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="47d15-127">В представлении имеется следующий или предыдущий непрочитанные сообщения.</span><span class="sxs-lookup"><span data-stu-id="47d15-127">There is a next or previous unread message in the view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="47d15-128">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="47d15-128">Return value</span></span>

<span data-ttu-id="47d15-129">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="47d15-129">S_OK</span></span> 
  
> <span data-ttu-id="47d15-130">Средство просмотра состояния успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="47d15-130">The viewer's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="47d15-131">Замечания</span><span class="sxs-lookup"><span data-stu-id="47d15-131">Remarks</span></span>

<span data-ttu-id="47d15-132">Объекты формы вызовите метод **IMAPIViewContext::GetViewStatus** , чтобы определить, есть ли дополнительные сообщения будут активироваться в представлении формы в одном или обоих направлениях то есть в направлении, в котором активируется команда **Далее** сообщения в направление, в котором **Предыдущая** команда активирует сообщения, или в обоих направлениях.</span><span class="sxs-lookup"><span data-stu-id="47d15-132">Form objects call the **IMAPIViewContext::GetViewStatus** method to determine whether there are more messages to be activated in a form view in either or both directions that is, in the direction in which a **Next** command activates messages, in the direction in which a **Previous** command activates messages, or in both directions.</span></span> <span data-ttu-id="47d15-133">Значение, указывает параметр _lpulStatus_ используется для определения допустимости флаги VCSTATUS_NEXT и VCSTATUS_PREV для [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md).</span><span class="sxs-lookup"><span data-stu-id="47d15-133">The value pointed to by the  _lpulStatus_ parameter is used to determine whether the VCSTATUS_NEXT and VCSTATUS_PREV flags are valid for [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md).</span></span> <span data-ttu-id="47d15-134">Если флаг VCSTATUS_DELETE, set, но не флаг VCSTATUS_READONLY, а затем сообщения можно удалить с помощью метода [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) .</span><span class="sxs-lookup"><span data-stu-id="47d15-134">If the VCSTATUS_DELETE flag is set, but not the VCSTATUS_READONLY flag, then the message can be deleted using the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) method.</span></span> 
  
<span data-ttu-id="47d15-135">Как правило форм отключить команды меню и кнопки, если они не являются действительными для контекста средство просмотра.</span><span class="sxs-lookup"><span data-stu-id="47d15-135">Typically, forms disable menu commands and buttons if they are not valid for the viewer's context.</span></span> <span data-ttu-id="47d15-136">Средство просмотра можно предупредить формы на изменение состояния путем вызова метода [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) .</span><span class="sxs-lookup"><span data-stu-id="47d15-136">A viewer can alert a form to a change in status by calling its [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) method.</span></span> 
  
<span data-ttu-id="47d15-137">Флаг VCSTATUS_MODAL имеет значение, если форма должна быть модальное окно, дескриптор которого передается в более ранних [IMAPIForm::DoVerb](imapiform-doverb.md) вызова.</span><span class="sxs-lookup"><span data-stu-id="47d15-137">The VCSTATUS_MODAL flag is set if the form must be modal to the window whose handle is passed in the earlier [IMAPIForm::DoVerb](imapiform-doverb.md) call.</span></span> <span data-ttu-id="47d15-138">Если значение VCSTATUS_MODAL, форму можно использовать поток, на котором был выполнен вызов **DoVerb** , пока эта форма закрывается.</span><span class="sxs-lookup"><span data-stu-id="47d15-138">If VCSTATUS_MODAL is set, the form can use the thread on which the **DoVerb** call was made until the form closes.</span></span> <span data-ttu-id="47d15-139">Если VCSTATUS_MODAL не установлен, форма не должна быть модальное окно и не должны использовать потока.</span><span class="sxs-lookup"><span data-stu-id="47d15-139">If VCSTATUS_MODAL is not set, the form should not be modal to this window and must not use the thread.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="47d15-140">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="47d15-140">MFCMAPI reference</span></span>

<span data-ttu-id="47d15-141">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="47d15-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="47d15-142">**����**</span><span class="sxs-lookup"><span data-stu-id="47d15-142">**File**</span></span>|<span data-ttu-id="47d15-143">**�������**</span><span class="sxs-lookup"><span data-stu-id="47d15-143">**Function**</span></span>|<span data-ttu-id="47d15-144">**�����������**</span><span class="sxs-lookup"><span data-stu-id="47d15-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="47d15-145">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="47d15-145">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="47d15-146">CMyMAPIFormViewer::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="47d15-146">CMyMAPIFormViewer::GetViewStatus</span></span>  <br/> |<span data-ttu-id="47d15-147">Mfcmapi (en) реализован метод **IMAPIViewContext::GetViewStatus** в этой функции.</span><span class="sxs-lookup"><span data-stu-id="47d15-147">MFCMAPI implements the **IMAPIViewContext::GetViewStatus** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="47d15-148">См. также</span><span class="sxs-lookup"><span data-stu-id="47d15-148">See also</span></span>



[<span data-ttu-id="47d15-149">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="47d15-149">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="47d15-150">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="47d15-150">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)


[<span data-ttu-id="47d15-151">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="47d15-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

