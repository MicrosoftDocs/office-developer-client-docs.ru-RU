---
title: имаписуппортреадрецеипт
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
# <a name="imapisupportreadreceipt"></a><span data-ttu-id="dcebd-103">IMAPISupport::ReadReceipt</span><span class="sxs-lookup"><span data-stu-id="dcebd-103">IMAPISupport::ReadReceipt</span></span>

  
  
<span data-ttu-id="dcebd-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dcebd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dcebd-105">Создает отчет о прочтении или непрочтении для сообщения.</span><span class="sxs-lookup"><span data-stu-id="dcebd-105">Generates a read or nonread report for a message.</span></span>
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a><span data-ttu-id="dcebd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dcebd-106">Parameters</span></span>

 <span data-ttu-id="dcebd-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dcebd-107">_ulFlags_</span></span>
  
> <span data-ttu-id="dcebd-108">возврата Битовая маска флагов, определяющих способ создания отчета о прочтении или непрочтении.</span><span class="sxs-lookup"><span data-stu-id="dcebd-108">[in] A bitmask of flags that controls how the read or nonread report is generated.</span></span> <span data-ttu-id="dcebd-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="dcebd-109">The following flag can be set:</span></span>
    
<span data-ttu-id="dcebd-110">MAPI_NON_READ</span><span class="sxs-lookup"><span data-stu-id="dcebd-110">MAPI_NON_READ</span></span> 
  
> <span data-ttu-id="dcebd-111">Создается отчет о непрочтенном.</span><span class="sxs-lookup"><span data-stu-id="dcebd-111">A nonread report is generated.</span></span> <span data-ttu-id="dcebd-112">Если MAPI_NON_READ не задано, создается отчет о прочтении.</span><span class="sxs-lookup"><span data-stu-id="dcebd-112">If MAPI_NON_READ is not set, a read report is generated.</span></span>
    
 <span data-ttu-id="dcebd-113">_лпреадмессаже_</span><span class="sxs-lookup"><span data-stu-id="dcebd-113">_lpReadMessage_</span></span>
  
> <span data-ttu-id="dcebd-114">возврата Указатель на сообщение, о котором должен быть создан отчет.</span><span class="sxs-lookup"><span data-stu-id="dcebd-114">[in] A pointer to the message about which the report should be generated.</span></span>
    
 <span data-ttu-id="dcebd-115">_лппемптимессаже_</span><span class="sxs-lookup"><span data-stu-id="dcebd-115">_lppEmptyMessage_</span></span>
  
> <span data-ttu-id="dcebd-116">[вход, выход] Во входных данных _лппемптимессаже_ указывает на указатель на пустое сообщение.</span><span class="sxs-lookup"><span data-stu-id="dcebd-116">[in, out] On input,  _lppEmptyMessage_ points to a pointer to an empty message.</span></span> <span data-ttu-id="dcebd-117">В выходных данных _лппемптимессаже_ указывает на указатель на сообщение отчета.</span><span class="sxs-lookup"><span data-stu-id="dcebd-117">On output,  _lppEmptyMessage_ points to a pointer to the report message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dcebd-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dcebd-118">Return value</span></span>

<span data-ttu-id="dcebd-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="dcebd-119">S_OK</span></span> 
  
> <span data-ttu-id="dcebd-120">Отчет успешно создан.</span><span class="sxs-lookup"><span data-stu-id="dcebd-120">The report was successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dcebd-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="dcebd-121">Remarks</span></span>

<span data-ttu-id="dcebd-122">Метод **имаписуппорт:: ReadReceipt** реализован только для объектов поддержки поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="dcebd-122">The **IMAPISupport::ReadReceipt** method is implemented only for message store provider support objects.</span></span> <span data-ttu-id="dcebd-123">Поставщики хранилищ сообщений вызывают **ReadReceipt** , чтобы сообщить MAPI о создании отчета о прочтении или непрочтении для сообщения, на которое указывает параметр _лпреадмессаже_ .</span><span class="sxs-lookup"><span data-stu-id="dcebd-123">Message store providers call **ReadReceipt** to instruct MAPI to generate a read or nonread report for the message pointed to by the  _lpReadMessage_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dcebd-124">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="dcebd-124">Notes to callers</span></span>

