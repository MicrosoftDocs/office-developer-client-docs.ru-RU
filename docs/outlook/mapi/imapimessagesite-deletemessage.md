---
title: IMAPIMessageSiteDeleteMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.DeleteMessage
api_type:
- COM
ms.assetid: 09955996-b904-4c0d-8ba5-954a8875c055
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7b2761e20444c51d08380aee01c41eee797733eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321415"
---
# <a name="imapimessagesitedeletemessage"></a><span data-ttu-id="bbdc8-103">IMAPIMessageSite::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="bbdc8-103">IMAPIMessageSite::DeleteMessage</span></span>

  
  
<span data-ttu-id="bbdc8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbdc8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bbdc8-105">Удаляет текущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="bbdc8-105">Deletes the current message.</span></span>
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="bbdc8-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="bbdc8-106">Parameters</span></span>

 <span data-ttu-id="bbdc8-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="bbdc8-107">_pViewContext_</span></span>
  
> <span data-ttu-id="bbdc8-108">[in] Указатель на объект контекста представления.</span><span class="sxs-lookup"><span data-stu-id="bbdc8-108">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="bbdc8-109">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="bbdc8-109">_prcPosRect_</span></span>
  
> <span data-ttu-id="bbdc8-110">[in] Указатель на структуру [RECT,](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) которая содержит размер и положение окна текущей формы.</span><span class="sxs-lookup"><span data-stu-id="bbdc8-110">[in] A pointer to a [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="bbdc8-111">Следующая отображаемая форма также использует этот прямоугольник окна.</span><span class="sxs-lookup"><span data-stu-id="bbdc8-111">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bbdc8-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bbdc8-112">Return value</span></span>

<span data-ttu-id="bbdc8-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="bbdc8-113">S_OK</span></span> 
  
> <span data-ttu-id="bbdc8-114">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="bbdc8-114">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="bbdc8-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="bbdc8-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="bbdc8-116">Операция не поддерживается на этом сайте сообщений.</span><span class="sxs-lookup"><span data-stu-id="bbdc8-116">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bbdc8-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="bbdc8-117">Remarks</span></span>

<span data-ttu-id="bbdc8-118">Объект формы вызывает **метод IMAPIMessageSite::D eleteMessage,** чтобы удалить сообщение, которое отображается в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="bbdc8-118">A form object calls the **IMAPIMessageSite::DeleteMessage** method to delete the message that the form is currently displaying.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bbdc8-119">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="bbdc8-119">Notes to callers</span></span>

<span data-ttu-id="bbdc8-120">После возвращения **DeleteMessage** объекты формы должны проверить новое сообщение, а затем отклоняться, если их нет.</span><span class="sxs-lookup"><span data-stu-id="bbdc8-120">Following the return of **DeleteMessage**, form objects must check for a new message and then dismiss themselves if none exists.</span></span> <span data-ttu-id="bbdc8-121">Чтобы определить, было ли удалено или перемещено сообщение **DeleteMessage** в папку "Удаленные элементы", объект формы может вызвать [метод IMAPIMessageSite::GetSiteStatus,](imapimessagesite-getsitestatus.md) чтобы определить, был ли возвращен флаг DELETE_IS_MOVE. </span><span class="sxs-lookup"><span data-stu-id="bbdc8-121">To determine whether the message **DeleteMessage** acted on was deleted or moved to a **Deleted Items** folder, a form object can call the [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method to determine whether the DELETE_IS_MOVE flag was returned.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="bbdc8-122">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="bbdc8-122">Notes to implementers</span></span>

<span data-ttu-id="bbdc8-123">Если реализация метода **DeleteMessage** для просмотра формы перемещается к следующему сообщению после удаления сообщения, реализация должна вызвать метод [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) и передать флаг VCDIR_DELETE перед выполнением фактического удаления.</span><span class="sxs-lookup"><span data-stu-id="bbdc8-123">If a form viewer's implementation of the **DeleteMessage** method moves to the next message after it deletes a message, the implementation should call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method and pass the VCDIR_DELETE flag before performing the actual deletion.</span></span> <span data-ttu-id="bbdc8-124">Если реализация удаленных сообщений  (например, папки удаленных элементов) для  просмотра формы, реализация должна сохранить изменения в сообщении, если сообщение было изменено.</span><span class="sxs-lookup"><span data-stu-id="bbdc8-124">If a form viewer's implementation of **DeleteMessage** moves the deleted message (for example, to a **Deleted Items** folder), the implementation must save changes to the message if the message was modified.</span></span> 
  
<span data-ttu-id="bbdc8-125">Типичная реализация **DeleteMessage** выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="bbdc8-125">A typical implementation of **DeleteMessage** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="bbdc8-126">Если реализация перемещает сообщение, он вызывает [метод IPersistMessage::Save,](ipersistmessage-save.md) передавая **null** в _параметре pMessage_ и true **в** _параметре fSameAsLoad._</span><span class="sxs-lookup"><span data-stu-id="bbdc8-126">If the implementation is moving the message, it calls the [IPersistMessage::Save](ipersistmessage-save.md) method, passing **null** in the  _pMessage_ parameter and **true** in the  _fSameAsLoad_ parameter.</span></span> 
    
2. <span data-ttu-id="bbdc8-127">Он вызывает **метод IMAPIViewContext::ActivateNext,** передав флаг VCDIR_DELETE в _параметре ulDir._</span><span class="sxs-lookup"><span data-stu-id="bbdc8-127">It calls the **IMAPIViewContext::ActivateNext** method, passing the VCDIR_DELETE flag in the  _ulDir_ parameter.</span></span> 
    
3. <span data-ttu-id="bbdc8-128">Если вызов **ActivateNext** не удается, он возвращается.</span><span class="sxs-lookup"><span data-stu-id="bbdc8-128">If the **ActivateNext** call fails, it returns.</span></span> <span data-ttu-id="bbdc8-129">Если **activateNext** возвращает S_FALSE, он вызывает [метод IPersistMessage::HandsOffMessage.](ipersistmessage-handsoffmessage.md)</span><span class="sxs-lookup"><span data-stu-id="bbdc8-129">If **ActivateNext** returns S_FALSE, it calls the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method.</span></span> 
    
4. <span data-ttu-id="bbdc8-130">Он удаляет или перемещает сообщение.</span><span class="sxs-lookup"><span data-stu-id="bbdc8-130">It deletes or moves the message.</span></span>
    
<span data-ttu-id="bbdc8-131">Чтобы получить **структуру RECT,** используемую в окне формы, позвоните в Windows [GetWindowRect.](https://msdn.microsoft.com/library/ms633519)</span><span class="sxs-lookup"><span data-stu-id="bbdc8-131">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](https://msdn.microsoft.com/library/ms633519) function.</span></span> 
  
<span data-ttu-id="bbdc8-132">Список интерфейсов, связанных с серверами форм, см. в [перечне интерфейсов форм MAPI.](mapi-form-interfaces.md)</span><span class="sxs-lookup"><span data-stu-id="bbdc8-132">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bbdc8-133">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="bbdc8-133">MFCMAPI reference</span></span>

<span data-ttu-id="bbdc8-134">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="bbdc8-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bbdc8-135">**Файл**</span><span class="sxs-lookup"><span data-stu-id="bbdc8-135">**File**</span></span>|<span data-ttu-id="bbdc8-136">**Функция**</span><span class="sxs-lookup"><span data-stu-id="bbdc8-136">**Function**</span></span>|<span data-ttu-id="bbdc8-137">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="bbdc8-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bbdc8-138">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="bbdc8-138">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="bbdc8-139">CMyMAPIFormViewer::D eleteMessage</span><span class="sxs-lookup"><span data-stu-id="bbdc8-139">CMyMAPIFormViewer::DeleteMessage</span></span>  <br/> |<span data-ttu-id="bbdc8-140">Не реализовано.</span><span class="sxs-lookup"><span data-stu-id="bbdc8-140">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bbdc8-141">См. также</span><span class="sxs-lookup"><span data-stu-id="bbdc8-141">See also</span></span>



[<span data-ttu-id="bbdc8-142">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="bbdc8-142">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="bbdc8-143">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="bbdc8-143">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="bbdc8-144">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="bbdc8-144">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="bbdc8-145">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="bbdc8-145">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="bbdc8-146">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bbdc8-146">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="bbdc8-147">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="bbdc8-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="bbdc8-148">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="bbdc8-148">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

