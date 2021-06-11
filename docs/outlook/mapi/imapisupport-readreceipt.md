---
title: IMAPISupportReadReceipt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ReadReceipt
api_type:
- COM
ms.assetid: ef31b61a-93b6-4ae8-bc71-f5ef5caf43f4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1915004847fdfd27c97656223866aaab9d3e59c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425325"
---
# <a name="imapisupportreadreceipt"></a><span data-ttu-id="fe25d-103">IMAPISupport::ReadReceipt</span><span class="sxs-lookup"><span data-stu-id="fe25d-103">IMAPISupport::ReadReceipt</span></span>

  
  
<span data-ttu-id="fe25d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe25d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe25d-105">Создает отчет о прочтях или непрочитанных сообщениях.</span><span class="sxs-lookup"><span data-stu-id="fe25d-105">Generates a read or nonread report for a message.</span></span>
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a><span data-ttu-id="fe25d-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="fe25d-106">Parameters</span></span>

 <span data-ttu-id="fe25d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fe25d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="fe25d-108">[in] Битмаска флагов, которая управляет тем, как создается отчет о считывке или непрочитанке.</span><span class="sxs-lookup"><span data-stu-id="fe25d-108">[in] A bitmask of flags that controls how the read or nonread report is generated.</span></span> <span data-ttu-id="fe25d-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="fe25d-109">The following flag can be set:</span></span>
    
<span data-ttu-id="fe25d-110">MAPI_NON_READ</span><span class="sxs-lookup"><span data-stu-id="fe25d-110">MAPI_NON_READ</span></span> 
  
> <span data-ttu-id="fe25d-111">Создается непрочитаемый отчет.</span><span class="sxs-lookup"><span data-stu-id="fe25d-111">A nonread report is generated.</span></span> <span data-ttu-id="fe25d-112">Если MAPI_NON_READ не установлено, создается отчет о считыве.</span><span class="sxs-lookup"><span data-stu-id="fe25d-112">If MAPI_NON_READ is not set, a read report is generated.</span></span>
    
 <span data-ttu-id="fe25d-113">_lpReadMessage_</span><span class="sxs-lookup"><span data-stu-id="fe25d-113">_lpReadMessage_</span></span>
  
> <span data-ttu-id="fe25d-114">[in] Указатель на сообщение, о котором должен быть создан отчет.</span><span class="sxs-lookup"><span data-stu-id="fe25d-114">[in] A pointer to the message about which the report should be generated.</span></span>
    
 <span data-ttu-id="fe25d-115">_lppEmptyMessage_</span><span class="sxs-lookup"><span data-stu-id="fe25d-115">_lppEmptyMessage_</span></span>
  
> <span data-ttu-id="fe25d-116">[in, out] На входе  _lppEmptyMessage_ указывает на указатель на пустое сообщение.</span><span class="sxs-lookup"><span data-stu-id="fe25d-116">[in, out] On input,  _lppEmptyMessage_ points to a pointer to an empty message.</span></span> <span data-ttu-id="fe25d-117">На выходе  _lppEmptyMessage_ указывает указатель на сообщение отчета.</span><span class="sxs-lookup"><span data-stu-id="fe25d-117">On output,  _lppEmptyMessage_ points to a pointer to the report message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fe25d-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe25d-118">Return value</span></span>

<span data-ttu-id="fe25d-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="fe25d-119">S_OK</span></span> 
  
> <span data-ttu-id="fe25d-120">Отчет был успешно создан.</span><span class="sxs-lookup"><span data-stu-id="fe25d-120">The report was successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fe25d-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="fe25d-121">Remarks</span></span>

<span data-ttu-id="fe25d-122">Метод **IMAPISupport::ReadReceipt** реализуется только для объектов поддержки поставщиков сообщений.</span><span class="sxs-lookup"><span data-stu-id="fe25d-122">The **IMAPISupport::ReadReceipt** method is implemented only for message store provider support objects.</span></span> <span data-ttu-id="fe25d-123">Поставщики магазинов сообщений вызывают **ReadReceipt,** чтобы поручить MAPI создать отчет о считывке или непрочитанности для сообщения, на которое указывает _параметр lpReadMessage._</span><span class="sxs-lookup"><span data-stu-id="fe25d-123">Message store providers call **ReadReceipt** to instruct MAPI to generate a read or nonread report for the message pointed to by the  _lpReadMessage_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="fe25d-124">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="fe25d-124">Notes to callers</span></span>

