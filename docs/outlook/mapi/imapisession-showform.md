---
title: имаписессионшовформ
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
# <a name="imapisessionshowform"></a><span data-ttu-id="d157c-103">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="d157c-103">IMAPISession::ShowForm</span></span>

  
  
<span data-ttu-id="d157c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d157c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d157c-105">Отображает форму.</span><span class="sxs-lookup"><span data-stu-id="d157c-105">Displays a form.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="d157c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d157c-106">Parameters</span></span>

 <span data-ttu-id="d157c-107">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="d157c-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="d157c-108">возврата Дескриптор родительского окна формы.</span><span class="sxs-lookup"><span data-stu-id="d157c-108">[in] A handle to the parent window of the form.</span></span>
    
 <span data-ttu-id="d157c-109">_лпмсгсторе_</span><span class="sxs-lookup"><span data-stu-id="d157c-109">_lpMsgStore_</span></span>
  
> <span data-ttu-id="d157c-110">возврата Указатель на хранилище сообщений, содержащее папку, на которую указывает параметр _лппарентфолдер_ .</span><span class="sxs-lookup"><span data-stu-id="d157c-110">[in] A pointer to the message store that contains the folder pointed to by the  _lpParentFolder_ parameter.</span></span> 
    
 <span data-ttu-id="d157c-111">_лппарентфолдер_</span><span class="sxs-lookup"><span data-stu-id="d157c-111">_lpParentFolder_</span></span>
  
> <span data-ttu-id="d157c-112">возврата Указатель на папку, в которой было создано сообщение, связанное с параметром _улмессажетокен_ .</span><span class="sxs-lookup"><span data-stu-id="d157c-112">[in] A pointer to the folder in which the message associated with the  _ulMessageToken_ parameter was created.</span></span> 
    
 <span data-ttu-id="d157c-113">_лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="d157c-113">_lpInterface_</span></span>
  
> <span data-ttu-id="d157c-114">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к сообщению, отображаемому в форме.</span><span class="sxs-lookup"><span data-stu-id="d157c-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message that is displayed in the form.</span></span> <span data-ttu-id="d157c-115">Параметр _лпинтерфаце_ должен иметь значение NULL или IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="d157c-115">The  _lpInterface_ parameter must be NULL or IID_IMessage.</span></span> <span data-ttu-id="d157c-116">Передача значений NULL в стандартный интерфейс [iMessage](imessageimapiprop.md)используется.</span><span class="sxs-lookup"><span data-stu-id="d157c-116">Passing NULL results in the standard interface, [IMessage](imessageimapiprop.md), being used.</span></span> 
    
 <span data-ttu-id="d157c-117">_улмессажетокен_</span><span class="sxs-lookup"><span data-stu-id="d157c-117">_ulMessageToken_</span></span>
  
> <span data-ttu-id="d157c-118">возврата Маркер, связанный с сообщением, которое должно отображаться в форме.</span><span class="sxs-lookup"><span data-stu-id="d157c-118">[in] The token that is associated with the message to be displayed in the form.</span></span> <span data-ttu-id="d157c-119">Параметру _улмессажетокен_ должно быть присвоено значение параметра _лпулмессажетокен_ из предыдущего вызова [IMAPISession::P репареформ](imapisession-prepareform.md).</span><span class="sxs-lookup"><span data-stu-id="d157c-119">The  _ulMessageToken_ parameter must be set to the contents of the  _lpulMessageToken_ parameter from the previous call to [IMAPISession::PrepareForm](imapisession-prepareform.md).</span></span>
    
 <span data-ttu-id="d157c-120">_лпмессажесент_</span><span class="sxs-lookup"><span data-stu-id="d157c-120">_lpMessageSent_</span></span>
  
> <span data-ttu-id="d157c-121">возврата Резервирования должно иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="d157c-121">[in] Reserved; must be NULL.</span></span> 
    
 <span data-ttu-id="d157c-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d157c-122">_ulFlags_</span></span>
  
