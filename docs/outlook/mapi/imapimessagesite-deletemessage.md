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
ms.openlocfilehash: da6de94342c8d8bbd378a3cde2fb065c97632291
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808959"
---
# <a name="imapimessagesitedeletemessage"></a><span data-ttu-id="08582-103">IMAPIMessageSite::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="08582-103">IMAPIMessageSite::DeleteMessage</span></span>

  
  
<span data-ttu-id="08582-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="08582-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="08582-105">Удаление текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="08582-105">Deletes the current message.</span></span>
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a><span data-ttu-id="08582-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="08582-106">Parameters</span></span>

 <span data-ttu-id="08582-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="08582-107">_pViewContext_</span></span>
  
> <span data-ttu-id="08582-108">[in] Указатель на объект контекста представления.</span><span class="sxs-lookup"><span data-stu-id="08582-108">[in] A pointer to a view context object.</span></span>
    
 <span data-ttu-id="08582-109">_prcPosRect_</span><span class="sxs-lookup"><span data-stu-id="08582-109">_prcPosRect_</span></span>
  
> <span data-ttu-id="08582-110">[in] Указатель на структуру [Прямоугольник](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) , содержащий положение и размер окна текущей формы.</span><span class="sxs-lookup"><span data-stu-id="08582-110">[in] A pointer to a [RECT](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) structure that contains the current form's window size and position.</span></span> <span data-ttu-id="08582-111">Далее форме, отображаемой также использует этот прямоугольник окна.</span><span class="sxs-lookup"><span data-stu-id="08582-111">The next form displayed also uses this window rectangle.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="08582-112">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="08582-112">Return value</span></span>

<span data-ttu-id="08582-113">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="08582-113">S_OK</span></span> 
  
> <span data-ttu-id="08582-114">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="08582-114">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="08582-115">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="08582-115">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="08582-116">Операция не поддерживается на этом сайте сообщения.</span><span class="sxs-lookup"><span data-stu-id="08582-116">The operation is not supported by this message site.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="08582-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="08582-117">Remarks</span></span>

<span data-ttu-id="08582-118">Объект формы вызывает метод **IMAPIMessageSite::DeleteMessage** для удаления сообщения, в настоящее время отображения формы.</span><span class="sxs-lookup"><span data-stu-id="08582-118">A form object calls the **IMAPIMessageSite::DeleteMessage** method to delete the message that the form is currently displaying.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="08582-119">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="08582-119">Notes to callers</span></span>

