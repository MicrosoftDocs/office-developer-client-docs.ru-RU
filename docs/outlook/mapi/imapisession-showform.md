---
title: IMAPISessionShowForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.ShowForm
api_type:
- COM
ms.assetid: 233cf936-34db-42d4-b5e3-17a93acb2009
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8b90dee3958a20994f9a60d104ae714ad95307d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412529"
---
# <a name="imapisessionshowform"></a><span data-ttu-id="f6366-103">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="f6366-103">IMAPISession::ShowForm</span></span>

  
  
<span data-ttu-id="f6366-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6366-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6366-105">Отображает форму.</span><span class="sxs-lookup"><span data-stu-id="f6366-105">Displays a form.</span></span>
  
```cpp
HRESULT ShowForm(
  ULONG_PTR ulUIParam,
  LPMDB lpMsgStore,
  LPMAPIFOLDER lpParentFolder,
  LPCIID lpInterface,
  ULONG ulMessageToken,
  LPMESSAGE lpMessageSent,
  ULONG ulFlags,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  ULONG ulAccess,
  LPSTR lpszMessageClass
);
```

## <a name="parameters"></a><span data-ttu-id="f6366-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6366-106">Parameters</span></span>

 <span data-ttu-id="f6366-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f6366-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="f6366-108">[in] Handle to the parent window of the form.</span><span class="sxs-lookup"><span data-stu-id="f6366-108">[in] A handle to the parent window of the form.</span></span>
    
 <span data-ttu-id="f6366-109">_lpMsgStore_</span><span class="sxs-lookup"><span data-stu-id="f6366-109">_lpMsgStore_</span></span>
  
> <span data-ttu-id="f6366-110">[in] Указатель на хранилище сообщений, которое содержит папку, на которую указывает параметр _lpParentFolder._</span><span class="sxs-lookup"><span data-stu-id="f6366-110">[in] A pointer to the message store that contains the folder pointed to by the  _lpParentFolder_ parameter.</span></span> 
    
 <span data-ttu-id="f6366-111">_lpParentFolder_</span><span class="sxs-lookup"><span data-stu-id="f6366-111">_lpParentFolder_</span></span>
  
> <span data-ttu-id="f6366-112">[in] Указатель на папку, в которой было создано сообщение, связанное с параметром _ulMessageToken._</span><span class="sxs-lookup"><span data-stu-id="f6366-112">[in] A pointer to the folder in which the message associated with the  _ulMessageToken_ parameter was created.</span></span> 
    
 <span data-ttu-id="f6366-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="f6366-113">_lpInterface_</span></span>
  
