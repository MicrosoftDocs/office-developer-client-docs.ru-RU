---
title: Отслеживание бесед
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 0500dee8-a39d-45ce-87b1-c515e92e083d
description: 'Дата последнего изменения: 23 июля 2011 г.'
localization_priority: Priority
ms.openlocfilehash: 3a59a7a15b4647832634adc4757544876b8841b1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706224"
---
# <a name="tracking-conversations"></a><span data-ttu-id="cf009-103">Отслеживание бесед</span><span class="sxs-lookup"><span data-stu-id="cf009-103">Tracking Conversations</span></span>

  
  
<span data-ttu-id="cf009-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf009-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf009-p101">Отслеживание беседы — это сбор ответов на сообщение. Клиенты должны настроить два свойства, помогающие облегчающие отслеживание бесед:</span><span class="sxs-lookup"><span data-stu-id="cf009-p101">Conversation tracking is collecting responses to a message. Clients should set two properties that aid in tracking conversations:</span></span>
  
- <span data-ttu-id="cf009-107">**PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cf009-107">**PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md))</span></span>
    
    <span data-ttu-id="cf009-108">**PR_CONVERSATION_TOPIC** — нормализованная тема сообщения, тема без строк префикса</span><span class="sxs-lookup"><span data-stu-id="cf009-108">**PR_CONVERSATION_TOPIC** is the normalized subject of the message, the subject without the prefix strings.</span></span> <span data-ttu-id="cf009-109">Установите для этого свойства значение свойства **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) сообщения.</span><span class="sxs-lookup"><span data-stu-id="cf009-109">Set this property to the value of the message's **PR_NORMALIZED_SUBJECT** ( [PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span> 
    
- <span data-ttu-id="cf009-110">**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cf009-110">**PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md))</span></span>
    
    <span data-ttu-id="cf009-p103">**PR_CONVERSATION_INDEX** указывает расположение сообщения в определенной беседе. За установку свойства **PR_CONVERSATION_INDEX** для каждого исходящего сообщения отвечает клиент, вне зависимости, новое ли это сообщение, пересылаемое или ответ. Клиенты могут настроить это свойство вручную или вызвать служебную функцию [ScCreateConversationIndex](sccreateconversationindex.md), предусмотренную в MAPI.</span><span class="sxs-lookup"><span data-stu-id="cf009-p103">**PR_CONVERSATION_INDEX** indicates the position of the message within a particular conversation. It is a client's reponsibility to set **PR_CONVERSATION_INDEX** for each outgoing message, whether it is a new message, a forwarded message, or a reply. Clients can set this property manually or call [ScCreateConversationIndex](sccreateconversationindex.md), a utility function provided by MAPI.</span></span> 
    
 <span data-ttu-id="cf009-p104">**ScCreateConversationIndex** создает значение индекса беседы для любого исходящего сообщения. **ScCreateConversationIndex** реализует индекс как блок заголовка длиной 22 байта, за которым следует нуль или дополнительные дочерние блоки длиной 5 байт каждый.</span><span class="sxs-lookup"><span data-stu-id="cf009-p104">**ScCreateConversationIndex** generates the value of a conversation index for any outgoing message. **ScCreateConversationIndex** implements the index as a header block that is 22 bytes in length, followed by zero or more child blocks each 5 bytes in length.</span></span> 
  
<span data-ttu-id="cf009-116">Блок заголовка состоит из 22 байт, разделенных на три части:</span><span class="sxs-lookup"><span data-stu-id="cf009-116">The header block is composed of 22 bytes, divided into three parts:</span></span>
  
- <span data-ttu-id="cf009-p105">Один резервный байт. Его значение — 1.</span><span class="sxs-lookup"><span data-stu-id="cf009-p105">One reserved byte. Its value is 1.</span></span>
    
- <span data-ttu-id="cf009-119">Пять байт для текущего системного времени, преобразованного в структурный формат [FILETIME](filetime.md).</span><span class="sxs-lookup"><span data-stu-id="cf009-119">Five bytes for the current system time converted to the [FILETIME](filetime.md) structure format.</span></span> 
    
- <span data-ttu-id="cf009-120">Шестнадцать байт, содержащих глобальный уникальный идентификатор [GUID](guid.md).</span><span class="sxs-lookup"><span data-stu-id="cf009-120">Sixteen bytes holding a [GUID](guid.md), or globally unique identifier.</span></span>
    
<span data-ttu-id="cf009-121">Каждый дочерний блок состоит из 5 байт, разделенных указанным ниже образом:</span><span class="sxs-lookup"><span data-stu-id="cf009-121">Each child block is composed of 5 bytes, divided as follows:</span></span>
  
- <span data-ttu-id="cf009-p106">Один бит, содержащий код, который представляет разницу между текущим временем и временем, сохраненным в блоке заголовка. Этот бит равен 0, если разница составляет меньше 0,02 секунды или больше двух лет, и равен 1, если разница составляет меньше одной секунды или больше 56 лет.</span><span class="sxs-lookup"><span data-stu-id="cf009-p106">One bit containing a code representing the difference between the current time and the time stored in the header block. This bit will be 0 if the difference is less than .02 second and greater than two years and 1 if the difference is less than one second and greater than 56 years.</span></span>
    
- <span data-ttu-id="cf009-p107">Тридцать один бит, содержащий разницу между текущим временем и временем в блоке заголовка, выраженным в единицах **FILETIME**. Эта часть дочернего блока создается с помощью одного из двух методов в зависимости от значения первого бита. Если этот бит равен нулю, функция **ScCreateConversationIndex** удаляет старшие 15 бит и младшие 18 бит. Если этот бит равен единице, функция удаляет старшие 10 бит и младшие 23 бита.</span><span class="sxs-lookup"><span data-stu-id="cf009-p107">Thirty one bits containing the difference between the current time and the time in the header block expressed in **FILETIME** units.This part of the child block is produced using one of two strategies, depending on the value of the first bit. If this bit is zero, **ScCreateConversationIndex** discards the high 15 bits and the low 18 bits. If this bit is one, the function discards the high 10 bits and the low 23 bits.</span></span> 
    
