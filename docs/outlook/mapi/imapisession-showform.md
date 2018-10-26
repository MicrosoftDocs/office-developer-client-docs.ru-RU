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
ms.openlocfilehash: e9e0ad958acc40dd28f3d9aab9996c1b7a36f38a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591487"
---
# <a name="imapisessionshowform"></a><span data-ttu-id="a1e2b-103">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="a1e2b-103">IMAPISession::ShowForm</span></span>

  
  
<span data-ttu-id="a1e2b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1e2b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1e2b-105">Отображает форму.</span><span class="sxs-lookup"><span data-stu-id="a1e2b-105">Displays a form.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="a1e2b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1e2b-106">Parameters</span></span>

 <span data-ttu-id="a1e2b-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a1e2b-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="a1e2b-108">[in] Дескриптор родительского окна формы.</span><span class="sxs-lookup"><span data-stu-id="a1e2b-108">[in] A handle to the parent window of the form.</span></span>
    
 <span data-ttu-id="a1e2b-109">_lpMsgStore_</span><span class="sxs-lookup"><span data-stu-id="a1e2b-109">_lpMsgStore_</span></span>
  
> <span data-ttu-id="a1e2b-110">[in] Указатель на хранилище сообщений, содержащем папку, на который указывает параметр _lpParentFolder_ .</span><span class="sxs-lookup"><span data-stu-id="a1e2b-110">[in] A pointer to the message store that contains the folder pointed to by the  _lpParentFolder_ parameter.</span></span> 
    
 <span data-ttu-id="a1e2b-111">_lpParentFolder_</span><span class="sxs-lookup"><span data-stu-id="a1e2b-111">_lpParentFolder_</span></span>
  
> <span data-ttu-id="a1e2b-112">[in] Указатель на папку, в котором был создан сообщения, связанного с параметром _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="a1e2b-112">[in] A pointer to the folder in which the message associated with the  _ulMessageToken_ parameter was created.</span></span> 
    
 <span data-ttu-id="a1e2b-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="a1e2b-113">_lpInterface_</span></span>
  
> <span data-ttu-id="a1e2b-114">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к сообщение, которое отображается в форме.</span><span class="sxs-lookup"><span data-stu-id="a1e2b-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message that is displayed in the form.</span></span> <span data-ttu-id="a1e2b-115">Параметр _lpInterface_ должен быть NULL или IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="a1e2b-115">The  _lpInterface_ parameter must be NULL or IID_IMessage.</span></span> <span data-ttu-id="a1e2b-116">В стандартный интерфейс [IMessage](imessageimapiprop.md)используется результаты передаче значения NULL.</span><span class="sxs-lookup"><span data-stu-id="a1e2b-116">Passing NULL results in the standard interface, [IMessage](imessageimapiprop.md), being used.</span></span> 
    
 <span data-ttu-id="a1e2b-117">_ulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="a1e2b-117">_ulMessageToken_</span></span>
  
> <span data-ttu-id="a1e2b-118">[in] Маркер, который связан с сообщение, отображаемое в форме.</span><span class="sxs-lookup"><span data-stu-id="a1e2b-118">[in] The token that is associated with the message to be displayed in the form.</span></span> <span data-ttu-id="a1e2b-119">Параметр _ulMessageToken_ должен иметь значение содержимого параметра _lpulMessageToken_ из предыдущего вызова [IMAPISession::PrepareForm](imapisession-prepareform.md).</span><span class="sxs-lookup"><span data-stu-id="a1e2b-119">The  _ulMessageToken_ parameter must be set to the contents of the  _lpulMessageToken_ parameter from the previous call to [IMAPISession::PrepareForm](imapisession-prepareform.md).</span></span>
    
 <span data-ttu-id="a1e2b-120">_lpMessageSent_</span><span class="sxs-lookup"><span data-stu-id="a1e2b-120">_lpMessageSent_</span></span>
  
