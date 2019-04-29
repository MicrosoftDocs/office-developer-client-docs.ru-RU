---
title: Имапивиевконтекстжетвиевстатус
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
# <a name="imapiviewcontextgetviewstatus"></a><span data-ttu-id="17774-103">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="17774-103">IMAPIViewContext::GetViewStatus</span></span>

  
  
<span data-ttu-id="17774-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17774-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17774-105">Получает текущее состояние средства просмотра.</span><span class="sxs-lookup"><span data-stu-id="17774-105">Retrieves the current viewer status.</span></span> 
  
```cpp
HRESULT GetViewStatus(
ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a><span data-ttu-id="17774-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="17774-106">Parameters</span></span>

 <span data-ttu-id="17774-107">_Лпулстатус_</span><span class="sxs-lookup"><span data-stu-id="17774-107">_lpulStatus_</span></span>
  
> <span data-ttu-id="17774-108">вышли Указатель на битовую маску флагов, обеспечивающих состояние средства просмотра.</span><span class="sxs-lookup"><span data-stu-id="17774-108">[out] Pointer to a bitmask of flags providing the status of the viewer.</span></span> <span data-ttu-id="17774-109">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="17774-109">The following flags can be set:</span></span>
    
<span data-ttu-id="17774-110">ВКСТАТУС_КАТЕГОРИ</span><span class="sxs-lookup"><span data-stu-id="17774-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="17774-111">В другой категории есть следующее или предыдущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="17774-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="17774-112">ВКСТАТУС_ДЕЛЕТЕ</span><span class="sxs-lookup"><span data-stu-id="17774-112">VCSTATUS_DELETE</span></span> 
  
> <span data-ttu-id="17774-113">Форма позволяет удалять сообщения.</span><span class="sxs-lookup"><span data-stu-id="17774-113">The form allows messages to be removed.</span></span> 
    
<span data-ttu-id="17774-114">ВКСТАТУС_ИНТЕРАКТИВЕ</span><span class="sxs-lookup"><span data-stu-id="17774-114">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="17774-115">Форма должна отображать пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="17774-115">The form should display a user interface.</span></span> <span data-ttu-id="17774-116">Если этот флаг не установлен, форма должна подавлять отображение пользовательского интерфейса даже в ответ на команду, которая обычно приводит к отображению пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="17774-116">If this flag is not set, the form should suppress displaying a user interface even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="17774-117">ВКСТАТУС_МОДАЛ</span><span class="sxs-lookup"><span data-stu-id="17774-117">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="17774-118">Форма является модальной для средства просмотра.</span><span class="sxs-lookup"><span data-stu-id="17774-118">The form is modal to the viewer.</span></span> 
    
<span data-ttu-id="17774-119">ВКСТАТУС_НЕКСТ</span><span class="sxs-lookup"><span data-stu-id="17774-119">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="17774-120">В представлении отображается следующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="17774-120">There is a next message in the view.</span></span> 
    
<span data-ttu-id="17774-121">ВКСТАТУС_ПРЕВ</span><span class="sxs-lookup"><span data-stu-id="17774-121">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="17774-122">В представлении имеется предыдущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="17774-122">There is a previous message in the view.</span></span> 
    
<span data-ttu-id="17774-123">ВКСТАТУС_РЕАДОНЛИ</span><span class="sxs-lookup"><span data-stu-id="17774-123">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="17774-124">Сообщение должно быть открыто в режиме "только чтение".</span><span class="sxs-lookup"><span data-stu-id="17774-124">The message is to be opened in read-only mode.</span></span> <span data-ttu-id="17774-125">Операции удаления, отсылки и перемещения следует отключить.</span><span class="sxs-lookup"><span data-stu-id="17774-125">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="17774-126">ВКСТАТУС_УНРЕАД</span><span class="sxs-lookup"><span data-stu-id="17774-126">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="17774-127">В представлении находится следующее или предыдущее непрочитанное сообщение.</span><span class="sxs-lookup"><span data-stu-id="17774-127">There is a next or previous unread message in the view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="17774-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17774-128">Return value</span></span>

<span data-ttu-id="17774-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="17774-129">S_OK</span></span> 
  
> <span data-ttu-id="17774-130">Состояние средства просмотра успешно возвращено.</span><span class="sxs-lookup"><span data-stu-id="17774-130">The viewer's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="17774-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="17774-131">Remarks</span></span>

<span data-ttu-id="17774-132">Объекты формы вызывают метод **имапивиевконтекст:: жетвиевстатус** , чтобы определить, больше ли сообщений, которые необходимо активировать в представлении формы, в любом направлении или в обоих направлениях, в котором **Следующая** команда активирует сообщения, в поле направление, в котором **Предыдущая** команда активирует сообщения или в обоих направлениях.</span><span class="sxs-lookup"><span data-stu-id="17774-132">Form objects call the **IMAPIViewContext::GetViewStatus** method to determine whether there are more messages to be activated in a form view in either or both directions that is, in the direction in which a **Next** command activates messages, in the direction in which a **Previous** command activates messages, or in both directions.</span></span> <span data-ttu-id="17774-133">Значение, указываемое параметром _лпулстатус_ , используется для определения того, допустимы ли флаги ВКСТАТУС_НЕКСТ и Вкстатус_прев для [Имапивиевконтекст:: активатенекст](imapiviewcontext-activatenext.md).</span><span class="sxs-lookup"><span data-stu-id="17774-133">The value pointed to by the  _lpulStatus_ parameter is used to determine whether the VCSTATUS_NEXT and VCSTATUS_PREV flags are valid for [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md).</span></span> <span data-ttu-id="17774-134">Если установлен флаг ВКСТАТУС_ДЕЛЕТЕ, но не установлен флаг ВКСТАТУС_РЕАДОНЛИ, то сообщение можно удалить с помощью метода [имапимессажесите::D елетемессаже](imapimessagesite-deletemessage.md) .</span><span class="sxs-lookup"><span data-stu-id="17774-134">If the VCSTATUS_DELETE flag is set, but not the VCSTATUS_READONLY flag, then the message can be deleted using the [IMAPIMessageSite::DeleteMessage](imapimessagesite-deletemessage.md) method.</span></span> 
  
<span data-ttu-id="17774-135">Как правило, формы отключают команды меню и кнопки, если они не являются допустимыми для контекста средства просмотра.</span><span class="sxs-lookup"><span data-stu-id="17774-135">Typically, forms disable menu commands and buttons if they are not valid for the viewer's context.</span></span> <span data-ttu-id="17774-136">Средство просмотра может оповещать форму об изменении состояния, вызывая метод [имапиформадвисесинк:: OnChange](imapiformadvisesink-onchange.md) .</span><span class="sxs-lookup"><span data-stu-id="17774-136">A viewer can alert a form to a change in status by calling its [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) method.</span></span> 
  
<span data-ttu-id="17774-137">Флаг ВКСТАТУС_МОДАЛ устанавливается, если форма должна быть модальной для окна, дескриптор которого передается в предыдущем [имапиформ::D вызов оверб](imapiform-doverb.md) .</span><span class="sxs-lookup"><span data-stu-id="17774-137">The VCSTATUS_MODAL flag is set if the form must be modal to the window whose handle is passed in the earlier [IMAPIForm::DoVerb](imapiform-doverb.md) call.</span></span> <span data-ttu-id="17774-138">Если задано значение ВКСТАТУС_МОДАЛ, форма может использовать поток, в котором был выполнен вызов **доверб** , до закрытия формы.</span><span class="sxs-lookup"><span data-stu-id="17774-138">If VCSTATUS_MODAL is set, the form can use the thread on which the **DoVerb** call was made until the form closes.</span></span> <span data-ttu-id="17774-139">Если ВКСТАТУС_МОДАЛ не задано, форма не должна быть модальной в этом окне и не должна использовать этот поток.</span><span class="sxs-lookup"><span data-stu-id="17774-139">If VCSTATUS_MODAL is not set, the form should not be modal to this window and must not use the thread.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="17774-140">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="17774-140">MFCMAPI reference</span></span>

<span data-ttu-id="17774-141">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="17774-141">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="17774-142">**Файл**</span><span class="sxs-lookup"><span data-stu-id="17774-142">**File**</span></span>|<span data-ttu-id="17774-143">**Функция**</span><span class="sxs-lookup"><span data-stu-id="17774-143">**Function**</span></span>|<span data-ttu-id="17774-144">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="17774-144">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="17774-145">Мимапиформвиевер. cpp</span><span class="sxs-lookup"><span data-stu-id="17774-145">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="17774-146">Кмимапиформвиевер:: Жетвиевстатус</span><span class="sxs-lookup"><span data-stu-id="17774-146">CMyMAPIFormViewer::GetViewStatus</span></span>  <br/> |<span data-ttu-id="17774-147">MFCMAPI реализует метод **имапивиевконтекст:: жетвиевстатус** в этой функции.</span><span class="sxs-lookup"><span data-stu-id="17774-147">MFCMAPI implements the **IMAPIViewContext::GetViewStatus** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="17774-148">См. также</span><span class="sxs-lookup"><span data-stu-id="17774-148">See also</span></span>



[<span data-ttu-id="17774-149">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="17774-149">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="17774-150">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="17774-150">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)


[<span data-ttu-id="17774-151">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="17774-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

