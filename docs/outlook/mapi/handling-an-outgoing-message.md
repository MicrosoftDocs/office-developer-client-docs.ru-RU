---
title: Обработка исходящих сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f40c2e0b-1a35-4901-868f-af6c191c921e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3f3330c132abdf35d0e4f67775c03f7d2e9fcc76
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563991"
---
# <a name="handling-an-outgoing-message"></a><span data-ttu-id="0cc6b-103">Обработка исходящих сообщений</span><span class="sxs-lookup"><span data-stu-id="0cc6b-103">Handling an outgoing message</span></span>

<span data-ttu-id="0cc6b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0cc6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0cc6b-105">Исходящее сообщение — это сообщение, который может быть отправлен для одного или нескольких получателей через один или несколько систем обмена сообщениями или учитываться в папку в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-105">An outgoing message is a message that can be sent to one or more recipients across one or more messaging systems or be posted to a folder in a message store.</span></span>
  
## <a name="create-and-send-an-outgoing-message"></a><span data-ttu-id="0cc6b-106">Создание и отправка исходящих сообщений</span><span class="sxs-lookup"><span data-stu-id="0cc6b-106">Create and send an outgoing message</span></span>
  
1. <span data-ttu-id="0cc6b-107">Откройте хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-107">Open the default message store.</span></span> <span data-ttu-id="0cc6b-108">Для получения дополнительных сведений см [открытии хранилища сообщений](opening-a-message-store.md) и [Открытие хранилище сообщений по умолчанию](opening-the-default-message-store.md).</span><span class="sxs-lookup"><span data-stu-id="0cc6b-108">For more information, see [Opening a Message Store](opening-a-message-store.md) and [Opening the Default Message Store](opening-the-default-message-store.md).</span></span>
    
2. <span data-ttu-id="0cc6b-109">Откройте папку "Исходящие".</span><span class="sxs-lookup"><span data-stu-id="0cc6b-109">Open the Outbox folder.</span></span> <span data-ttu-id="0cc6b-110">Дополнительные сведения можно [открывать папки хранения сообщений](opening-a-message-store-folder.md).</span><span class="sxs-lookup"><span data-stu-id="0cc6b-110">For more information, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span>
    
3. <span data-ttu-id="0cc6b-111">Вызов метода **IMAPIFolder::CreateMessage** папке Исходящие для создания нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-111">Call the Outbox folder's **IMAPIFolder::CreateMessage** method to create the new message.</span></span> <span data-ttu-id="0cc6b-112">Для получения дополнительных сведений см [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)</span><span class="sxs-lookup"><span data-stu-id="0cc6b-112">For more information, see [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),</span></span>
    
4. <span data-ttu-id="0cc6b-113">Создание списка получателей с помощью одного или нескольких получателей возможности разрешения.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-113">Create a recipient list with one or more resolved recipients.</span></span> <span data-ttu-id="0cc6b-114">[Список получателей](creating-a-recipient-list.md)для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-114">For more information, see [Creating a Recipient List](creating-a-recipient-list.md).</span></span>
    
5. <span data-ttu-id="0cc6b-115">При необходимости добавьте тему.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-115">Optionally, add a subject.</span></span> <span data-ttu-id="0cc6b-116">[Тема сообщения](creating-a-message-subject.md)для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-116">For more information, see [Creating a Message Subject](creating-a-message-subject.md).</span></span>
    
6. <span data-ttu-id="0cc6b-117">Добавление текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-117">Add the message text.</span></span> <span data-ttu-id="0cc6b-118">Дополнительные сведения содержатся в разделе [Создание текста сообщения](creating-message-text.md).</span><span class="sxs-lookup"><span data-stu-id="0cc6b-118">For more information, see [Creating Message Text](creating-message-text.md).</span></span>
    
7. <span data-ttu-id="0cc6b-119">Если формат текста сообщения, добавьте сведения о визуализации.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-119">If the message text is formatted, add rendering information.</span></span> <span data-ttu-id="0cc6b-120">Для получения дополнительных сведений см [Добавление отображения информации в форматированный текст](adding-rendering-information-to-formatted-text.md).</span><span class="sxs-lookup"><span data-stu-id="0cc6b-120">For more information, see [Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md).</span></span>
    