<span data-ttu-id="fe25d-125">Вызов **ReadReceipt** **при PR_READ_RECEIPT_REQUESTED** свойства [(PidTagReadReceiptRequested)](pidtagreadreceiptrequested-canonical-property.md)и верно одно из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="fe25d-125">Call **ReadReceipt** when the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set and one of the following conditions is true:</span></span>
  
- <span data-ttu-id="fe25d-126">Сообщение было прочитано.</span><span class="sxs-lookup"><span data-stu-id="fe25d-126">The message has been read.</span></span>
    
- <span data-ttu-id="fe25d-127">Сообщение было перемещено.</span><span class="sxs-lookup"><span data-stu-id="fe25d-127">The message has been moved.</span></span>
    
- <span data-ttu-id="fe25d-128">Сообщение было скопировано.</span><span class="sxs-lookup"><span data-stu-id="fe25d-128">The message has been copied.</span></span>
    
- <span data-ttu-id="fe25d-129">Был вызван метод [IMessage::SetReadFlag.](imessage-setreadflag.md)</span><span class="sxs-lookup"><span data-stu-id="fe25d-129">The message's [IMessage::SetReadFlag](imessage-setreadflag.md) method has been called.</span></span> 
    
<span data-ttu-id="fe25d-130">Не **вызывайте ReadReceipt** при удалении сообщения.</span><span class="sxs-lookup"><span data-stu-id="fe25d-130">Do not call **ReadReceipt** when a message is deleted.</span></span> 
  
<span data-ttu-id="fe25d-131">Отчет о считываемом или непрочитаемом тексте должен отправляться только один раз для сообщения.</span><span class="sxs-lookup"><span data-stu-id="fe25d-131">A read or nonread report should be sent only once for a message.</span></span> <span data-ttu-id="fe25d-132">Отслеживайте состояние чтения сообщения и не отправляйте несколько отчетов для одного сообщения.</span><span class="sxs-lookup"><span data-stu-id="fe25d-132">Keep track of a message's read status and do not send multiple reports for a single message.</span></span>
  
<span data-ttu-id="fe25d-133">Если параметр _lppEmptyMessage_ указывает на действительное сообщение отчета при возвращении MAPI из **ReadReceipt,** позвоните в [метод IMessage::SubmitMessage,](imessage-submitmessage.md) чтобы отправить сообщение, а затем отпустите указатель, назвав метод **IUnknown:s:Release.**</span><span class="sxs-lookup"><span data-stu-id="fe25d-133">If the  _lppEmptyMessage_ parameter points to a valid report message when MAPI returns from **ReadReceipt**, call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send the message and then release the pointer by calling its **IUnknown:s:Release** method.</span></span> 
  
<span data-ttu-id="fe25d-134">Если **readReceipt** не удается, сообщение должно быть выпущено без отправки.</span><span class="sxs-lookup"><span data-stu-id="fe25d-134">If **ReadReceipt** fails, the message should be released without being submitted.</span></span> <span data-ttu-id="fe25d-135">Если вы сохраняете состояние чтения сообщения, можно попытаться создать отчет о считывке или непрочитанном тексте в более позднее время.</span><span class="sxs-lookup"><span data-stu-id="fe25d-135">If you store the message's read status, you can attempt to generate the read or nonread report at a later time.</span></span> 
  
<span data-ttu-id="fe25d-136">Можно скрыть или отобразить отчеты о считываемых и непрочитаемых данных, созданные в магазинах в папках.</span><span class="sxs-lookup"><span data-stu-id="fe25d-136">You can either hide or display read and nonread reports generated by stores in your folders.</span></span> <span data-ttu-id="fe25d-137">Хранение отчетов о прочтение и непрочитание в скрытых папках позволяет реализовать более жесткую безопасность.</span><span class="sxs-lookup"><span data-stu-id="fe25d-137">Storing read and nonread reports in hidden folders enables you to implement tighter security.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fe25d-138">См. также</span><span class="sxs-lookup"><span data-stu-id="fe25d-138">See also</span></span>



[<span data-ttu-id="fe25d-139">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="fe25d-139">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
  
[<span data-ttu-id="fe25d-140">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="fe25d-140">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="fe25d-141">Каноническое свойство PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="fe25d-141">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)
  
[<span data-ttu-id="fe25d-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="fe25d-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

