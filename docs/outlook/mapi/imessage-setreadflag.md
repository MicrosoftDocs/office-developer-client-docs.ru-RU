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
ms.openlocfilehash: 874dba4aa18190792a52e29064155f5afa0ef44d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439872"
---
# <a name="imessagesetreadflag"></a><span data-ttu-id="b20f3-103">IMessage::SetReadFlag</span><span class="sxs-lookup"><span data-stu-id="b20f3-103">IMessage::SetReadFlag</span></span>

<span data-ttu-id="b20f3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b20f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b20f3-105">Задает или очищает MSGFLAG_READ флага в свойстве **PR_MESSAGE_FLAGS** ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)сообщения и управляет отправкой отчетов о прочтенных сообщениях.</span><span class="sxs-lookup"><span data-stu-id="b20f3-105">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of the message and manages the sending of read reports.</span></span>
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b20f3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b20f3-106">Parameters</span></span>

<span data-ttu-id="b20f3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b20f3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b20f3-108">[in] Битовая почта флагов, которая управляет установкой флага чтения сообщения, то есть флагом MSGFLAG_READ сообщения в его свойстве **PR_MESSAGE_FLAGS** и обработкой отчетов о прочтовке.</span><span class="sxs-lookup"><span data-stu-id="b20f3-108">[in] Bitmask of flags that controls the setting of a message's read flag that is, the message's MSGFLAG_READ flag in its **PR_MESSAGE_FLAGS** property and the processing of read reports.</span></span> <span data-ttu-id="b20f3-109">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="b20f3-109">The following flags can be set:</span></span> 
    
  - <span data-ttu-id="b20f3-110">CLEAR_READ_FLAG: флаг MSGFLAG_READ должен быть очищен в  PR_MESSAGE_FLAGS и не должен быть отправлен отчет о прочтях.</span><span class="sxs-lookup"><span data-stu-id="b20f3-110">CLEAR_READ_FLAG: The MSGFLAG_READ flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="b20f3-111">CLEAR_NRN_PENDING: флаг MSGFLAG_NRN_PENDING должен быть очищен в  PR_MESSAGE_FLAGS и не должен быть отправлен отчет о непрочитанных сообщениях.</span><span class="sxs-lookup"><span data-stu-id="b20f3-111">CLEAR_NRN_PENDING: The MSGFLAG_NRN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and a non-read report should not be sent.</span></span> 
      
  - <span data-ttu-id="b20f3-112">CLEAR_RN_PENDING: флаг MSGFLAG_RN_PENDING должен быть очищен в PR_MESSAGE_FLAGS  и не должен быть отправлен отчет о прочтях.</span><span class="sxs-lookup"><span data-stu-id="b20f3-112">CLEAR_RN_PENDING: The MSGFLAG_RN_PENDING flag should be cleared in **PR_MESSAGE_FLAGS** and no read report should be sent.</span></span> 
      
  - <span data-ttu-id="b20f3-113">GENERATE_RECEIPT_ONLY. Если отчет находится в состоянии ожидания, должен быть отправлен отчет о MSGFLAG_READ состояния.</span><span class="sxs-lookup"><span data-stu-id="b20f3-113">GENERATE_RECEIPT_ONLY: A read report should be sent if one is pending, but there should be no change in the state of the MSGFLAG_READ flag.</span></span>
      
  - <span data-ttu-id="b20f3-114">MAPI_DEFERRED_ERRORS: позволяет **SetReadFlag** успешно возвращаться, возможно, до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="b20f3-114">MAPI_DEFERRED_ERRORS: Allows **SetReadFlag** to return successfully, possibly before the operation has completed.</span></span> 
      
  - <span data-ttu-id="b20f3-115">SUPPRESS_RECEIPT: отчет об ожидающих чтениях должен быть отменен, если запросят отчет о прочтечении и этот вызов изменяет состояние сообщения с непрочитанного на прочитанные.</span><span class="sxs-lookup"><span data-stu-id="b20f3-115">SUPPRESS_RECEIPT: A pending read report should be canceled if a read report had been requested and this call changes the state of the message from unread to read.</span></span> <span data-ttu-id="b20f3-116">Если этот вызов не меняет состояние сообщения, поставщик store сообщений может игнорировать этот флаг.</span><span class="sxs-lookup"><span data-stu-id="b20f3-116">If this call does not change the state of the message, the message store provider can ignore this flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b20f3-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b20f3-117">Return value</span></span>

<span data-ttu-id="b20f3-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="b20f3-118">S_OK</span></span> 
  
> <span data-ttu-id="b20f3-119">Флаг чтения сообщения успешно установлен или очищен.</span><span class="sxs-lookup"><span data-stu-id="b20f3-119">The message's read flag has been successfully set or cleared.</span></span>
    
<span data-ttu-id="b20f3-120">MAPI_E_NO_SUPPRESS</span><span class="sxs-lookup"><span data-stu-id="b20f3-120">MAPI_E_NO_SUPPRESS</span></span> 
  
