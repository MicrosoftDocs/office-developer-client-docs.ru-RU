---
title: IMessageSubmitMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SubmitMessage
api_type:
- COM
ms.assetid: 9ce93469-c55d-48d1-9abb-a637716ed4f2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 28786f483c4d2031c334d7b9697db7c5e627fe93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437366"
---
# <a name="imessagesubmitmessage"></a><span data-ttu-id="806a8-103">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="806a8-103">IMessage::SubmitMessage</span></span>

  
  
<span data-ttu-id="806a8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="806a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="806a8-105">Сохраняет все свойства сообщения и пометит сообщение как готовое к отправлению.</span><span class="sxs-lookup"><span data-stu-id="806a8-105">Saves all of the message's properties and marks the message as ready to be sent.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="806a8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="806a8-106">Parameters</span></span>

 <span data-ttu-id="806a8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="806a8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="806a8-108">[in] Битовая почта флагов, используемых для управления отправкой сообщения.</span><span class="sxs-lookup"><span data-stu-id="806a8-108">[in] Bitmask of flags used to control how a message is submitted.</span></span> <span data-ttu-id="806a8-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="806a8-109">The following flag can be set:</span></span>
    
<span data-ttu-id="806a8-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="806a8-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="806a8-111">MAPI должен немедленно отправить сообщение.</span><span class="sxs-lookup"><span data-stu-id="806a8-111">MAPI should submit the message immediately.</span></span> <span data-ttu-id="806a8-112">Этот флаг в настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="806a8-112">This flag is not currently in use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="806a8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="806a8-113">Return value</span></span>

<span data-ttu-id="806a8-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="806a8-114">S_OK</span></span> 
  
> <span data-ttu-id="806a8-115">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="806a8-115">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="806a8-116">MAPI_E_NO_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="806a8-116">MAPI_E_NO_RECIPIENTS</span></span> 
  
> <span data-ttu-id="806a8-117">Таблица получателей сообщения пуста.</span><span class="sxs-lookup"><span data-stu-id="806a8-117">The message's recipient table is empty.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="806a8-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="806a8-118">Remarks</span></span>

<span data-ttu-id="806a8-119">Метод **IMessage::SubmitMessage** пометит сообщение как готовое к передаче.</span><span class="sxs-lookup"><span data-stu-id="806a8-119">The **IMessage::SubmitMessage** method marks a message as ready to be transmitted.</span></span> <span data-ttu-id="806a8-120">MAPI передает сообщения в систему обмена сообщениями в том порядке, в котором они помечаются для отправки.</span><span class="sxs-lookup"><span data-stu-id="806a8-120">MAPI passes messages to the underlying messaging system in the order in which they are marked for sending.</span></span> <span data-ttu-id="806a8-121">Из-за этой функциональности сообщение может оставаться в хранилище сообщений в течение некоторого времени, прежде чем система обмена сообщениями сможет взять на себя за него ответственность.</span><span class="sxs-lookup"><span data-stu-id="806a8-121">Because of this functionality, a message might stay in a message store for some time before the underlying messaging system can take responsibility for it.</span></span> <span data-ttu-id="806a8-122">Порядок получения в месте назначения находится в системе управления системой обмена сообщениями и не обязательно соответствует порядку отправки сообщений.</span><span class="sxs-lookup"><span data-stu-id="806a8-122">The order of receipt at the destination is in the underlying messaging system's control and does not necessarily match the order in which messages were sent.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="806a8-123">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="806a8-123">Notes to implementers</span></span>

