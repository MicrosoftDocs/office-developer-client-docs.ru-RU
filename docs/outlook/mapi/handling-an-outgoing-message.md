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
# <a name="handling-an-outgoing-message"></a><span data-ttu-id="bef6f-103">Обработка исходящего сообщения</span><span class="sxs-lookup"><span data-stu-id="bef6f-103">Handling an outgoing message</span></span>

<span data-ttu-id="bef6f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bef6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bef6f-105">Исходяние сообщения — это сообщение, которое может быть отправлено одному или более получателям через одну или несколько систем обмена сообщениями или отправлено в папку в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="bef6f-105">An outgoing message is a message that can be sent to one or more recipients across one or more messaging systems or be posted to a folder in a message store.</span></span>
  
## <a name="create-and-send-an-outgoing-message"></a><span data-ttu-id="bef6f-106">Создание и отправка исходя из сообщения</span><span class="sxs-lookup"><span data-stu-id="bef6f-106">Create and send an outgoing message</span></span>
  
1. <span data-ttu-id="bef6f-107">Откройте хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bef6f-107">Open the default message store.</span></span> <span data-ttu-id="bef6f-108">Дополнительные сведения см. в [тексте Открытие магазина сообщений](opening-a-message-store.md) и открытие магазина сообщений [по умолчанию.](opening-the-default-message-store.md)</span><span class="sxs-lookup"><span data-stu-id="bef6f-108">For more information, see [Opening a Message Store](opening-a-message-store.md) and [Opening the Default Message Store](opening-the-default-message-store.md).</span></span>
    
2. <span data-ttu-id="bef6f-109">Откройте папку "Избокс".</span><span class="sxs-lookup"><span data-stu-id="bef6f-109">Open the Outbox folder.</span></span> <span data-ttu-id="bef6f-110">Дополнительные сведения см. в [сообщении "Открытие папки магазина сообщений".](opening-a-message-store-folder.md)</span><span class="sxs-lookup"><span data-stu-id="bef6f-110">For more information, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span>
    
3. <span data-ttu-id="bef6f-111">Чтобы создать новое сообщение, вызовите метод **IMAPIFolder::CreateMessage** папки".</span><span class="sxs-lookup"><span data-stu-id="bef6f-111">Call the Outbox folder's **IMAPIFolder::CreateMessage** method to create the new message.</span></span> <span data-ttu-id="bef6f-112">Дополнительные сведения см. [в странице IMAPIFolder::CreateMessage](imapifolder-createmessage.md),</span><span class="sxs-lookup"><span data-stu-id="bef6f-112">For more information, see [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),</span></span>
    
4. <span data-ttu-id="bef6f-113">Создайте список получателей с одним или более разрешенными получателями.</span><span class="sxs-lookup"><span data-stu-id="bef6f-113">Create a recipient list with one or more resolved recipients.</span></span> <span data-ttu-id="bef6f-114">Дополнительные сведения см. в [списке "Создание списка получателей".](creating-a-recipient-list.md)</span><span class="sxs-lookup"><span data-stu-id="bef6f-114">For more information, see [Creating a Recipient List](creating-a-recipient-list.md).</span></span>
    
5. <span data-ttu-id="bef6f-115">Дополнительно добавьте субъект.</span><span class="sxs-lookup"><span data-stu-id="bef6f-115">Optionally, add a subject.</span></span> <span data-ttu-id="bef6f-116">Дополнительные сведения см. в [тексте Создание темы сообщения.](creating-a-message-subject.md)</span><span class="sxs-lookup"><span data-stu-id="bef6f-116">For more information, see [Creating a Message Subject](creating-a-message-subject.md).</span></span>
    
6. <span data-ttu-id="bef6f-117">Добавьте текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="bef6f-117">Add the message text.</span></span> <span data-ttu-id="bef6f-118">Дополнительные сведения см. в [сообщении Creating Message Text.](creating-message-text.md)</span><span class="sxs-lookup"><span data-stu-id="bef6f-118">For more information, see [Creating Message Text](creating-message-text.md).</span></span>
    
7. <span data-ttu-id="bef6f-119">Если текст сообщения форматирован, добавьте сведения о отрисовки.</span><span class="sxs-lookup"><span data-stu-id="bef6f-119">If the message text is formatted, add rendering information.</span></span> <span data-ttu-id="bef6f-120">Дополнительные сведения см. в [добавлении сведений о отрисовки в форматированный текст.](adding-rendering-information-to-formatted-text.md)</span><span class="sxs-lookup"><span data-stu-id="bef6f-120">For more information, see [Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md).</span></span>
    