> <span data-ttu-id="b20f3-121">Поставщик store сообщений не поддерживает подавление отчетов о прочтениях.</span><span class="sxs-lookup"><span data-stu-id="b20f3-121">The message store provider does not support the suppression of read reports.</span></span>
    
<span data-ttu-id="b20f3-122">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b20f3-122">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="b20f3-123">В параметре  _ulFlags_ задано одно из следующих сочетаний флагов:</span><span class="sxs-lookup"><span data-stu-id="b20f3-123">One of the following combinations of flags is set in the  _ulFlags_ parameter:</span></span> 
    
   - <span data-ttu-id="b20f3-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span><span class="sxs-lookup"><span data-stu-id="b20f3-124">SUPPRESS_RECEIPT | CLEAR_READ_FLAG</span></span> 
    
   - <span data-ttu-id="b20f3-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="b20f3-125">SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
   - <span data-ttu-id="b20f3-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span><span class="sxs-lookup"><span data-stu-id="b20f3-126">CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b20f3-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="b20f3-127">Remarks</span></span>

<span data-ttu-id="b20f3-128">Метод **IMessage::SetReadFlag** задает или очищает флаг MSGFLAG_READ сообщения в свойстве **PR_MESSAGE_FLAGS** и вызывает [IMAPIProp::SaveChanges,](imapiprop-savechanges.md) чтобы сохранить сообщение.</span><span class="sxs-lookup"><span data-stu-id="b20f3-128">The **IMessage::SetReadFlag** method sets or clears the message's MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** property and calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md) to save the message.</span></span> <span data-ttu-id="b20f3-129">Установка флага MSGFLAG_READ помечания сообщения как прочитаного, что необязательно указывает на то, что указанный получатель действительно прочитал сообщение.</span><span class="sxs-lookup"><span data-stu-id="b20f3-129">Setting the MSGFLAG_READ flag marks a message as having been read, which does not necessarily indicate that the intended recipient has actually read the message.</span></span> 
  
<span data-ttu-id="b20f3-130">**SetReadFlags** также управляет отправкой отчетов чтения.</span><span class="sxs-lookup"><span data-stu-id="b20f3-130">**SetReadFlags** also manages the sending of read reports.</span></span> <span data-ttu-id="b20f3-131">Отчет о прочтовке отправляется только в том случае, если отправитель запросил его.</span><span class="sxs-lookup"><span data-stu-id="b20f3-131">A read report is sent only if the sender has requested one.</span></span> 
  
<span data-ttu-id="b20f3-132">Флаг чтения нельзя изменить для:</span><span class="sxs-lookup"><span data-stu-id="b20f3-132">The read flag cannot be altered for:</span></span>
  
- <span data-ttu-id="b20f3-133">Сообщения, которые не существуют.</span><span class="sxs-lookup"><span data-stu-id="b20f3-133">Messages that do not exist.</span></span>
    
- <span data-ttu-id="b20f3-134">Сообщения, которые были перемещены в другое место.</span><span class="sxs-lookup"><span data-stu-id="b20f3-134">Messages that have been moved elsewhere.</span></span>
    
- <span data-ttu-id="b20f3-135">Сообщения, которые открываются с разрешением на чтение и записи.</span><span class="sxs-lookup"><span data-stu-id="b20f3-135">Messages that are open with read/write permission.</span></span>
    
- <span data-ttu-id="b20f3-136">Отправленные в данный момент сообщения.</span><span class="sxs-lookup"><span data-stu-id="b20f3-136">Messages that are currently submitted.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="b20f3-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="b20f3-137">Notes to callers</span></span>

<span data-ttu-id="b20f3-138">Если ни один из флагов не задан в параметре  _ulFlags,_ применяются следующие правила:</span><span class="sxs-lookup"><span data-stu-id="b20f3-138">If none of the flags are set in the  _ulFlags_ parameter, the following rules apply:</span></span> 
  
- <span data-ttu-id="b20f3-139">Если MSGFLAG_READ уже установлен, ничего не делать.</span><span class="sxs-lookup"><span data-stu-id="b20f3-139">If MSGFLAG_READ is already set, do nothing.</span></span>
    