- <span data-ttu-id="cf009-127">Четыре бита, содержащие случайное число, созданное с помощью вызова функции Win32 [GetTickCount](https://msdn.microsoft.com/library/ms724408%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="cf009-127">Four bits containing a random number generated by calling the Win32 function [GetTickCount](https://msdn.microsoft.com/library/ms724408%28VS.85%29.aspx).</span></span>
    
- <span data-ttu-id="cf009-128">Четыре бита, содержащие значение порядкового номера, взятого из части случайного числа.</span><span class="sxs-lookup"><span data-stu-id="cf009-128">Four bits containing a sequence count that is taken from part of the random number.</span></span>
    
<span data-ttu-id="cf009-129">Если вы решили установить индексы сообщений для беседы вручную, рекомендуется учитывать указанные ниже предложения.</span><span class="sxs-lookup"><span data-stu-id="cf009-129">If you choose to set the conversation indexes of messages manually, consider the following suggestions:</span></span>
  
1. <span data-ttu-id="cf009-130">Сохраняйте разницу в часовых поясах респондентов понятной. Используйте время UTC, а не местное время.</span><span class="sxs-lookup"><span data-stu-id="cf009-130">Keep differences in the respondents' time zones transparent; use UTC times rather than local time.</span></span>
    
2. <span data-ttu-id="cf009-131">Используйте одинаковые отступы для каждой группы сообщений.</span><span class="sxs-lookup"><span data-stu-id="cf009-131">Indent each conversation group by the same amount.</span></span>
    
3. <span data-ttu-id="cf009-132">Сортируйте ответы по одинаковой дате сообщения.</span><span class="sxs-lookup"><span data-stu-id="cf009-132">Sort responses to the same message date.</span></span>
    
4. <span data-ttu-id="cf009-133">Разделяйте относящиеся к одной теме цепочки бесед, начатые в разное время.</span><span class="sxs-lookup"><span data-stu-id="cf009-133">Separate threads started at different times that happen to share the same topic.</span></span> 
    
5. <span data-ttu-id="cf009-134">Для реализации сортировки по категориям, чтобы сообщения группировались по темам, сначала выполните сортировку по **PR_CONVERSATION_TOPIC**, а затем по **PR_CONVERSATION_INDEX**.</span><span class="sxs-lookup"><span data-stu-id="cf009-134">To implement a categorized sort so that messages are grouped by topic, sort by **PR_CONVERSATION_TOPIC** first and then by **PR_CONVERSATION_INDEX**.</span></span> <span data-ttu-id="cf009-135">Чтобы представить результаты сортировки, присвойте свойству **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) значение 0 для сообщений с длиной индекса беседы 22 байта.</span><span class="sxs-lookup"><span data-stu-id="cf009-135">To present the results of the sort, set the **PR_DEPTH** ( [PidTagDepth](pidtagdepth-canonical-property.md)) property to 0 for messages with a conversation index that is 22 bytes in length.</span></span> <span data-ttu-id="cf009-136">Затем для каждого увеличения длины на 5 байтов увеличивайте значение свойства **PR_DEPTH** на единицу.</span><span class="sxs-lookup"><span data-stu-id="cf009-136">Then, for every 5-byte increment in the length, increment the value of the **PR_DEPTH** property by one.</span></span> 
    
<span data-ttu-id="cf009-137">Группу свойств PR_ORIGINAL также можно использовать для отслеживания бесед.</span><span class="sxs-lookup"><span data-stu-id="cf009-137">The PR_ORIGINAL group of properties can also be used for conversation tracking.</span></span> <span data-ttu-id="cf009-138">Настройте эти свойства, чтобы связать ответные или пересылаемые сообщения с исходным сообщением.</span><span class="sxs-lookup"><span data-stu-id="cf009-138">Set these properties to link reply or forwarded messages to the original message.</span></span> <span data-ttu-id="cf009-139">Все свойства PR_ORIGINAL являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="cf009-139">All of the PR_ORIGINAL properties are optional.</span></span> <span data-ttu-id="cf009-140">Если явным образом не присвоено значение, например **PR_ORIGINAL_AUTHOR_ENTRYID** ([PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)), поставщик хранилища сообщений может использовать значение по умолчанию или значение свойства **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cf009-140">If you do not explicitly set, for example, **PR_ORIGINAL_AUTHOR_ENTRYID** ( [PidTagOriginalAuthorEntryId](pidtagoriginalauthorentryid-canonical-property.md)), the message store provider can use the default value, or the value of the **PR_SENDER_ENTRYID** ( [PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="cf009-141">Аналогичным образом, если не установлено значение **PR_ORIGINAL_AUTHOR_NAME** или **PR_ORIGINAL_SUBMIT_TIME** ([PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)), этим свойствам могут быть по умолчанию присвоены значения свойств **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) и **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) соответственно.</span><span class="sxs-lookup"><span data-stu-id="cf009-141">Likewise, if you do not set **PR_ORIGINAL_AUTHOR_NAME** or **PR_ORIGINAL_SUBMIT_TIME** ( [PidTagOriginalSubmitTime](pidtagoriginalsubmittime-canonical-property.md)), these properties can default to the values of the **PR_SENDER_NAME** ( [PidTagSenderName](pidtagsendername-canonical-property.md)) and **PR_CLIENT_SUBMIT_TIME** ( [PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) properties, respectively.</span></span> 
  