> <span data-ttu-id="a1e2b-121">[in] Зарезервировано; должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="a1e2b-121">[in] Reserved; must be NULL.</span></span> 
    
 <span data-ttu-id="a1e2b-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a1e2b-122">_ulFlags_</span></span>
  
> <span data-ttu-id="a1e2b-123">[in] Битовая маска флаги, который определяет, как и ли сообщение сохраняется.</span><span class="sxs-lookup"><span data-stu-id="a1e2b-123">[in] A bitmask of flags that controls how and whether the message is saved.</span></span> <span data-ttu-id="a1e2b-124">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="a1e2b-124">The following flags can be set:</span></span>
    
<span data-ttu-id="a1e2b-125">MAPI_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="a1e2b-125">MAPI_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="a1e2b-126">Сообщения никогда не были сохранены (то есть, его [IMAPIProp::SaveChanges](imapiprop-savechanges.md) никогда не был вызван метод).</span><span class="sxs-lookup"><span data-stu-id="a1e2b-126">The message has never been saved (that is, its [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has never been called).</span></span> 
    
<span data-ttu-id="a1e2b-127">MAPI_POST_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="a1e2b-127">MAPI_POST_MESSAGE</span></span> 
  
> <span data-ttu-id="a1e2b-128">Сообщения должны сохраняться в родительской папки.</span><span class="sxs-lookup"><span data-stu-id="a1e2b-128">The message should be saved to its parent folder.</span></span> <span data-ttu-id="a1e2b-129">Сообщение не обрабатывается для отправки, но вместо этого он был отправлен в папку.</span><span class="sxs-lookup"><span data-stu-id="a1e2b-129">The message is not processed for sending but is posted to the folder instead.</span></span> <span data-ttu-id="a1e2b-130">Если этот флаг не установлен, сообщение копируется в папке "Исходящие" и обрабатывается для отправки.</span><span class="sxs-lookup"><span data-stu-id="a1e2b-130">If this flag is not set, the message is copied to the Outbox and is processed for sending.</span></span> 
    
 <span data-ttu-id="a1e2b-131">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="a1e2b-131">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="a1e2b-132">[in] Битовая маска флаги, скопированные из свойства **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) сообщения, связанный с маркером в параметре _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="a1e2b-132">[in] A bitmask of flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="a1e2b-133">Флаги предоставляют информацию о состоянии сообщения.</span><span class="sxs-lookup"><span data-stu-id="a1e2b-133">The flags provide information about the state of the message.</span></span> 
    
 <span data-ttu-id="a1e2b-134">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="a1e2b-134">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="a1e2b-135">[in] Битовая маска флаги, скопированные из свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) сообщения, связанный с маркером в параметре _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="a1e2b-135">[in] A bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="a1e2b-136">Эти флаги предоставляют информацию о состоянии сообщения.</span><span class="sxs-lookup"><span data-stu-id="a1e2b-136">These flags provide further information about the state of the message.</span></span> 
    
 <span data-ttu-id="a1e2b-137">_ulAccess_</span><span class="sxs-lookup"><span data-stu-id="a1e2b-137">_ulAccess_</span></span>
  
> <span data-ttu-id="a1e2b-138">[in] Флаг, указывающий уровень разрешений для сообщения, которое отображается в форме.</span><span class="sxs-lookup"><span data-stu-id="a1e2b-138">[in] A flag that indicates the permission level for the message that is displayed in the form.</span></span> <span data-ttu-id="a1e2b-139">Эта информация копируется из свойства **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) сообщения, связанный с маркером в параметре _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="a1e2b-139">This information is copied from the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
 <span data-ttu-id="a1e2b-140">_lpszMessageClass_</span><span class="sxs-lookup"><span data-stu-id="a1e2b-140">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="a1e2b-141">[in] Указатель на класс сообщения сообщения, отображаемого в форме, скопированные из свойства **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) сообщения, связанный с маркером в параметре _ulMessageToken_ .</span><span class="sxs-lookup"><span data-stu-id="a1e2b-141">[in] A pointer to the message class of the message being displayed in the form, copied from the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a1e2b-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a1e2b-142">Return value</span></span>