<span data-ttu-id="dcebd-125">Вызовите **ReadReceipt** , когда задано свойство **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)), выполняется одно из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="dcebd-125">Call **ReadReceipt** when the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set and one of the following conditions is true:</span></span>
  
- <span data-ttu-id="dcebd-126">Сообщение прочитано.</span><span class="sxs-lookup"><span data-stu-id="dcebd-126">The message has been read.</span></span>
    
- <span data-ttu-id="dcebd-127">Сообщение было перемещено.</span><span class="sxs-lookup"><span data-stu-id="dcebd-127">The message has been moved.</span></span>
    
- <span data-ttu-id="dcebd-128">Сообщение скопировано.</span><span class="sxs-lookup"><span data-stu-id="dcebd-128">The message has been copied.</span></span>
    
- <span data-ttu-id="dcebd-129">Был вызван метод сообщения [iMessage:: сетреадфлаг](imessage-setreadflag.md) .</span><span class="sxs-lookup"><span data-stu-id="dcebd-129">The message's [IMessage::SetReadFlag](imessage-setreadflag.md) method has been called.</span></span> 
    
<span data-ttu-id="dcebd-130">Не вызывайте **ReadReceipt** при удалении сообщения.</span><span class="sxs-lookup"><span data-stu-id="dcebd-130">Do not call **ReadReceipt** when a message is deleted.</span></span> 
  
<span data-ttu-id="dcebd-131">Отчет о прочтении или непрочтении должен быть отправлен только один раз для сообщения.</span><span class="sxs-lookup"><span data-stu-id="dcebd-131">A read or nonread report should be sent only once for a message.</span></span> <span data-ttu-id="dcebd-132">Следите за состоянием чтения сообщения и не отправляете несколько отчетов для одного сообщения.</span><span class="sxs-lookup"><span data-stu-id="dcebd-132">Keep track of a message's read status and do not send multiple reports for a single message.</span></span>
  
<span data-ttu-id="dcebd-133">Если параметр _лппемптимессаже_ указывает на допустимое сообщение отчета, когда MAPI возвращает значение из **ReadReceipt**, вызовите метод [iMessage:: субмитмессаже](imessage-submitmessage.md) , чтобы отправить сообщение, а затем отпустите указатель, вызвав его метод **выпуска IUnknown: s:** .</span><span class="sxs-lookup"><span data-stu-id="dcebd-133">If the  _lppEmptyMessage_ parameter points to a valid report message when MAPI returns from **ReadReceipt**, call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send the message and then release the pointer by calling its **IUnknown:s:Release** method.</span></span> 
  
<span data-ttu-id="dcebd-134">Если **ReadReceipt** завершается с ошибкой, сообщение должно быть выпущено без отправки.</span><span class="sxs-lookup"><span data-stu-id="dcebd-134">If **ReadReceipt** fails, the message should be released without being submitted.</span></span> <span data-ttu-id="dcebd-135">Если вы сохраняете состояние чтения сообщения, вы можете попытаться создать отчет о прочтении или непрочтении позже.</span><span class="sxs-lookup"><span data-stu-id="dcebd-135">If you store the message's read status, you can attempt to generate the read or nonread report at a later time.</span></span> 
  
<span data-ttu-id="dcebd-136">Можно либо скрыть, либо отобразить отчеты о прочтении и непрочтении, созданные хранилищами в папках.</span><span class="sxs-lookup"><span data-stu-id="dcebd-136">You can either hide or display read and nonread reports generated by stores in your folders.</span></span> <span data-ttu-id="dcebd-137">Хранение отчетов о прочтении и непрочтенных в скрытых папках позволяет реализовать более тесную защиту.</span><span class="sxs-lookup"><span data-stu-id="dcebd-137">Storing read and nonread reports in hidden folders enables you to implement tighter security.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dcebd-138">См. также</span><span class="sxs-lookup"><span data-stu-id="dcebd-138">See also</span></span>



[<span data-ttu-id="dcebd-139">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="dcebd-139">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
  
[<span data-ttu-id="dcebd-140">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="dcebd-140">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="dcebd-141">Каноническое свойство PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="dcebd-141">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)
  
[<span data-ttu-id="dcebd-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="dcebd-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

