---
title: Обработка исходящего сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f40c2e0b-1a35-4901-868f-af6c191c921e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 07785ac82c41108b4333b3c370e3d2f5bfd1426a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407629"
---
# <a name="handling-an-outgoing-message"></a><span data-ttu-id="0443d-103">Обработка исходящего сообщения</span><span class="sxs-lookup"><span data-stu-id="0443d-103">Handling an outgoing message</span></span>

<span data-ttu-id="0443d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0443d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0443d-105">Исходя сообщение — это сообщение, которое может быть отправлено одному или одному или более получателям в одной или более системах обмена сообщениями или опубликовано в папке в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="0443d-105">An outgoing message is a message that can be sent to one or more recipients across one or more messaging systems or be posted to a folder in a message store.</span></span>
  
## <a name="create-and-send-an-outgoing-message"></a><span data-ttu-id="0443d-106">Создание и отправка исходяного сообщения</span><span class="sxs-lookup"><span data-stu-id="0443d-106">Create and send an outgoing message</span></span>
  
1. <span data-ttu-id="0443d-107">Откройте хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0443d-107">Open the default message store.</span></span> <span data-ttu-id="0443d-108">Дополнительные сведения см. в сведениях об открытии [и](opening-a-message-store.md) открытии магазина сообщений [по умолчанию.](opening-the-default-message-store.md)</span><span class="sxs-lookup"><span data-stu-id="0443d-108">For more information, see [Opening a Message Store](opening-a-message-store.md) and [Opening the Default Message Store](opening-the-default-message-store.md).</span></span>
    
2. <span data-ttu-id="0443d-109">Откройте папку "Outbox".</span><span class="sxs-lookup"><span data-stu-id="0443d-109">Open the Outbox folder.</span></span> <span data-ttu-id="0443d-110">Дополнительные сведения [см. в открываемой папке магазина сообщений.](opening-a-message-store-folder.md)</span><span class="sxs-lookup"><span data-stu-id="0443d-110">For more information, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span>
    
3. <span data-ttu-id="0443d-111">Вызовите метод **IMAPIFolder::CreateMessage** папки "Outbox", чтобы создать новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="0443d-111">Call the Outbox folder's **IMAPIFolder::CreateMessage** method to create the new message.</span></span> <span data-ttu-id="0443d-112">Дополнительные сведения см. в подразделе [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),</span><span class="sxs-lookup"><span data-stu-id="0443d-112">For more information, see [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),</span></span>
    
4. <span data-ttu-id="0443d-113">Создайте список получателей с одним или более разрешенными получателями.</span><span class="sxs-lookup"><span data-stu-id="0443d-113">Create a recipient list with one or more resolved recipients.</span></span> <span data-ttu-id="0443d-114">Дополнительные сведения см. [в теме "Создание списка получателей".](creating-a-recipient-list.md)</span><span class="sxs-lookup"><span data-stu-id="0443d-114">For more information, see [Creating a Recipient List](creating-a-recipient-list.md).</span></span>
    
5. <span data-ttu-id="0443d-115">При желании добавьте тему.</span><span class="sxs-lookup"><span data-stu-id="0443d-115">Optionally, add a subject.</span></span> <span data-ttu-id="0443d-116">Дополнительные сведения см. в [теме "Создание темы сообщения".](creating-a-message-subject.md)</span><span class="sxs-lookup"><span data-stu-id="0443d-116">For more information, see [Creating a Message Subject](creating-a-message-subject.md).</span></span>
    
6. <span data-ttu-id="0443d-117">Добавьте текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="0443d-117">Add the message text.</span></span> <span data-ttu-id="0443d-118">Дополнительные сведения см. в [документе "Создание текста сообщения".](creating-message-text.md)</span><span class="sxs-lookup"><span data-stu-id="0443d-118">For more information, see [Creating Message Text](creating-message-text.md).</span></span>
    
7. <span data-ttu-id="0443d-119">Если текст сообщения отформатирован, добавьте сведения об отрисовки.</span><span class="sxs-lookup"><span data-stu-id="0443d-119">If the message text is formatted, add rendering information.</span></span> <span data-ttu-id="0443d-120">Дополнительные сведения см. в документе ["Добавление сведений об отрисовки в форматированный текст".](adding-rendering-information-to-formatted-text.md)</span><span class="sxs-lookup"><span data-stu-id="0443d-120">For more information, see [Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md).</span></span>
    