> <span data-ttu-id="d157c-123">возврата Битовая маска флагов, определяющих способ и способ сохранения сообщения.</span><span class="sxs-lookup"><span data-stu-id="d157c-123">[in] A bitmask of flags that controls how and whether the message is saved.</span></span> <span data-ttu-id="d157c-124">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="d157c-124">The following flags can be set:</span></span>
    
<span data-ttu-id="d157c-125">MAPI_NEW_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="d157c-125">MAPI_NEW_MESSAGE</span></span> 
  
> <span data-ttu-id="d157c-126">Сообщение никогда не сохранялось (то есть метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) не вызывался).</span><span class="sxs-lookup"><span data-stu-id="d157c-126">The message has never been saved (that is, its [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method has never been called).</span></span> 
    
<span data-ttu-id="d157c-127">MAPI_POST_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="d157c-127">MAPI_POST_MESSAGE</span></span> 
  
> <span data-ttu-id="d157c-128">Сообщение должно быть сохранено в родительской папке.</span><span class="sxs-lookup"><span data-stu-id="d157c-128">The message should be saved to its parent folder.</span></span> <span data-ttu-id="d157c-129">Сообщение не обрабатывается для отправки, но вместо этого отправляется в папку.</span><span class="sxs-lookup"><span data-stu-id="d157c-129">The message is not processed for sending but is posted to the folder instead.</span></span> <span data-ttu-id="d157c-130">Если этот флаг не установлен, сообщение копируется в папку "Исходящие" и обрабатывается для отправки.</span><span class="sxs-lookup"><span data-stu-id="d157c-130">If this flag is not set, the message is copied to the Outbox and is processed for sending.</span></span> 
    
 <span data-ttu-id="d157c-131">_улмессажестатус_</span><span class="sxs-lookup"><span data-stu-id="d157c-131">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="d157c-132">возврата Битовая маска флагов, скопированных из свойства **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) сообщения, связанного с маркером в параметре _улмессажетокен_ .</span><span class="sxs-lookup"><span data-stu-id="d157c-132">[in] A bitmask of flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="d157c-133">Флаги предоставляют сведения о состоянии сообщения.</span><span class="sxs-lookup"><span data-stu-id="d157c-133">The flags provide information about the state of the message.</span></span> 
    
 <span data-ttu-id="d157c-134">_улмессажефлагс_</span><span class="sxs-lookup"><span data-stu-id="d157c-134">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="d157c-135">возврата Битовая маска флагов, скопированных из свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) сообщения, связанного с маркером в параметре _улмессажетокен_ .</span><span class="sxs-lookup"><span data-stu-id="d157c-135">[in] A bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> <span data-ttu-id="d157c-136">Эти флаги предоставляют дополнительные сведения о состоянии сообщения.</span><span class="sxs-lookup"><span data-stu-id="d157c-136">These flags provide further information about the state of the message.</span></span> 
    
 <span data-ttu-id="d157c-137">_улакцесс_</span><span class="sxs-lookup"><span data-stu-id="d157c-137">_ulAccess_</span></span>
  
> <span data-ttu-id="d157c-138">возврата Флаг, указывающий уровень разрешений для сообщения, отображаемого в форме.</span><span class="sxs-lookup"><span data-stu-id="d157c-138">[in] A flag that indicates the permission level for the message that is displayed in the form.</span></span> <span data-ttu-id="d157c-139">Эти сведения копируются из свойства **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) сообщения, связанного с маркером, в параметре _улмессажетокен_ .</span><span class="sxs-lookup"><span data-stu-id="d157c-139">This information is copied from the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
 <span data-ttu-id="d157c-140">_лпсзмессажекласс_</span><span class="sxs-lookup"><span data-stu-id="d157c-140">_lpszMessageClass_</span></span>
  
