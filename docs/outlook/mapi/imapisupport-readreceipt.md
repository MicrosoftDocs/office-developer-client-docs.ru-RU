---
title: Имаписуппортреадрецеипт
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326308"
---
# <a name="imapisupportreadreceipt"></a><span data-ttu-id="cbafc-103">IMAPISupport::ReadReceipt</span><span class="sxs-lookup"><span data-stu-id="cbafc-103">IMAPISupport::ReadReceipt</span></span>

  
  
<span data-ttu-id="cbafc-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbafc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbafc-105">Создает отчет о прочтении или непрочтении для сообщения.</span><span class="sxs-lookup"><span data-stu-id="cbafc-105">Generates a read or nonread report for a message.</span></span>
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a><span data-ttu-id="cbafc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cbafc-106">Parameters</span></span>

 <span data-ttu-id="cbafc-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cbafc-107">_ulFlags_</span></span>
  
> <span data-ttu-id="cbafc-108">возврата Битовая маска флагов, определяющих способ создания отчета о прочтении или непрочтении.</span><span class="sxs-lookup"><span data-stu-id="cbafc-108">[in] A bitmask of flags that controls how the read or nonread report is generated.</span></span> <span data-ttu-id="cbafc-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="cbafc-109">The following flag can be set:</span></span>
    
<span data-ttu-id="cbafc-110">МАПИ_НОН_РЕАД</span><span class="sxs-lookup"><span data-stu-id="cbafc-110">MAPI_NON_READ</span></span> 
  
> <span data-ttu-id="cbafc-111">Создается отчет о непрочтенном.</span><span class="sxs-lookup"><span data-stu-id="cbafc-111">A nonread report is generated.</span></span> <span data-ttu-id="cbafc-112">Если МАПИ_НОН_РЕАД не задано, создается отчет о прочтении.</span><span class="sxs-lookup"><span data-stu-id="cbafc-112">If MAPI_NON_READ is not set, a read report is generated.</span></span>
    
 <span data-ttu-id="cbafc-113">_Лпреадмессаже_</span><span class="sxs-lookup"><span data-stu-id="cbafc-113">_lpReadMessage_</span></span>
  
> <span data-ttu-id="cbafc-114">возврата Указатель на сообщение, о котором должен быть создан отчет.</span><span class="sxs-lookup"><span data-stu-id="cbafc-114">[in] A pointer to the message about which the report should be generated.</span></span>
    
 <span data-ttu-id="cbafc-115">_Лппемптимессаже_</span><span class="sxs-lookup"><span data-stu-id="cbafc-115">_lppEmptyMessage_</span></span>
  
> <span data-ttu-id="cbafc-116">[вход, выход] Во входных данных _лппемптимессаже_ указывает на указатель на пустое сообщение.</span><span class="sxs-lookup"><span data-stu-id="cbafc-116">[in, out] On input,  _lppEmptyMessage_ points to a pointer to an empty message.</span></span> <span data-ttu-id="cbafc-117">В выходных данных _лппемптимессаже_ указывает на указатель на сообщение отчета.</span><span class="sxs-lookup"><span data-stu-id="cbafc-117">On output,  _lppEmptyMessage_ points to a pointer to the report message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cbafc-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cbafc-118">Return value</span></span>

<span data-ttu-id="cbafc-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="cbafc-119">S_OK</span></span> 
  
> <span data-ttu-id="cbafc-120">Отчет успешно создан.</span><span class="sxs-lookup"><span data-stu-id="cbafc-120">The report was successfully generated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cbafc-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="cbafc-121">Remarks</span></span>

<span data-ttu-id="cbafc-122">Метод **имаписуппорт:: ReadReceipt** реализован только для объектов поддержки поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="cbafc-122">The **IMAPISupport::ReadReceipt** method is implemented only for message store provider support objects.</span></span> <span data-ttu-id="cbafc-123">Поставщики хранилищ сообщений вызывают **ReadReceipt** , чтобы сообщить MAPI о создании отчета о прочтении или непрочтении для сообщения, на которое указывает параметр _лпреадмессаже_ .</span><span class="sxs-lookup"><span data-stu-id="cbafc-123">Message store providers call **ReadReceipt** to instruct MAPI to generate a read or nonread report for the message pointed to by the  _lpReadMessage_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cbafc-124">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="cbafc-124">Notes to callers</span></span>

