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
ms.openlocfilehash: 1d325c67c836e727d8285bd2dceecf88bf68327c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809277"
---
# <a name="imessagesubmitmessage"></a><span data-ttu-id="10b18-103">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="10b18-103">IMessage::SubmitMessage</span></span>

  
  
<span data-ttu-id="10b18-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="10b18-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="10b18-105">Сохраняет все свойства сообщений и помечает сообщения как Готово к отправке.</span><span class="sxs-lookup"><span data-stu-id="10b18-105">Saves all of the message's properties and marks the message as ready to be sent.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="10b18-106">���������</span><span class="sxs-lookup"><span data-stu-id="10b18-106">Parameters</span></span>

 <span data-ttu-id="10b18-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="10b18-107">_ulFlags_</span></span>
  
> <span data-ttu-id="10b18-108">[in] Битовая маска флаги, используемые для управления, как отправить сообщение.</span><span class="sxs-lookup"><span data-stu-id="10b18-108">[in] Bitmask of flags used to control how a message is submitted.</span></span> <span data-ttu-id="10b18-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="10b18-109">The following flag can be set:</span></span>
    
<span data-ttu-id="10b18-110">FORCE_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="10b18-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="10b18-111">MAPI следует отправить сообщение немедленно.</span><span class="sxs-lookup"><span data-stu-id="10b18-111">MAPI should submit the message immediately.</span></span> <span data-ttu-id="10b18-112">Этот флаг не в настоящее время используется.</span><span class="sxs-lookup"><span data-stu-id="10b18-112">This flag is not currently in use.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="10b18-113">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="10b18-113">Return value</span></span>

<span data-ttu-id="10b18-114">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="10b18-114">S_OK</span></span> 
  
> <span data-ttu-id="10b18-115">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="10b18-115">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="10b18-116">MAPI_E_NO_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="10b18-116">MAPI_E_NO_RECIPIENTS</span></span> 
  
> <span data-ttu-id="10b18-117">Таблица получателей сообщения будет пустым.</span><span class="sxs-lookup"><span data-stu-id="10b18-117">The message's recipient table is empty.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="10b18-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="10b18-118">Remarks</span></span>

<span data-ttu-id="10b18-119">Метод **IMessage::SubmitMessage** помечает сообщения как готовые для передачи.</span><span class="sxs-lookup"><span data-stu-id="10b18-119">The **IMessage::SubmitMessage** method marks a message as ready to be transmitted.</span></span> <span data-ttu-id="10b18-120">MAPI передает сообщения системы обмена сообщениями в том порядке, в котором они помечены как для отправки.</span><span class="sxs-lookup"><span data-stu-id="10b18-120">MAPI passes messages to the underlying messaging system in the order in which they are marked for sending.</span></span> <span data-ttu-id="10b18-121">Из-за эту функцию сообщение может оставаться в хранилище сообщений некоторое время вступления системы обмена сообщениями ответственность за его.</span><span class="sxs-lookup"><span data-stu-id="10b18-121">Because of this functionality, a message might stay in a message store for some time before the underlying messaging system can take responsibility for it.</span></span> <span data-ttu-id="10b18-122">Порядок получения в месте назначения находится в базовом обмена сообщениями системы управления и не соответствует порядке, в котором отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="10b18-122">The order of receipt at the destination is in the underlying messaging system's control and does not necessarily match the order in which messages were sent.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="10b18-123">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="10b18-123">Notes to implementers</span></span>

<span data-ttu-id="10b18-124">Вызов метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сообщения, сохраните его и проверьте свойство message **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="10b18-124">Call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to save it and then check the message's **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property.</span></span> <span data-ttu-id="10b18-125">Если значение флага MSGFLAG_RESEND, вызовите [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md).</span><span class="sxs-lookup"><span data-stu-id="10b18-125">If the MSGFLAG_RESEND flag is set, call [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md).</span></span> <span data-ttu-id="10b18-126">**PrepareSubmit** обновления тип получателя и свойство **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) для всех получателей в повторная отправка сообщений.</span><span class="sxs-lookup"><span data-stu-id="10b18-126">**PrepareSubmit** updates the recipient type and **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property for all of the recipients in the resend message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="10b18-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="10b18-127">Notes to callers</span></span>