8. <span data-ttu-id="0cc6b-121">При необходимости добавьте один или несколько вложений.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-121">Optionally, add one or more attachments.</span></span> <span data-ttu-id="0cc6b-122">[Вложения сообщения](creating-a-message-attachment.md)для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-122">For more information, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
9. <span data-ttu-id="0cc6b-123">При необходимости задайте другие свойства сообщений и затем сохранить и отправить сообщение путем вызова **IMessage::SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-123">Set other message properties as desired and then save and send the message by calling **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="0cc6b-124">Для получения дополнительных сведений см [IMessage::SubmitMessage](imessage-submitmessage.md).</span><span class="sxs-lookup"><span data-stu-id="0cc6b-124">For more information, see [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span>
    
10. <span data-ttu-id="0cc6b-125">Удаление отправленное сообщение, если **связей с Общественностью\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) свойству присвоено значение TRUE или перемещения его в папку определяемую свойством **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0cc6b-125">Delete the sent message if the **PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property is set to TRUE or move it to the folder identified by the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="0cc6b-126">[Сообщение отправлено](processing-a-sent-message.md)для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-126">For more information, see [Processing a Sent Message](processing-a-sent-message.md).</span></span>
    
<span data-ttu-id="0cc6b-127">Если вы хотите intermittantly сохранить сообщение перед отправкой, вызовите метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сообщение.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-127">If you want to intermittantly save the message before sending it, call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="0cc6b-128">Для получения дополнительных сведений см, [Сохранение сообщения](saving-a-message.md) или [Отправка сообщения](sending-a-message.md).</span><span class="sxs-lookup"><span data-stu-id="0cc6b-128">For more information, see, [Saving a Message](saving-a-message.md) or [Sending a Message](sending-a-message.md).</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="0cc6b-129">В этой статье</span><span class="sxs-lookup"><span data-stu-id="0cc6b-129">In this section</span></span>

- <span data-ttu-id="0cc6b-130">[Создание списка получателей](creating-a-recipient-list.md): описывает порядок создания списка получателей.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-130">[Creating a Recipient List](creating-a-recipient-list.md): Describes how to create a recipient list.</span></span>
    
- <span data-ttu-id="0cc6b-131">[Создание тема сообщения](creating-a-message-subject.md): описывается, как создать дополнительные темы сообщения.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-131">[Creating a Message Subject](creating-a-message-subject.md): Describes how to create an optional subject for a message.</span></span>
    
- <span data-ttu-id="0cc6b-132">[Создание текста сообщения](creating-message-text.md): Описание создания текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-132">[Creating Message Text](creating-message-text.md): Describes how to create message text.</span></span>
    
- <span data-ttu-id="0cc6b-133">[Добавление визуализации сведения, которые текст в формате](adding-rendering-information-to-formatted-text.md): описывается, где в форматированный текст вложения для отображения.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-133">[Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md): Describes where in formatted text an attachment is to be rendered.</span></span>
    
- <span data-ttu-id="0cc6b-134">[Создание вложения сообщения](creating-a-message-attachment.md): описывает порядок создания вложения.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-134">[Creating a Message Attachment](creating-a-message-attachment.md): Describes how to create attachments.</span></span>
    
- <span data-ttu-id="0cc6b-135">[Сохранение сообщения](saving-a-message.md): описывает, как клиенты сохраняются сообщения.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-135">[Saving a Message](saving-a-message.md): Describes how clients save messages.</span></span>
    
- <span data-ttu-id="0cc6b-136">[Отправка сообщения](sending-a-message.md): описывается, как отправить сообщение.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-136">[Sending a Message](sending-a-message.md): Describes how to send a message.</span></span>
    
- <span data-ttu-id="0cc6b-137">[Обработка сообщений, отправленных](processing-a-sent-message.md): описывается, как отправлять сообщения могут быть обработаны.</span><span class="sxs-lookup"><span data-stu-id="0cc6b-137">[Processing a Sent Message](processing-a-sent-message.md): Describes how to sent messages can be processed.</span></span>
    