8. <span data-ttu-id="0443d-121">При желании добавьте одно или несколько вложений.</span><span class="sxs-lookup"><span data-stu-id="0443d-121">Optionally, add one or more attachments.</span></span> <span data-ttu-id="0443d-122">Дополнительные сведения см. в [теме "Создание вложения сообщения".](creating-a-message-attachment.md)</span><span class="sxs-lookup"><span data-stu-id="0443d-122">For more information, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
9. <span data-ttu-id="0443d-123">При желании задайте другие свойства сообщения, а затем сохраните и отправьте сообщение, вызывая **IMessage::SubmitMessage.**</span><span class="sxs-lookup"><span data-stu-id="0443d-123">Set other message properties as desired and then save and send the message by calling **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="0443d-124">Дополнительные сведения см. в [iMessage::SubmitMessage.](imessage-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="0443d-124">For more information, see [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span>
    
10. <span data-ttu-id="0443d-125">Удалите отправленное **\_ сообщение,** если свойству PR DELETE_AFTER_SUBMIT ([PidTagDeleteAfterSubmit)](pidtagdeleteaftersubmit-canonical-property.md)задано true, или переместите его в папку, заданную свойством **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId).](pidtagsentmailentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="0443d-125">Delete the sent message if the **PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property is set to TRUE or move it to the folder identified by the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="0443d-126">Дополнительные сведения см. в [теме "Обработка отправленного сообщения".](processing-a-sent-message.md)</span><span class="sxs-lookup"><span data-stu-id="0443d-126">For more information, see [Processing a Sent Message](processing-a-sent-message.md).</span></span>
    
<span data-ttu-id="0443d-127">Если вы хотите периодически сохранить сообщение перед его отправкой, вызовите метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сообщения.</span><span class="sxs-lookup"><span data-stu-id="0443d-127">If you want to intermittantly save the message before sending it, call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="0443d-128">Дополнительные сведения см. в [теме "Сохранение сообщения"](saving-a-message.md) или ["Отправка сообщения".](sending-a-message.md)</span><span class="sxs-lookup"><span data-stu-id="0443d-128">For more information, see, [Saving a Message](saving-a-message.md) or [Sending a Message](sending-a-message.md).</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="0443d-129">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="0443d-129">In this section</span></span>

- <span data-ttu-id="0443d-130">[Создание списка получателей](creating-a-recipient-list.md): описывает создание списка получателей.</span><span class="sxs-lookup"><span data-stu-id="0443d-130">[Creating a Recipient List](creating-a-recipient-list.md): Describes how to create a recipient list.</span></span>
    
- <span data-ttu-id="0443d-131">[Создание темы сообщения](creating-a-message-subject.md): описывает создание необязательной темы для сообщения.</span><span class="sxs-lookup"><span data-stu-id="0443d-131">[Creating a Message Subject](creating-a-message-subject.md): Describes how to create an optional subject for a message.</span></span>
    
- <span data-ttu-id="0443d-132">[Создание текста сообщения](creating-message-text.md): описывает создание текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="0443d-132">[Creating Message Text](creating-message-text.md): Describes how to create message text.</span></span>
    
- <span data-ttu-id="0443d-133">[Добавление сведений об](adding-rendering-information-to-formatted-text.md)отрисовки в форматированный текст : описывает, где в форматном тексте должно быть отрисовка вложения.</span><span class="sxs-lookup"><span data-stu-id="0443d-133">[Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md): Describes where in formatted text an attachment is to be rendered.</span></span>
    
- <span data-ttu-id="0443d-134">[Создание вложения в сообщение](creating-a-message-attachment.md): описывает создание вложений.</span><span class="sxs-lookup"><span data-stu-id="0443d-134">[Creating a Message Attachment](creating-a-message-attachment.md): Describes how to create attachments.</span></span>
    
- <span data-ttu-id="0443d-135">[Сохранение сообщения](saving-a-message.md): описывает, как клиенты сохранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="0443d-135">[Saving a Message](saving-a-message.md): Describes how clients save messages.</span></span>
    
- <span data-ttu-id="0443d-136">[Отправка сообщения](sending-a-message.md): описывает, как отправить сообщение.</span><span class="sxs-lookup"><span data-stu-id="0443d-136">[Sending a Message](sending-a-message.md): Describes how to send a message.</span></span>
    
- <span data-ttu-id="0443d-137">[Обработка отправленного сообщения](processing-a-sent-message.md): описывает, как можно обрабатывать отправленные сообщения.</span><span class="sxs-lookup"><span data-stu-id="0443d-137">[Processing a Sent Message](processing-a-sent-message.md): Describes how to sent messages can be processed.</span></span>
    

