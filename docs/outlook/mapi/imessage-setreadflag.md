---
title: IMessageSetReadFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SetReadFlag
api_type:
- COM
ms.assetid: 2d02ebf6-bb8b-42bb-9bd0-870dbae9aeb4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 40815f1df597a8fb1fd8adef3dcc09323e946d30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592964"
---
# <a name="imessagesetreadflag"></a><span data-ttu-id="2b2f2-103">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="2b2f2-103">IMessage::SetReadFlag</span></span>

<span data-ttu-id="2b2f2-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b2f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b2f2-105">Устанавливает или сбрасывает MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) сообщения и управляет Отправка чтения отчеты.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message and manages the sending of read reports.</span></span>
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="2b2f2-106">���������</span><span class="sxs-lookup"><span data-stu-id="2b2f2-106">Parameters</span></span>

<span data-ttu-id="2b2f2-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2b2f2-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2b2f2-108">[in] Битовую маску флагов, который управляет параметром чтение сообщения флаг, то есть отметку MSGFLAG_READ в своем свойстве **PR_MESSAGE_FLAGS** и функции обработки для просмотра отчетов.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-108">[in] Bitmask of flags that controls the setting of a message's read flag that is, the message's MSGFLAG_READ flag in its **PR_MESSAGE_FLAGS** property and the processing of read reports.</span></span> <span data-ttu-id="2b2f2-109">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="2b2f2-109">The following flags can be set:</span></span> 
    
  - <span data-ttu-id="2b2f2-110">CLEAR_READ_FLAG: Флаг MSGFLAG_READ должен быть снят в **PR_MESSAGE_FLAGS** и чтения отчет не будут отправляться.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-110">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="2b2f2-111">CLEAR_NRN_PENDING: Флаг MSGFLAG_NRN_PENDING должен быть снят в **PR_MESSAGE_FLAGS** и не будут отправляться непрочтении отчета.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-111">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a non-read report should not be sent.</span></span> 
      
  - <span data-ttu-id="2b2f2-112">CLEAR_RN_PENDING: Флаг MSGFLAG_RN_PENDING должен быть снят в **PR_MESSAGE_FLAGS** и чтения отчет не будут отправляться.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-112">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="2b2f2-113">GENERATE_RECEIPT_ONLY: Чтения отчет следует отправить один ожидающий, когда должно быть никаких изменений в состояние флага MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-113">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
      
  - <span data-ttu-id="2b2f2-114">MAPI_DEFERRED_ERRORS: Разрешает **SetReadFlag** для возврата успешно, возможно до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-114">MAPI_DEFERRED_ERRORS: Allows **SetReadFlag** to return successfully, possibly before the operation has completed.</span></span> 
      
  - <span data-ttu-id="2b2f2-115">SUPPRESS_RECEIPT: Ожидающие чтения отчета должна быть отменена Если запрошен чтения отчета, и этот вызов изменяет состояние сообщения из непрочитанные сообщения для чтения.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-115">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="2b2f2-116">Если этот вызов не изменяет состояние сообщения, поставщик хранения сообщений можно игнорировать этот флаг.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-116">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2b2f2-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="2b2f2-117">Return value</span></span>

<span data-ttu-id="2b2f2-118">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="2b2f2-118">S_OK</span></span> 
  
> <span data-ttu-id="2b2f2-119">Чтение отметку успешно установить или снять.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-119">The message's read flag has been successfully set or cleared.</span></span>
    
<span data-ttu-id="2b2f2-120">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="2b2f2-120">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="2b2f2-121">Поставщик хранения сообщения не поддерживает подавления чтения отчеты.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-121">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="2b2f2-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2b2f2-122">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="2b2f2-123">Один из следующих комбинаций флаги задано с помощью параметра _ulFlags_ :</span><span class="sxs-lookup"><span data-stu-id="2b2f2-123">One of the following combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="2b2f2-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="2b2f2-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="2b2f2-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="2b2f2-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="2b2f2-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="2b2f2-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2b2f2-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="2b2f2-127">Remarks</span></span>

