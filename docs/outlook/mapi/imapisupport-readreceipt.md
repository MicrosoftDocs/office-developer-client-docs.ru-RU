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
ms.openlocfilehash: 5e56fd8c053ff32bdeb7b243701c0330b378cdc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809177"
---
# <a name="imapisupportreadreceipt"></a><span data-ttu-id="9ee3b-103">IMAPISupport::ReadReceipt</span><span class="sxs-lookup"><span data-stu-id="9ee3b-103">IMAPISupport::ReadReceipt</span></span>

  
  
<span data-ttu-id="9ee3b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9ee3b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9ee3b-105">Создает доступ на чтение или nonread отчет для сообщения.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-105">Generates a read or nonread report for a message.</span></span>
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a><span data-ttu-id="9ee3b-106">���������</span><span class="sxs-lookup"><span data-stu-id="9ee3b-106">Parameters</span></span>

 <span data-ttu-id="9ee3b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9ee3b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9ee3b-108">[in] Битовая маска флаги, который управляет созданием доступ на чтение или nonread отчета.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-108">[in] A bitmask of flags that controls how the read or nonread report is generated.</span></span> <span data-ttu-id="9ee3b-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="9ee3b-109">The following flag can be set:</span></span>
    
<span data-ttu-id="9ee3b-110">MAPI_NON_READ</span><span class="sxs-lookup"><span data-stu-id="9ee3b-110">MAPI_NON_READ</span></span> 
  
> <span data-ttu-id="9ee3b-111">Создается nonread отчет.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-111">A nonread report is generated.</span></span> <span data-ttu-id="9ee3b-112">Если MAPI_NON_READ не установлен, создается чтения отчет.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-112">If MAPI_NON_READ is not set, a read report is generated.</span></span>
    
 <span data-ttu-id="9ee3b-113">_lpReadMessage_</span><span class="sxs-lookup"><span data-stu-id="9ee3b-113">_lpReadMessage_</span></span>
  
> <span data-ttu-id="9ee3b-114">[in] Указатель на сообщение о том, какие будет создан отчет.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-114">[in] A pointer to the message about which the report should be generated.</span></span>
    
 <span data-ttu-id="9ee3b-115">_lppEmptyMessage_</span><span class="sxs-lookup"><span data-stu-id="9ee3b-115">_lppEmptyMessage_</span></span>
  
> <span data-ttu-id="9ee3b-116">[in, out] На входе _lppEmptyMessage_ указывает указатель на пустое сообщение.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-116">[in, out] On input,  _lppEmptyMessage_ points to a pointer to an empty message.</span></span> <span data-ttu-id="9ee3b-117">На выходе _lppEmptyMessage_ указывает указатель на сообщение отчета.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-117">On output,  _lppEmptyMessage_ points to a pointer to the report message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9ee3b-118">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="9ee3b-118">Return value</span></span>

<span data-ttu-id="9ee3b-119">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="9ee3b-119">S_OK</span></span> 
  
> <span data-ttu-id="9ee3b-120">Отчет создан успешно.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-120">The report was successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9ee3b-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="9ee3b-121">Remarks</span></span>

<span data-ttu-id="9ee3b-122">Метод **IMAPISupport::ReadReceipt** применяется только для объектов поддержки поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-122">The **IMAPISupport::ReadReceipt** method is implemented only for message store provider support objects.</span></span> <span data-ttu-id="9ee3b-123">Поставщики хранилища сообщений вызов **ReadReceipt** для указания MAPI для создания доступ на чтение или nonread отчетов для сообщений, на который указывает параметр _lpReadMessage_ .</span><span class="sxs-lookup"><span data-stu-id="9ee3b-123">Message store providers call **ReadReceipt** to instruct MAPI to generate a read or nonread report for the message pointed to by the  _lpReadMessage_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9ee3b-124">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="9ee3b-124">Notes to callers</span></span>

<span data-ttu-id="9ee3b-125">Вызовите **ReadReceipt** , когда свойству **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) и выполняется одно из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="9ee3b-125">Call **ReadReceipt** when the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set and one of the following conditions is true:</span></span>
  
- <span data-ttu-id="9ee3b-126">О сообщениях.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-126">The message has been read.</span></span>
    
- <span data-ttu-id="9ee3b-127">Сообщение перемещено.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-127">The message has been moved.</span></span>
    
- <span data-ttu-id="9ee3b-128">Сообщение скопирован.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-128">The message has been copied.</span></span>
    
- <span data-ttu-id="9ee3b-129">Был вызван метод [IMessage::SetReadFlag](imessage-setreadflag.md) сообщений.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-129">The message's [IMessage::SetReadFlag](imessage-setreadflag.md) method has been called.</span></span> 
    
<span data-ttu-id="9ee3b-130">Не вызывайте **ReadReceipt** , когда сообщение удаляется.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-130">Do not call **ReadReceipt** when a message is deleted.</span></span> 
  
<span data-ttu-id="9ee3b-131">Доступ на чтение или nonread отчет следует отправить только один раз для сообщения.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-131">A read or nonread report should be sent only once for a message.</span></span> <span data-ttu-id="9ee3b-132">Отслеживать состояние чтения сообщения и не отправляет несколько отчетов для одного сообщения.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-132">Keep track of a message's read status and do not send multiple reports for a single message.</span></span>
  
<span data-ttu-id="9ee3b-133">Если параметр _lppEmptyMessage_ указывает действительный отчет при возврате MAPI из **ReadReceipt**, вызовите метод [IMessage::SubmitMessage](imessage-submitmessage.md) , чтобы отправить сообщение и затем выпуска указателя мыши, вызвав его **IUnknown:s:Release **метод.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-133">If the  _lppEmptyMessage_ parameter points to a valid report message when MAPI returns from **ReadReceipt**, call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send the message and then release the pointer by calling its **IUnknown:s:Release** method.</span></span> 
  
<span data-ttu-id="9ee3b-134">В случае сбоя **ReadReceipt** необходимо освободить сообщение без отправки.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-134">If **ReadReceipt** fails, the message should be released without being submitted.</span></span> <span data-ttu-id="9ee3b-135">Если сохранять состояние чтения сообщения можно попытка создать доступ на чтение или nonread отчета в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-135">If you store the message's read status, you can attempt to generate the read or nonread report at a later time.</span></span> 
  
<span data-ttu-id="9ee3b-136">Можно скрыть или отобразить чтения и nonread отчеты, созданные с хранилищ в папках.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-136">You can either hide or display read and nonread reports generated by stores in your folders.</span></span> <span data-ttu-id="9ee3b-137">Хранение отчетов чтения и nonread в скрытых папок позволяет реализовывать повышения безопасности.</span><span class="sxs-lookup"><span data-stu-id="9ee3b-137">Storing read and nonread reports in hidden folders enables you to implement tighter security.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9ee3b-138">См. также</span><span class="sxs-lookup"><span data-stu-id="9ee3b-138">See also</span></span>



[<span data-ttu-id="9ee3b-139">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="9ee3b-139">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
  
[<span data-ttu-id="9ee3b-140">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="9ee3b-140">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="9ee3b-141">Каноническое свойство PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="9ee3b-141">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)
  
[<span data-ttu-id="9ee3b-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9ee3b-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