<span data-ttu-id="10b18-128">При возврате **SubmitMessage** , все указатели на сообщение и его сообщения связанных вложенных папок, вложения, потоки, таблицы и т. п. недействительны.</span><span class="sxs-lookup"><span data-stu-id="10b18-128">When **SubmitMessage** returns, all pointers to the message and its associated subobjects messages, folders, attachments, streams, tables, and so on are no longer valid.</span></span> <span data-ttu-id="10b18-129">MAPI не разрешает любых дополнительных операций на эти указатели, за исключением вызова их методов **функции IUnknown::Release** .</span><span class="sxs-lookup"><span data-stu-id="10b18-129">MAPI does not permit any further operations on these pointers, except for calling their **IUnknown::Release** methods.</span></span> <span data-ttu-id="10b18-130">Таким образом, что после вызова **SubmitMessage** освобождение сообщения и все связанные с ним вложенных предоставляет MAPI.</span><span class="sxs-lookup"><span data-stu-id="10b18-130">MAPI is designed such that after **SubmitMessage** is called, you should release the message and all associated subobjects.</span></span> <span data-ttu-id="10b18-131">Тем не менее если **SubmitMessage** возвращает значение, указывающее, отсутствующие или недопустимые данные ошибки, сообщение открыто и указатели остаются действительными.</span><span class="sxs-lookup"><span data-stu-id="10b18-131">However, if **SubmitMessage** returns an error value indicating missing or invalid information, the message remains open and the pointers remain valid.</span></span> 
  
<span data-ttu-id="10b18-132">Чтобы отменить операцию отправки, получения и хранения указатель свойство message **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) перед отправкой сообщения.</span><span class="sxs-lookup"><span data-stu-id="10b18-132">To cancel a send operation, get and store a pointer to the message's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property before the message is submitted.</span></span> <span data-ttu-id="10b18-133">Так как идентификатор записи сообщения недействительными после отправки сообщения, это необходимо для сохранения до вызова метода **SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="10b18-133">Because a message's entry identifier is invalidated after the message has been submitted, it is necessary to save it before calling **SubmitMessage**.</span></span> <span data-ttu-id="10b18-134">Чтобы отменить отправить, выберите параметр _lpEntryId_ этот идентификатор записи и вызова [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).</span><span class="sxs-lookup"><span data-stu-id="10b18-134">To cancel the send, point the  _lpEntryId_ parameter to this entry identifier and call [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="10b18-135">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="10b18-135">MFCMAPI reference</span></span>

<span data-ttu-id="10b18-136">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="10b18-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="10b18-137">**����**</span><span class="sxs-lookup"><span data-stu-id="10b18-137">**File**</span></span>|<span data-ttu-id="10b18-138">**�������**</span><span class="sxs-lookup"><span data-stu-id="10b18-138">**Function**</span></span>|<span data-ttu-id="10b18-139">**�����������**</span><span class="sxs-lookup"><span data-stu-id="10b18-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="10b18-140">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="10b18-140">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="10b18-141">**CFolderDlg::OnSubmitMessage**</span><span class="sxs-lookup"><span data-stu-id="10b18-141">**CFolderDlg::OnSubmitMessage**</span></span> <br/> |<span data-ttu-id="10b18-142">Mfcmapi (en) использует метод **IMessage::SubmitMessage** для отправки выбранного сообщения.</span><span class="sxs-lookup"><span data-stu-id="10b18-142">MFCMAPI uses the **IMessage::SubmitMessage** method to submit the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="10b18-143">См. также</span><span class="sxs-lookup"><span data-stu-id="10b18-143">See also</span></span>



[<span data-ttu-id="10b18-144">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="10b18-144">IMsgStore::AbortSubmit</span></span>](imsgstore-abortsubmit.md)
  
[<span data-ttu-id="10b18-145">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="10b18-145">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="10b18-146">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="10b18-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