> <span data-ttu-id="f6366-114">[in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, который будет использоваться для доступа к сообщению, которое отображается в форме.</span><span class="sxs-lookup"><span data-stu-id="f6366-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message that is displayed in the form.</span></span> <span data-ttu-id="f6366-115">Параметр  _lpInterface_ должен иметь NULL или IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="f6366-115">The  _lpInterface_ parameter must be NULL or IID_IMessage.</span></span> <span data-ttu-id="f6366-116">Передача NULL приводит к использования [стандартного интерфейса IMessage.](imessageimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="f6366-116">Passing NULL results in the standard interface, [IMessage](imessageimapiprop.md), being used.</span></span> 
    
 <span data-ttu-id="f6366-117">_ulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="f6366-117">_ulMessageToken_</span></span>
  
> <span data-ttu-id="f6366-118">[in] Маркер, связанный с сообщением для отображения в форме.</span><span class="sxs-lookup"><span data-stu-id="f6366-118">[in] The token that is associated with the message to be displayed in the form.</span></span> <span data-ttu-id="f6366-119">Параметр _ulMessageToken_ должен иметь содержимое параметра _lpulMessageToken_ из предыдущего вызова [IMAPISession::P repareForm.](imapisession-prepareform.md)</span><span class="sxs-lookup"><span data-stu-id="f6366-119">The  _ulMessageToken_ parameter must be set to the contents of the  _lpulMessageToken_ parameter from the previous call to [IMAPISession::PrepareForm](imapisession-prepareform.md).</span></span>
    
 <span data-ttu-id="f6366-120">_lpMessageSent_</span><span class="sxs-lookup"><span data-stu-id="f6366-120">_lpMessageSent_</span></span>
  
> <span data-ttu-id="f6366-121">[in] Зарезервировано; должно быть NULL.</span><span class="sxs-lookup"><span data-stu-id="f6366-121">[in] Reserved; must be NULL.</span></span> 
    
 <span data-ttu-id="f6366-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f6366-122">_ulFlags_</span></span>
  
> <span data-ttu-id="f6366-123">[in] Битоваяmas флагов, которая управляет тем, как и является ли сообщение сохраненным.</span><span class="sxs-lookup"><span data-stu-id="f6366-123">[in] A bitmask of flags that controls how and whether the message is saved.</span></span> <span data-ttu-id="f6366-124">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="f6366-124">The following flags can be set:</span></span>
    
<span data-ttu-id="f6366-125">MAPI_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="f6366-125">MAPI_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="f6366-126">Сообщение никогда не было сохранено (то есть его метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) никогда не был вызван).</span><span class="sxs-lookup"><span data-stu-id="f6366-126">The message has never been saved (that is, its [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has never been called).</span></span> 
    
<span data-ttu-id="f6366-127">MAPI_POST_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="f6366-127">MAPI_POST_MESSAGE</span></span> 
  
> <span data-ttu-id="f6366-128">Сообщение должно быть сохранено в родительской папке.</span><span class="sxs-lookup"><span data-stu-id="f6366-128">The message should be saved to its parent folder.</span></span> <span data-ttu-id="f6366-129">Сообщение не обрабатывается для отправки, а отправляется в папку.</span><span class="sxs-lookup"><span data-stu-id="f6366-129">The message is not processed for sending but is posted to the folder instead.</span></span> <span data-ttu-id="f6366-130">Если этот флаг не установлен, сообщение копируется в почтовый ящик и обрабатывается для отправки.</span><span class="sxs-lookup"><span data-stu-id="f6366-130">If this flag is not set, the message is copied to the Outbox and is processed for sending.</span></span> 
    
 <span data-ttu-id="f6366-131">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="f6366-131">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="f6366-132">[in] Битоваяmas флагов, скопированная из свойства **PR_MSG_STATUS** ([PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)сообщения, связанного с маркером в параметре _ulMessageToken._</span><span class="sxs-lookup"><span data-stu-id="f6366-132">[in] A bitmask of flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="f6366-133">Флаги предоставляют сведения о состоянии сообщения.</span><span class="sxs-lookup"><span data-stu-id="f6366-133">The flags provide information about the state of the message.</span></span> 
    
 <span data-ttu-id="f6366-134">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="f6366-134">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="f6366-135">[in] Битоваяmas флагов, скопированная из свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)сообщения, связанного с маркером в параметре _ulMessageToken._</span><span class="sxs-lookup"><span data-stu-id="f6366-135">[in] A bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="f6366-136">Эти флаги предоставляют дополнительные сведения о состоянии сообщения.</span><span class="sxs-lookup"><span data-stu-id="f6366-136">These flags provide further information about the state of the message.</span></span> 
    
 <span data-ttu-id="f6366-137">_ulAccess_</span><span class="sxs-lookup"><span data-stu-id="f6366-137">_ulAccess_</span></span>
  
> <span data-ttu-id="f6366-138">[in] Флаг, который указывает уровень разрешений для сообщения, отображаемой в форме.</span><span class="sxs-lookup"><span data-stu-id="f6366-138">[in] A flag that indicates the permission level for the message that is displayed in the form.</span></span> <span data-ttu-id="f6366-139">Эти сведения копируются из свойства **PR_ACCESS** ([PidTagAccess)](pidtagaccess-canonical-property.md)сообщения, связанного с маркером в параметре _ulMessageToken._</span><span class="sxs-lookup"><span data-stu-id="f6366-139">This information is copied from the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
 <span data-ttu-id="f6366-140">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="f6366-140">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="f6366-141">[in] Указатель на класс сообщения, отображаемого в форме, **скопирован** из свойства PR_MESSAGE_CLASS ([PidTagMessageClass)](pidtagmessageclass-canonical-property.md)сообщения, связанного с маркером в параметре _ulMessageToken._</span><span class="sxs-lookup"><span data-stu-id="f6366-141">[in] A pointer to the message class of the message being displayed in the form, copied from the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f6366-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6366-142">Return value</span></span>

<span data-ttu-id="f6366-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="f6366-143">S_OK</span></span> 
  
> <span data-ttu-id="f6366-144">Форма успешно отобрана.</span><span class="sxs-lookup"><span data-stu-id="f6366-144">The form was successfully displayed.</span></span>
    
<span data-ttu-id="f6366-145">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="f6366-145">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="f6366-146">Пользователь отменил операцию, обычно нажав  кнопку "Отмена" в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="f6366-146">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f6366-147">Примечания</span><span class="sxs-lookup"><span data-stu-id="f6366-147">Remarks</span></span>

<span data-ttu-id="f6366-148">Метод **IMAPISession::ShowForm** отображает форму сообщения, подготовленную методом **IMAPISession::P repareForm.**</span><span class="sxs-lookup"><span data-stu-id="f6366-148">The **IMAPISession::ShowForm** method displays a message form that has been prepared by the **IMAPISession::PrepareForm** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f6366-149">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="f6366-149">Notes to callers</span></span>

<span data-ttu-id="f6366-150">В параметре _lpMessage_ метода **PrepareForm** должна быть только одна ссылка на сообщение.</span><span class="sxs-lookup"><span data-stu-id="f6366-150">You should have only a single reference to the message passed in the **PrepareForm** method's  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="f6366-151">Следует помнить, что реализации форм могут возвращать значения ошибок, кроме значений, задокументированных в MAPI.</span><span class="sxs-lookup"><span data-stu-id="f6366-151">Be aware that form implementations can return error values other than the ones documented by MAPI.</span></span> <span data-ttu-id="f6366-152">Если эти значения ошибки можно использовать для более точного определения условия ошибки, сделайте это.</span><span class="sxs-lookup"><span data-stu-id="f6366-152">If you can use these error values to make a more accurate determination of the error condition, do so.</span></span> <span data-ttu-id="f6366-153">В противном случае обработать эти ошибки так же, как и MAPI_E_CALL_FAILED.</span><span class="sxs-lookup"><span data-stu-id="f6366-153">Otherwise, handle these errors as you would handle MAPI_E_CALL_FAILED.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f6366-154">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f6366-154">MFCMAPI reference</span></span>

<span data-ttu-id="f6366-155">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="f6366-155">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f6366-156">**Файл**</span><span class="sxs-lookup"><span data-stu-id="f6366-156">**File**</span></span>|<span data-ttu-id="f6366-157">**Функция**</span><span class="sxs-lookup"><span data-stu-id="f6366-157">**Function**</span></span>|<span data-ttu-id="f6366-158">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="f6366-158">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f6366-159">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="f6366-159">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="f6366-160">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="f6366-160">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="f6366-161">MFCMAPI использует метод **IMAPISession::ShowForm** вместе с методом **PrepareForm** для отображения сообщения в модальной форме.</span><span class="sxs-lookup"><span data-stu-id="f6366-161">MFCMAPI uses the **IMAPISession::ShowForm** method, together with the **PrepareForm** method, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f6366-162">См. также</span><span class="sxs-lookup"><span data-stu-id="f6366-162">See also</span></span>



[<span data-ttu-id="f6366-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="f6366-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="f6366-164">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f6366-164">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="f6366-165">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="f6366-165">IMAPISession::PrepareForm</span></span>](imapisession-prepareform.md)
  
[<span data-ttu-id="f6366-166">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f6366-166">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="f6366-167">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="f6366-167">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