<span data-ttu-id="806a8-124">Вызовите метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сообщения, чтобы сохранить его, а затем **проверьте** свойство PR_MESSAGE_FLAGS [(PidTagMessageFlags).](pidtagmessageflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="806a8-124">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it and then check the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="806a8-125">Если установлен MSGFLAG_RESEND, вызовите [IMAPISupport::P repareSubmit.](imapisupport-preparesubmit.md)</span><span class="sxs-lookup"><span data-stu-id="806a8-125">If the MSGFLAG_RESEND flag is set, call [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md).</span></span> <span data-ttu-id="806a8-126">**PrepareSubmit** обновляет тип получателя **и PR_RESPONSIBILITY** ([PidTagResponsibility)](pidtagresponsibility-canonical-property.md)для всех получателей в повторном сообщении.</span><span class="sxs-lookup"><span data-stu-id="806a8-126">**PrepareSubmit** updates the recipient type and **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property for all of the recipients in the resend message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="806a8-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="806a8-127">Notes to callers</span></span>

<span data-ttu-id="806a8-128">При **возвращении SubmitMessage** все указатели на сообщение и связанные с ним подобекты сообщений, папок, вложений, потоков, таблиц и т. д. больше не являются допустимым.</span><span class="sxs-lookup"><span data-stu-id="806a8-128">When **SubmitMessage** returns, all pointers to the message and its associated subobjects messages, folders, attachments, streams, tables, and so on are no longer valid.</span></span> <span data-ttu-id="806a8-129">MAPI не разрешает дальнейшие операции с этими указателями, за исключением вызова методов **IUnknown::Release.**</span><span class="sxs-lookup"><span data-stu-id="806a8-129">MAPI does not permit any further operations on these pointers, except for calling their **IUnknown::Release** methods.</span></span> <span data-ttu-id="806a8-130">MAPI разработан таким образом, что после того как **будет вызвано решение SubmitMessage,** необходимо освободить сообщение и все связанные подпроекты.</span><span class="sxs-lookup"><span data-stu-id="806a8-130">MAPI is designed such that after **SubmitMessage** is called, you should release the message and all associated subobjects.</span></span> <span data-ttu-id="806a8-131">Однако если **SubmitMessage** возвращает значение ошибки, указывающее отсутствующие или недопустимые сведения, сообщение остается открытым, а указатели остаются действительными.</span><span class="sxs-lookup"><span data-stu-id="806a8-131">However, if **SubmitMessage** returns an error value indicating missing or invalid information, the message remains open and the pointers remain valid.</span></span> 
  
<span data-ttu-id="806a8-132">Чтобы отменить операцию отправки, получите и храните  указатель на свойство PR_ENTRYID[(PidTagEntryId)](pidtagentryid-canonical-property.md)перед отправкой сообщения.</span><span class="sxs-lookup"><span data-stu-id="806a8-132">To cancel a send operation, get and store a pointer to the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property before the message is submitted.</span></span> <span data-ttu-id="806a8-133">Так как идентификатор записи сообщения недействителен после отправки сообщения, его необходимо сохранить перед вызовом **SubmitMessage.**</span><span class="sxs-lookup"><span data-stu-id="806a8-133">Because a message's entry identifier is invalidated after the message has been submitted, it is necessary to save it before calling **SubmitMessage**.</span></span> <span data-ttu-id="806a8-134">Чтобы отменить отправку, направите _параметру lpEntryId_ этот идентификатор записи и вызовите [IMsgStore::AbortSubmit.](imsgstore-abortsubmit.md)</span><span class="sxs-lookup"><span data-stu-id="806a8-134">To cancel the send, point the  _lpEntryId_ parameter to this entry identifier and call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="806a8-135">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="806a8-135">MFCMAPI reference</span></span>

<span data-ttu-id="806a8-136">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="806a8-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="806a8-137">**Файл**</span><span class="sxs-lookup"><span data-stu-id="806a8-137">**File**</span></span>|<span data-ttu-id="806a8-138">**Функция**</span><span class="sxs-lookup"><span data-stu-id="806a8-138">**Function**</span></span>|<span data-ttu-id="806a8-139">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="806a8-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="806a8-140">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="806a8-140">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="806a8-141">**CFolderDlg::OnSubmitMessage**</span><span class="sxs-lookup"><span data-stu-id="806a8-141">**CFolderDlg::OnSubmitMessage**</span></span> <br/> |<span data-ttu-id="806a8-142">MFCMAPI использует метод **IMessage::SubmitMessage** для отправки выбранного сообщения.</span><span class="sxs-lookup"><span data-stu-id="806a8-142">MFCMAPI uses the **IMessage::SubmitMessage** method to submit the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="806a8-143">См. также</span><span class="sxs-lookup"><span data-stu-id="806a8-143">See also</span></span>



[<span data-ttu-id="806a8-144">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="806a8-144">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="806a8-145">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="806a8-145">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="806a8-146">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="806a8-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