<span data-ttu-id="a1e2b-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="a1e2b-143">S_OK</span></span> 
  
> <span data-ttu-id="a1e2b-144">Успешно отобразить форму.</span><span class="sxs-lookup"><span data-stu-id="a1e2b-144">The form was successfully displayed.</span></span>
    
<span data-ttu-id="a1e2b-145">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="a1e2b-145">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="a1e2b-146">Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="a1e2b-146">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a1e2b-147">Замечания</span><span class="sxs-lookup"><span data-stu-id="a1e2b-147">Remarks</span></span>

<span data-ttu-id="a1e2b-148">Метод **IMAPISession::ShowForm** отображает форму сообщение, которое было подготовлено с помощью метода **IMAPISession::PrepareForm** .</span><span class="sxs-lookup"><span data-stu-id="a1e2b-148">The **IMAPISession::ShowForm** method displays a message form that has been prepared by the **IMAPISession::PrepareForm** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a1e2b-149">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a1e2b-149">Notes to callers</span></span>

<span data-ttu-id="a1e2b-150">Должен иметь только один ссылку на сообщение, переданной в параметре _lpMessage_ метод **PrepareForm** .</span><span class="sxs-lookup"><span data-stu-id="a1e2b-150">You should have only a single reference to the message passed in the **PrepareForm** method's  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="a1e2b-151">Обратите внимание, что реализации формы можно вернуть ошибочные значения не указаны, задокументированные с MAPI.</span><span class="sxs-lookup"><span data-stu-id="a1e2b-151">Be aware that form implementations can return error values other than the ones documented by MAPI.</span></span> <span data-ttu-id="a1e2b-152">Если значения этих ошибок можно использовать для более точные определения условия ошибки, сделайте это.</span><span class="sxs-lookup"><span data-stu-id="a1e2b-152">If you can use these error values to make a more accurate determination of the error condition, do so.</span></span> <span data-ttu-id="a1e2b-153">В противном случае обрабатывает эти ошибки, как обрабатывается MAPI_E_CALL_FAILED.</span><span class="sxs-lookup"><span data-stu-id="a1e2b-153">Otherwise, handle these errors as you would handle MAPI_E_CALL_FAILED.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a1e2b-154">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a1e2b-154">MFCMAPI reference</span></span>

<span data-ttu-id="a1e2b-155">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a1e2b-155">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a1e2b-156">**Файл**</span><span class="sxs-lookup"><span data-stu-id="a1e2b-156">**File**</span></span>|<span data-ttu-id="a1e2b-157">**Функция**</span><span class="sxs-lookup"><span data-stu-id="a1e2b-157">**Function**</span></span>|<span data-ttu-id="a1e2b-158">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="a1e2b-158">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a1e2b-159">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="a1e2b-159">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="a1e2b-160">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="a1e2b-160">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="a1e2b-161">Mfcmapi (en) использует метод **IMAPISession::ShowForm** вместе с методом **PrepareForm** для отображения сообщения в модальную форму.</span><span class="sxs-lookup"><span data-stu-id="a1e2b-161">MFCMAPI uses the **IMAPISession::ShowForm** method, together with the **PrepareForm** method, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a1e2b-162">См. также</span><span class="sxs-lookup"><span data-stu-id="a1e2b-162">See also</span></span>



[<span data-ttu-id="a1e2b-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="a1e2b-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="a1e2b-164">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a1e2b-164">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="a1e2b-165">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="a1e2b-165">IMAPISession::PrepareForm</span></span>](imapisession-prepareform.md)
  
[<span data-ttu-id="a1e2b-166">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a1e2b-166">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="a1e2b-167">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="a1e2b-167">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