> <span data-ttu-id="d157c-141">возврата Указатель на класс сообщения, отображаемый в форме, скопированный из свойства **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) сообщения, связанного с маркером в параметре _улмессажетокен_ .</span><span class="sxs-lookup"><span data-stu-id="d157c-141">[in] A pointer to the message class of the message being displayed in the form, copied from the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message associated with the token in the  _ulMessageToken_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d157c-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d157c-142">Return value</span></span>

<span data-ttu-id="d157c-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="d157c-143">S_OK</span></span> 
  
> <span data-ttu-id="d157c-144">Форма успешно отображена.</span><span class="sxs-lookup"><span data-stu-id="d157c-144">The form was successfully displayed.</span></span>
    
<span data-ttu-id="d157c-145">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="d157c-145">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="d157c-146">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="d157c-146">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d157c-147">Примечания</span><span class="sxs-lookup"><span data-stu-id="d157c-147">Remarks</span></span>

<span data-ttu-id="d157c-148">Метод **IMAPISession:: шовформ** отображает форму сообщения, подготовленную методом **IMAPISession::P репареформ** .</span><span class="sxs-lookup"><span data-stu-id="d157c-148">The **IMAPISession::ShowForm** method displays a message form that has been prepared by the **IMAPISession::PrepareForm** method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d157c-149">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="d157c-149">Notes to callers</span></span>

<span data-ttu-id="d157c-150">Вы должны иметь только одну ссылку на сообщение, переданное в параметре _лпмессаже_ метода **препареформ** .</span><span class="sxs-lookup"><span data-stu-id="d157c-150">You should have only a single reference to the message passed in the **PrepareForm** method's  _lpMessage_ parameter.</span></span> 
  
<span data-ttu-id="d157c-151">Имейте в виду, что реализации форм могут возвращать значения ошибок, отличные от тех, которые задокументированы MAPI.</span><span class="sxs-lookup"><span data-stu-id="d157c-151">Be aware that form implementations can return error values other than the ones documented by MAPI.</span></span> <span data-ttu-id="d157c-152">Если вы можете использовать эти значения ошибок для более точного определения условия ошибки, сделайте это.</span><span class="sxs-lookup"><span data-stu-id="d157c-152">If you can use these error values to make a more accurate determination of the error condition, do so.</span></span> <span data-ttu-id="d157c-153">В противном случае обработайте эти ошибки так же, как при обработке MAPI_E_CALL_FAILED.</span><span class="sxs-lookup"><span data-stu-id="d157c-153">Otherwise, handle these errors as you would handle MAPI_E_CALL_FAILED.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d157c-154">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d157c-154">MFCMAPI reference</span></span>

<span data-ttu-id="d157c-155">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="d157c-155">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d157c-156">**Файл**</span><span class="sxs-lookup"><span data-stu-id="d157c-156">**File**</span></span>|<span data-ttu-id="d157c-157">**Функция**</span><span class="sxs-lookup"><span data-stu-id="d157c-157">**Function**</span></span>|<span data-ttu-id="d157c-158">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="d157c-158">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d157c-159">Мапиформфунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="d157c-159">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="d157c-160">опенмессажемодал</span><span class="sxs-lookup"><span data-stu-id="d157c-160">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="d157c-161">MFCMAPI использует метод **IMAPISession:: шовформ** вместе с методом **препареформ** для отображения сообщения в модальной форме.</span><span class="sxs-lookup"><span data-stu-id="d157c-161">MFCMAPI uses the **IMAPISession::ShowForm** method, together with the **PrepareForm** method, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d157c-162">См. также</span><span class="sxs-lookup"><span data-stu-id="d157c-162">See also</span></span>



[<span data-ttu-id="d157c-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="d157c-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="d157c-164">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d157c-164">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
  
[<span data-ttu-id="d157c-165">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="d157c-165">IMAPISession::PrepareForm</span></span>](imapisession-prepareform.md)
  
[<span data-ttu-id="d157c-166">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d157c-166">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="d157c-167">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="d157c-167">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