<span data-ttu-id="08582-120">После возврата **DeleteMessage**объекты формы необходимо проверить наличие новых сообщений и затем закрыть сами, если не существует.</span><span class="sxs-lookup"><span data-stu-id="08582-120">Following the return of **DeleteMessage**, form objects must check for a new message and then dismiss themselves if none exists.</span></span> <span data-ttu-id="08582-121">Чтобы определить, было ли сообщение, которое применяются **DeleteMessage** удаления или перемещения в папки " **Удаленные** ", объект формы может вызывать метод [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) , чтобы определить, был возвращен ли флаг DELETE_IS_MOVE.</span><span class="sxs-lookup"><span data-stu-id="08582-121">To determine whether the message **DeleteMessage** acted on was deleted or moved to a **Deleted Items** folder, a form object can call the [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method to determine whether the DELETE_IS_MOVE flag was returned.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="08582-122">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="08582-122">Notes to implementers</span></span>

<span data-ttu-id="08582-123">Если средство просмотра формы реализация метода **DeleteMessage** перемещается на следующее сообщение после удаляет сообщение, реализация должна вызовите метод [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) и передайте флаг VCDIR_DELETE перед выполнением Фактические удаления.</span><span class="sxs-lookup"><span data-stu-id="08582-123">If a form viewer's implementation of the **DeleteMessage** method moves to the next message after it deletes a message, the implementation should call the [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) method and pass the VCDIR_DELETE flag before performing the actual deletion.</span></span> <span data-ttu-id="08582-124">Если реализация средства просмотра формы **DeleteMessage** перемещение удаленных сообщений (например, для папки " **Удаленные** "), реализации необходимо сохранить изменения к сообщению, если сообщение было изменено.</span><span class="sxs-lookup"><span data-stu-id="08582-124">If a form viewer's implementation of **DeleteMessage** moves the deleted message (for example, to a **Deleted Items** folder), the implementation must save changes to the message if the message was modified.</span></span> 
  
<span data-ttu-id="08582-125">Типичное использование **DeleteMessage** выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="08582-125">A typical implementation of **DeleteMessage** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="08582-126">Если реализация перемещается сообщение, он вызывает метод [IPersistMessage::Save](ipersistmessage-save.md) , передав **значение null,** с помощью параметра _pMessage_ и **значение true,** с помощью параметра _fSameAsLoad_ .</span><span class="sxs-lookup"><span data-stu-id="08582-126">If the implementation is moving the message, it calls the [IPersistMessage::Save](ipersistmessage-save.md) method, passing **null** in the  _pMessage_ parameter and **true** in the  _fSameAsLoad_ parameter.</span></span> 
    
2. <span data-ttu-id="08582-127">Он вызывает метод **IMAPIViewContext::ActivateNext** , передав флаг VCDIR_DELETE с помощью параметра _ulDir_ .</span><span class="sxs-lookup"><span data-stu-id="08582-127">It calls the **IMAPIViewContext::ActivateNext** method, passing the VCDIR_DELETE flag in the  _ulDir_ parameter.</span></span> 
    
3. <span data-ttu-id="08582-128">Если происходит сбой вызова **ActivateNext** , возвращается.</span><span class="sxs-lookup"><span data-stu-id="08582-128">If the **ActivateNext** call fails, it returns.</span></span> <span data-ttu-id="08582-129">Если **ActivateNext** возвращает S_FALSE, он вызывает метод [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="08582-129">If **ActivateNext** returns S_FALSE, it calls the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method.</span></span> 
    
4. <span data-ttu-id="08582-130">Он удаляет или перемещает сообщение.</span><span class="sxs-lookup"><span data-stu-id="08582-130">It deletes or moves the message.</span></span>
    
<span data-ttu-id="08582-131">Для получения структуры **Прямоугольник** , используемых окно формы, вызовите функцию Windows [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) .</span><span class="sxs-lookup"><span data-stu-id="08582-131">To obtain the **RECT** structure used by a form's window, call the Windows [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) function.</span></span> 
  
<span data-ttu-id="08582-132">Список интерфейсы, связанные с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="08582-132">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="08582-133">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="08582-133">MFCMAPI reference</span></span>

<span data-ttu-id="08582-134">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="08582-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="08582-135">**����**</span><span class="sxs-lookup"><span data-stu-id="08582-135">**File**</span></span>|<span data-ttu-id="08582-136">**�������**</span><span class="sxs-lookup"><span data-stu-id="08582-136">**Function**</span></span>|<span data-ttu-id="08582-137">**�����������**</span><span class="sxs-lookup"><span data-stu-id="08582-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="08582-138">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="08582-138">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="08582-139">CMyMAPIFormViewer::DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="08582-139">CMyMAPIFormViewer::DeleteMessage</span></span>  <br/> |<span data-ttu-id="08582-140">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="08582-140">Not implemented.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="08582-141">См. также</span><span class="sxs-lookup"><span data-stu-id="08582-141">See also</span></span>



[<span data-ttu-id="08582-142">IMAPIMessageSite::GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="08582-142">IMAPIMessageSite::GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md)
  
[<span data-ttu-id="08582-143">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="08582-143">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="08582-144">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="08582-144">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="08582-145">IPersistMessage::Save</span><span class="sxs-lookup"><span data-stu-id="08582-145">IPersistMessage::Save</span></span>](ipersistmessage-save.md)
  
[<span data-ttu-id="08582-146">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="08582-146">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="08582-147">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="08582-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="08582-148">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="08582-148">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