- <span data-ttu-id="b20f3-140">Если MSGFLAG_READ не установлен, задайте его и отправьте все ожидающих отчетов о прочтение, если установлено свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested).](pidtagreadreceiptrequested-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b20f3-140">If MSGFLAG_READ is not set, set it and send any pending read reports if the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set.</span></span>
    
<span data-ttu-id="b20f3-141">Если установлены SUPPRESS_RECEIPT и GENERATE_RECEIPT_ONLY, следует очистить бит PR_READ_RECEIPT_REQUESTED, если он установлен, и не отправить отчет о прочтях.</span><span class="sxs-lookup"><span data-stu-id="b20f3-141">If both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, the PR_READ_RECEIPT_REQUESTED bit, if set, should be cleared and a read report should not be sent.</span></span>
  
<span data-ttu-id="b20f3-142">Если установлен SUPPRESS_RECEIPT флага:</span><span class="sxs-lookup"><span data-stu-id="b20f3-142">When the SUPPRESS_RECEIPT flag is set:</span></span>
  
- <span data-ttu-id="b20f3-143">Если MSGFLAG_READ уже установлен, ничего не делать.</span><span class="sxs-lookup"><span data-stu-id="b20f3-143">If MSGFLAG_READ is already set, do nothing.</span></span> 
    
- <span data-ttu-id="b20f3-144">Если MSGFLAG_READ не установлен, установите его и отмените все ожидающих отчетов о прочте..</span><span class="sxs-lookup"><span data-stu-id="b20f3-144">If MSGFLAG_READ is not set, set it and cancel any pending read reports.</span></span>
    
<span data-ttu-id="b20f3-145">Когда флаг CLEAR_READ_FLAG установлен, MSGFLAG_READ флага в свойстве PR_MESSAGE_FLAGS сообщения  и не отправляйте отчеты о прочтенных сообщениях.</span><span class="sxs-lookup"><span data-stu-id="b20f3-145">When the CLEAR_READ_FLAG flag is set, clear the MSGFLAG_READ flag in each message's **PR_MESSAGE_FLAGS** property and do not send any read reports.</span></span> 
  
<span data-ttu-id="b20f3-146">Когда флаг GENERATE_RECEIPT_ONLY, отправьте все ожидающих отчетов о прочте..</span><span class="sxs-lookup"><span data-stu-id="b20f3-146">When the GENERATE_RECEIPT_ONLY flag is set, send any pending read reports.</span></span> <span data-ttu-id="b20f3-147">Не устанавливать и не очищать MSGFLAG_READ.</span><span class="sxs-lookup"><span data-stu-id="b20f3-147">Do not set or clear MSGFLAG_READ.</span></span>
  
<span data-ttu-id="b20f3-148">Если установлены SUPPRESS_RECEIPT и GENERATE_RECEIPT_ONLY, установите для свойства PR_READ_RECEIPT_REQUESTED false, если оно установлено, и не отправьте отчет о прочте.</span><span class="sxs-lookup"><span data-stu-id="b20f3-148">When both the SUPPRESS_RECEIPT and GENERATE_RECEIPT_ONLY flags are set, set the PR_READ_RECEIPT_REQUESTED property to FALSE if it is set and do not send a read report.</span></span>
  
<span data-ttu-id="b20f3-149">Вы можете оптимизировать поведение отчетов, подавляя генерацию отчетов о прочтение при определенных условиях.</span><span class="sxs-lookup"><span data-stu-id="b20f3-149">You can optimize report behavior by suppressing the generation of read reports under certain conditions.</span></span> <span data-ttu-id="b20f3-150">Однако если вы не поддерживаете подавление отчетов и клиент вызывает **SetReadFlag** с установленным флагом SUPPRESS_RECEIPT, MAPI_E_NO_SUPPRESS.</span><span class="sxs-lookup"><span data-stu-id="b20f3-150">However, if you do not support the suppression of reports and a client calls **SetReadFlag** with the SUPPRESS_RECEIPT flag set, return MAPI_E_NO_SUPPRESS.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b20f3-151">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b20f3-151">MFCMAPI reference</span></span>

<span data-ttu-id="b20f3-152">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="b20f3-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b20f3-153">**Файл**</span><span class="sxs-lookup"><span data-stu-id="b20f3-153">**File**</span></span>|<span data-ttu-id="b20f3-154">**Функция**</span><span class="sxs-lookup"><span data-stu-id="b20f3-154">**Function**</span></span>|<span data-ttu-id="b20f3-155">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="b20f3-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b20f3-156">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="b20f3-156">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="b20f3-157">CFolderDlg::OnSetReadFlag</span><span class="sxs-lookup"><span data-stu-id="b20f3-157">CFolderDlg::OnSetReadFlag</span></span>  <br/> |<span data-ttu-id="b20f3-158">MFCMAPI использует метод **IMessage::SetReadFlag,** чтобы установить флаги чтения для выбранных сообщений.</span><span class="sxs-lookup"><span data-stu-id="b20f3-158">MFCMAPI uses the **IMessage::SetReadFlag** method to set read flags on selected messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b20f3-159">См. также</span><span class="sxs-lookup"><span data-stu-id="b20f3-159">See also</span></span>

- [<span data-ttu-id="b20f3-160">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="b20f3-160">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)  
- [<span data-ttu-id="b20f3-161">IMAPIFolder::SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="b20f3-161">IMAPIFolder::SetReadFlags</span></span>](imapifolder-setreadflags.md)  
- [<span data-ttu-id="b20f3-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="b20f3-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)  
- [<span data-ttu-id="b20f3-163">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="b20f3-163">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md) 
- [<span data-ttu-id="b20f3-164">Каноническое свойство PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="b20f3-164">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md) 
- [<span data-ttu-id="b20f3-165">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b20f3-165">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)
- [<span data-ttu-id="b20f3-166">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="b20f3-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

