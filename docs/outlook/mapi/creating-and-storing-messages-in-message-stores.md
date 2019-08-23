---
title: Создание и сохранение сообщений в хранилищах
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7c923a330c542dff8b1bbc476461ccd21680a5b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332902"
---
# <a name="creating-and-storing-messages-in-message-stores"></a><span data-ttu-id="0068f-103">Создание и сохранение сообщений в хранилищах</span><span class="sxs-lookup"><span data-stu-id="0068f-103">Creating and Storing Messages in Message Stores</span></span>

  
  
<span data-ttu-id="0068f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0068f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0068f-p101">То, как ваш поставщик услуг хранилища сообщения создает и сохраняет сообщения с помощью базового механизма хранилища, зависит от самого базового механизма хранилища. Как правило, вам нужно только написать код для сохранения свойств сообщения и их значений.</span><span class="sxs-lookup"><span data-stu-id="0068f-p101">How your message store provider creates and stores messages in the underlying storage mechanism depends heavily on the underlying storage mechanism itself. In general, you need only to write code to preserve the properties of a message and their values.</span></span>
  
<span data-ttu-id="0068f-p102">Когда поставщик хранилища сообщения создает сообщение, поставщику необходимо создать сообщение с обязательными свойствами сообщений. Список таких свойств см. в документации интерфейса[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). После этого клиентские приложения добавляют любые дополнительные свойства с помощью метода [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="0068f-p102">When the message store provider creates a new message, the provider needs to create the message with the required properties for messages. A list of these properties can be found in the documentation for the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface. After that, client applications add any additional properties with [IMAPIProp](imapipropiunknown.md) methods.</span></span> 
  
<span data-ttu-id="0068f-110">Когда сообщение сохраняете поставщика сохраняет сообщение, чтобы базовые механизм хранилища, поставщик нужно вывести следующий свойства сообщений и сохранить их базовые механизм хранилище так, что им может быть полностью восстановлен при последующем открытии сообщения.</span><span class="sxs-lookup"><span data-stu-id="0068f-110">When the message store provider saves a message to the underlying storage mechanism, the provider needs to iterate over the message's properties, and save them to the underlying storage mechanism such that they can be fully recovered if the message is later opened.</span></span>
  
<span data-ttu-id="0068f-p103">MAPI требует, чтобы свойства интерфейсов [IMessage](imessageimapiprop.md) передавались, что означает, что вносимые изменения не становятся постоянными, пока метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) вызывается для объекта сообщения. Поставщик услуг хранилища сообщения несет ответственность за реализацию данного поведение. Как правило, выполнить это несложно; это просто подразумевает удержание свойств в памяти, пока в них вносятся изменения, и внесение их в базовый механизм хранилища при вызове**SaveChanges**.</span><span class="sxs-lookup"><span data-stu-id="0068f-p103">MAPI requires that the properties on [IMessage](imessageimapiprop.md) interfaces are transacted, meaning that changes made to them do not become permanent until the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called on the message object. The message store provider is responsible for implementing this behavior. Usually this is not difficult; it simply means holding properties in memory while they are being modified and committing them to the underlying storage mechanism when **SaveChanges** is called.</span></span> 
  
<span data-ttu-id="0068f-114">Некоторые свойства для объектов обладают специальной семантикой для клиентских приложений в отношении метода **SaveChanges**, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="0068f-114">Some properties on message objects have special semantics for client applications with respect to the **SaveChanges** method, as follows:</span></span> 
  
- <span data-ttu-id="0068f-115">Некоторые свойства должны быть доступны для чтения/записи до вызова**SaveChanges**, а после должны быть доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0068f-115">Some properties should be read/write before **SaveChanges** is called, but read-only afterward.</span></span> <span data-ttu-id="0068f-116">Например, **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) определяется изначально клиентским приложением, которое создает сообщение (и поэтому может быть доступно для чтения и записи), но внести изменения будет нельзя после первого вызова \*\* SaveChanges\*\*.</span><span class="sxs-lookup"><span data-stu-id="0068f-116">For example, **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) is set initially by the client application that creates the message (and thus is read/write) but cannot be changed after the first call to **SaveChanges**.</span></span>
    
- <span data-ttu-id="0068f-p105">Некоторые свойства имеют особенные связи со свойствами папки, которые связаны с методами **IMAPIFolder**. Например, свойство **PR_MESSAGE_FLAGS** связано с флагами, которые используются вызовом [IMAPIFolder::CreateMessage](imapifolder-createmessage.md).</span><span class="sxs-lookup"><span data-stu-id="0068f-p105">Some properties have special relations to properties on the folder they are in or to **IMAPIFolder** methods. For example, the **PR_MESSAGE_FLAGS** property is related to the flags used on the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) call.</span></span> 
    
- <span data-ttu-id="0068f-119">Некоторые свойства могут быть недоступны до первого вызова **SaveChanges**.</span><span class="sxs-lookup"><span data-stu-id="0068f-119">Some properties may not be available until **SaveChanges** is called for the first time.</span></span> <span data-ttu-id="0068f-120">Например, свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) может быть недоступно до вызова **SaveChanges**.</span><span class="sxs-lookup"><span data-stu-id="0068f-120">For example, the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property may not be available until **SaveChanges** is called.</span></span> 
    
- <span data-ttu-id="0068f-121">Некоторые свойства могут иметь специальные связи с другими свойствами объекта сообщения.</span><span class="sxs-lookup"><span data-stu-id="0068f-121">Some properties can have special relationships to other properties on the message object.</span></span> <span data-ttu-id="0068f-122">Например, свойство**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) обычно получают из свойства **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) поставщиков услуг хранилища сообщений, которые поддерживают сообщения в формате RTF.</span><span class="sxs-lookup"><span data-stu-id="0068f-122">For example, the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property is usually derived from the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property in message store providers that support Rich Text Format messages.</span></span>
    
- <span data-ttu-id="0068f-123">Некоторые свойства используются более чем одним типом объекта, связанным с сообщением.</span><span class="sxs-lookup"><span data-stu-id="0068f-123">Some properties are used by more than one object type related to message stores.</span></span> <span data-ttu-id="0068f-124">Например, свойство **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) требуется для объектов папки и сообщения, а также объектов хранилища сообщения.</span><span class="sxs-lookup"><span data-stu-id="0068f-124">For example, the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property is required on folder and message objects as well as message store objects.</span></span>
    
<span data-ttu-id="0068f-125">В ответственность поставщика услуг хранилища сообщения входит реализации правильной семантики для таких свойств.</span><span class="sxs-lookup"><span data-stu-id="0068f-125">It is the responsibility of the message store provider to implement the correct semantics for such properties.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0068f-126">См. также</span><span class="sxs-lookup"><span data-stu-id="0068f-126">See also</span></span>



[<span data-ttu-id="0068f-127">Включение сообщений в хранилищах сообщений</span><span class="sxs-lookup"><span data-stu-id="0068f-127">Implementing Messages in Message Stores</span></span>](implementing-messages-in-message-stores.md)