<span data-ttu-id="cbafc-125">ВыЗовите **ReadReceipt** , если задано свойство **пр_реад_рецеипт_рекуестед** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)), и выполняется одно из следующих условий:</span><span class="sxs-lookup"><span data-stu-id="cbafc-125">Call **ReadReceipt** when the **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) property is set and one of the following conditions is true:</span></span>
  
- <span data-ttu-id="cbafc-126">Сообщение прочитано.</span><span class="sxs-lookup"><span data-stu-id="cbafc-126">The message has been read.</span></span>
    
- <span data-ttu-id="cbafc-127">Сообщение было перемещено.</span><span class="sxs-lookup"><span data-stu-id="cbafc-127">The message has been moved.</span></span>
    
- <span data-ttu-id="cbafc-128">Сообщение скопировано.</span><span class="sxs-lookup"><span data-stu-id="cbafc-128">The message has been copied.</span></span>
    
- <span data-ttu-id="cbafc-129">Был вызван метод сообщения [iMessage:: сетреадфлаг](imessage-setreadflag.md) .</span><span class="sxs-lookup"><span data-stu-id="cbafc-129">The message's [IMessage::SetReadFlag](imessage-setreadflag.md) method has been called.</span></span> 
    
<span data-ttu-id="cbafc-130">Не вызывайте **ReadReceipt** при удалении сообщения.</span><span class="sxs-lookup"><span data-stu-id="cbafc-130">Do not call **ReadReceipt** when a message is deleted.</span></span> 
  
<span data-ttu-id="cbafc-131">Отчет о прочтении или непрочтении должен быть отправлен только один раз для сообщения.</span><span class="sxs-lookup"><span data-stu-id="cbafc-131">A read or nonread report should be sent only once for a message.</span></span> <span data-ttu-id="cbafc-132">Следите за состоянием чтения сообщения и не отправляете несколько отчетов для одного сообщения.</span><span class="sxs-lookup"><span data-stu-id="cbafc-132">Keep track of a message's read status and do not send multiple reports for a single message.</span></span>
  
<span data-ttu-id="cbafc-133">Если параметр _лппемптимессаже_ указывает на допустимое сообщение отчета, когда MAPI возвращает значение из **ReadReceipt**, вызовите метод [iMessage:: субмитмессаже](imessage-submitmessage.md) , чтобы отправить сообщение, а затем отпустите указатель, вызвав его метод \*\*IUnknown: s: Release \*\*метод.</span><span class="sxs-lookup"><span data-stu-id="cbafc-133">If the  _lppEmptyMessage_ parameter points to a valid report message when MAPI returns from **ReadReceipt**, call the [IMessage::SubmitMessage](imessage-submitmessage.md) method to send the message and then release the pointer by calling its **IUnknown:s:Release** method.</span></span> 
  
<span data-ttu-id="cbafc-134">Если **ReadReceipt** завершается с ошибкой, сообщение должно быть выпущено без отправки.</span><span class="sxs-lookup"><span data-stu-id="cbafc-134">If **ReadReceipt** fails, the message should be released without being submitted.</span></span> <span data-ttu-id="cbafc-135">Если вы сохраняете состояние чтения сообщения, вы можете попытаться создать отчет о прочтении или непрочтении позже.</span><span class="sxs-lookup"><span data-stu-id="cbafc-135">If you store the message's read status, you can attempt to generate the read or nonread report at a later time.</span></span> 
  
<span data-ttu-id="cbafc-136">Можно либо скрыть, либо отобразить отчеты о прочтении и непрочтении, созданные хранилищами в папках.</span><span class="sxs-lookup"><span data-stu-id="cbafc-136">You can either hide or display read and nonread reports generated by stores in your folders.</span></span> <span data-ttu-id="cbafc-137">Хранение отчетов о прочтении и непрочтенных в скрытых папках позволяет реализовать более тесную защиту.</span><span class="sxs-lookup"><span data-stu-id="cbafc-137">Storing read and nonread reports in hidden folders enables you to implement tighter security.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cbafc-138">См. также</span><span class="sxs-lookup"><span data-stu-id="cbafc-138">See also</span></span>



[<span data-ttu-id="cbafc-139">IMAPIFolder::DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="cbafc-139">IMAPIFolder::DeleteMessages</span></span>](imapifolder-deletemessages.md)
  
[<span data-ttu-id="cbafc-140">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="cbafc-140">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="cbafc-141">Каноническое свойство PidTagReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="cbafc-141">PidTagReadReceiptRequested Canonical Property</span></span>](pidtagreadreceiptrequested-canonical-property.md)
  
[<span data-ttu-id="cbafc-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="cbafc-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