8. <span data-ttu-id="bef6f-121">Дополнительно добавьте одно или несколько вложений.</span><span class="sxs-lookup"><span data-stu-id="bef6f-121">Optionally, add one or more attachments.</span></span> <span data-ttu-id="bef6f-122">Дополнительные сведения см. в [сообщении Creating a Message Attachment](creating-a-message-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="bef6f-122">For more information, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
9. <span data-ttu-id="bef6f-123">Установите другие свойства сообщений по желанию, а затем сохраните и отправьте сообщение, позвонив **в IMessage::SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="bef6f-123">Set other message properties as desired and then save and send the message by calling **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="bef6f-124">Дополнительные сведения см. [в странице IMessage::SubmitMessage](imessage-submitmessage.md).</span><span class="sxs-lookup"><span data-stu-id="bef6f-124">For more information, see [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span>
    
10. <span data-ttu-id="bef6f-125">Удалите отправленное **\_ сообщение, если** свойство PR DELETE_AFTER_SUBMIT [(PidTagDeleteAfterSubmit)](pidtagdeleteaftersubmit-canonical-property.md)настроено на TRUE или  переместите его в папку, идентифицированную свойством [PR_SENTMAIL_ENTRYID (PidTagSentMailEntryId).](pidtagsentmailentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="bef6f-125">Delete the sent message if the **PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property is set to TRUE or move it to the folder identified by the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="bef6f-126">Дополнительные сведения см. в [тексте Обработка отправленного сообщения.](processing-a-sent-message.md)</span><span class="sxs-lookup"><span data-stu-id="bef6f-126">For more information, see [Processing a Sent Message](processing-a-sent-message.md).</span></span>
    
<span data-ttu-id="bef6f-127">Если перед отправкой необходимо периодически сохранять сообщение, позвоните в [метод IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="bef6f-127">If you want to intermittantly save the message before sending it, call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="bef6f-128">Дополнительные сведения см. в ["Сохранение сообщения"](saving-a-message.md) или ["Отправка сообщения".](sending-a-message.md)</span><span class="sxs-lookup"><span data-stu-id="bef6f-128">For more information, see, [Saving a Message](saving-a-message.md) or [Sending a Message](sending-a-message.md).</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="bef6f-129">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="bef6f-129">In this section</span></span>

- <span data-ttu-id="bef6f-130">[Создание списка получателей](creating-a-recipient-list.md). Описывает, как создать список получателей.</span><span class="sxs-lookup"><span data-stu-id="bef6f-130">[Creating a Recipient List](creating-a-recipient-list.md): Describes how to create a recipient list.</span></span>
    
- <span data-ttu-id="bef6f-131">[Создание темы сообщения.](creating-a-message-subject.md)Описывает, как создать необязательный субъект для сообщения.</span><span class="sxs-lookup"><span data-stu-id="bef6f-131">[Creating a Message Subject](creating-a-message-subject.md): Describes how to create an optional subject for a message.</span></span>
    
- <span data-ttu-id="bef6f-132">[Создание текста сообщения](creating-message-text.md). Описывает, как создать текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="bef6f-132">[Creating Message Text](creating-message-text.md): Describes how to create message text.</span></span>
    
- <span data-ttu-id="bef6f-133">[Добавление сведений о отрисовки в форматированный текст:](adding-rendering-information-to-formatted-text.md)Описывает, где в форматном тексте должно быть отрисовка вложения.</span><span class="sxs-lookup"><span data-stu-id="bef6f-133">[Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md): Describes where in formatted text an attachment is to be rendered.</span></span>
    
- <span data-ttu-id="bef6f-134">[Создание вложения сообщений.](creating-a-message-attachment.md)Описывает, как создавать вложения.</span><span class="sxs-lookup"><span data-stu-id="bef6f-134">[Creating a Message Attachment](creating-a-message-attachment.md): Describes how to create attachments.</span></span>
    
- <span data-ttu-id="bef6f-135">[Сохранение сообщения](saving-a-message.md). Описывает, как клиенты экономят сообщения.</span><span class="sxs-lookup"><span data-stu-id="bef6f-135">[Saving a Message](saving-a-message.md): Describes how clients save messages.</span></span>
    
- <span data-ttu-id="bef6f-136">[Отправка сообщения.](sending-a-message.md)Описывает, как отправлять сообщение.</span><span class="sxs-lookup"><span data-stu-id="bef6f-136">[Sending a Message](sending-a-message.md): Describes how to send a message.</span></span>
    
- <span data-ttu-id="bef6f-137">[Обработка отправленного сообщения](processing-a-sent-message.md). Описывает, как можно обрабатывать отправленные сообщения.</span><span class="sxs-lookup"><span data-stu-id="bef6f-137">[Processing a Sent Message](processing-a-sent-message.md): Describes how to sent messages can be processed.</span></span>
    