<span data-ttu-id="2b2f2-128">Метод **IMessage::SetReadFlag** устанавливает или сбрасывает MSGFLAG_READ сообщения в свойство **PR_MESSAGE_FLAGS** и вызовы [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сохранить сообщение.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-128">The **IMessage::SetReadFlag** method sets or clears the message's MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property and calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message.</span></span> <span data-ttu-id="2b2f2-129">Установка флага MSGFLAG_READ помечает сообщения как читать, которое не обязательно означает, что получателю фактически имеет чтение сообщения.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-129">Setting the MSGFLAG_READ flag marks a message as having been read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="2b2f2-130">Кроме того, **SetReadFlags** управляет Отправка просмотра отчетов.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-130">**SetReadFlags** also manages the sending of read reports.</span></span> <span data-ttu-id="2b2f2-131">Чтение отчета отправляется только в том случае, если отправитель запрашивает один.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-131">A read report is sent only if the sender has requested one.</span></span> 
  
<span data-ttu-id="2b2f2-132">Чтение флаг не могут быть изменены для:</span><span class="sxs-lookup"><span data-stu-id="2b2f2-132">The read flag cannot be altered for:</span></span>
  
- <span data-ttu-id="2b2f2-133">Сообщения, не существует.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-133">Messages that do not exist.</span></span>
    
- <span data-ttu-id="2b2f2-134">Сообщения, которые были перемещены в другом месте.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-134">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="2b2f2-135">Сообщения, открытые с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-135">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="2b2f2-136">Сообщения, которые передаются в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-136">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="2b2f2-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="2b2f2-137">Notes to callers</span></span>

<span data-ttu-id="2b2f2-138">Если ни один из флагов в параметре _ulFlags_ , применяются следующие правила:</span><span class="sxs-lookup"><span data-stu-id="2b2f2-138">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="2b2f2-139">Если MSGFLAG_READ уже задано, ничего не предпринимать.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-139">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="2b2f2-140">Если MSGFLAG_READ не установлен, установите его и отправить все ожидающие просмотра отчетов, если свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) имеет значение.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-140">If MSGFLAG_READ is not set, set it and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="2b2f2-141">Если SUPPRESS_RECEIPT и GENERATE_RECEIPT_ONLY флаги установлены, бит PR_READ_RECEIPT_REQUESTED, если задано, следует выполнить очистку и просмотра отчетов не будут отправляться.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-141">If both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, the PR_READ_RECEIPT_REQUESTED bit, if set, should be cleared and a read report should not be sent.</span></span>
  
<span data-ttu-id="2b2f2-142">Если задано флаг SUPPRESS_RECEIPT:</span><span class="sxs-lookup"><span data-stu-id="2b2f2-142">When the SUPPRESS_RECEIPT flag is set:</span></span>
  
- <span data-ttu-id="2b2f2-143">Если MSGFLAG_READ уже задано, ничего не предпринимать.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-143">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="2b2f2-144">Если MSGFLAG_READ не установлен, установите его и отменить ожидающие просмотра отчетов.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-144">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="2b2f2-145">Если флаг CLEAR_READ_FLAG, снимите флаг MSGFLAG_READ в свойстве **PR_MESSAGE_FLAGS** каждого сообщения и не отправлять чтения отчеты.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-145">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="2b2f2-146">Если для флага GENERATE_RECEIPT_ONLY, отправьте все ожидающие чтения отчеты.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-146">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="2b2f2-147">Выполните MSGFLAG_READ не установлен или clear.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-147">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="2b2f2-148">Когда SUPPRESS_RECEIPT и GENERATE_RECEIPT_ONLY флаги, присвойте свойству PR_READ_RECEIPT_REQUESTED значение FALSE, если оно установлено и не отправлять просмотра отчета.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-148">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set the PR_READ_RECEIPT_REQUESTED property to FALSE if it is set and do not send a read report.</span></span>
  
<span data-ttu-id="2b2f2-149">Можно оптимизировать поведение отчет с подавлением Создание чтения отчетов в определенных условиях.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-149">You can optimize report behavior by suppressing the generation of read reports under certain conditions.</span></span> <span data-ttu-id="2b2f2-150">Тем не менее если не поддерживают подавления отчеты и клиент вызывает **SetReadFlag** с установленным флагом SUPPRESS_RECEIPT, возвратите MAPI_E_NO_SUPPRESS.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-150">However, if you do not support the suppression of reports and a client calls **SetReadFlag** with the SUPPRESS_RECEIPT flag set, return MAPI_E_NO_SUPPRESS.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2b2f2-151">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="2b2f2-151">MFCMAPI reference</span></span>

<span data-ttu-id="2b2f2-152">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2b2f2-153">**����**</span><span class="sxs-lookup"><span data-stu-id="2b2f2-153">**File**</span></span>|<span data-ttu-id="2b2f2-154">**�������**</span><span class="sxs-lookup"><span data-stu-id="2b2f2-154">**Function**</span></span>|<span data-ttu-id="2b2f2-155">**�����������**</span><span class="sxs-lookup"><span data-stu-id="2b2f2-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2b2f2-156">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="2b2f2-156">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="2b2f2-157">CFolderDlg::OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="2b2f2-157">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="2b2f2-158">Mfcmapi (en) используется метод **IMessage::SetReadFlag** для задания чтения флаги для выбранного сообщения.</span><span class="sxs-lookup"><span data-stu-id="2b2f2-158">MFCMAPI uses the **IMessage::SetReadFlag** method to set read flags on selected messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2b2f2-159">См. также</span><span class="sxs-lookup"><span data-stu-id="2b2f2-159">See also</span></span>

- [<span data-ttu-id="2b2f2-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="2b2f2-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)  
- [<span data-ttu-id="2b2f2-161">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="2b2f2-161">IMAPIFolder::SetReadFlags</span></span>](imapifolder-setreadflags.md)  
- [<span data-ttu-id="2b2f2-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="2b2f2-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)  
- [<span data-ttu-id="2b2f2-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="2b2f2-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md) 
- [<span data-ttu-id="2b2f2-164">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="2b2f2-164">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md) 
- [<span data-ttu-id="2b2f2-165">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2b2f2-165">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
- [<span data-ttu-id="2b2f2-166">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="2b2f2-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

