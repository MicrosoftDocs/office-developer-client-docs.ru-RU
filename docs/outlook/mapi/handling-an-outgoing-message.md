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
# <a name="handling-an-outgoing-message"></a><span data-ttu-id="9752a-103">Обработка исходящего сообщения</span><span class="sxs-lookup"><span data-stu-id="9752a-103">Handling an outgoing message</span></span>

<span data-ttu-id="9752a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9752a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9752a-105">Исходящее сообщение — это сообщение, которое может быть отправлено одному или нескольким получателям по одной или нескольким системам обмена сообщениями или отправлено в папку в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="9752a-105">An outgoing message is a message that can be sent to one or more recipients across one or more messaging systems or be posted to a folder in a message store.</span></span>
  
## <a name="create-and-send-an-outgoing-message"></a><span data-ttu-id="9752a-106">Создание и отправка исходящего сообщения</span><span class="sxs-lookup"><span data-stu-id="9752a-106">Create and send an outgoing message</span></span>
  
1. <span data-ttu-id="9752a-107">Откройте хранилище сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9752a-107">Open the default message store.</span></span> <span data-ttu-id="9752a-108">Дополнительные сведения см. в разделе [Открытие хранилища сообщений](opening-a-message-store.md) и [Открытие хранилища сообщений по умолчанию](opening-the-default-message-store.md).</span><span class="sxs-lookup"><span data-stu-id="9752a-108">For more information, see [Opening a Message Store](opening-a-message-store.md) and [Opening the Default Message Store](opening-the-default-message-store.md).</span></span>
    
2. <span data-ttu-id="9752a-109">Откройте папку "исХодящие".</span><span class="sxs-lookup"><span data-stu-id="9752a-109">Open the Outbox folder.</span></span> <span data-ttu-id="9752a-110">Дополнительную информацию можно узнать в статье [Открытие папки хранилища сообщений](opening-a-message-store-folder.md).</span><span class="sxs-lookup"><span data-stu-id="9752a-110">For more information, see [Opening a Message Store Folder](opening-a-message-store-folder.md).</span></span>
    
3. <span data-ttu-id="9752a-111">ВыЗовите метод **IMAPIFolder:: CreateMessage** папки "Исходящие", чтобы создать новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="9752a-111">Call the Outbox folder's **IMAPIFolder::CreateMessage** method to create the new message.</span></span> <span data-ttu-id="9752a-112">Дополнительные сведения см. в статье [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md),</span><span class="sxs-lookup"><span data-stu-id="9752a-112">For more information, see [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),</span></span>
    
4. <span data-ttu-id="9752a-113">Создайте список получателей с одним или несколькими разрешенными получателями.</span><span class="sxs-lookup"><span data-stu-id="9752a-113">Create a recipient list with one or more resolved recipients.</span></span> <span data-ttu-id="9752a-114">Дополнительную информацию можно узнать [в статье Создание списка получателей](creating-a-recipient-list.md).</span><span class="sxs-lookup"><span data-stu-id="9752a-114">For more information, see [Creating a Recipient List](creating-a-recipient-list.md).</span></span>
    
5. <span data-ttu-id="9752a-115">При необходимости добавьте тему.</span><span class="sxs-lookup"><span data-stu-id="9752a-115">Optionally, add a subject.</span></span> <span data-ttu-id="9752a-116">Дополнительную информацию можно узнать в статье [Создание темы сообщения](creating-a-message-subject.md).</span><span class="sxs-lookup"><span data-stu-id="9752a-116">For more information, see [Creating a Message Subject](creating-a-message-subject.md).</span></span>
    
6. <span data-ttu-id="9752a-117">Добавьте текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="9752a-117">Add the message text.</span></span> <span data-ttu-id="9752a-118">Дополнительную информацию можно узнать в статье [Создание текста сообщения](creating-message-text.md).</span><span class="sxs-lookup"><span data-stu-id="9752a-118">For more information, see [Creating Message Text](creating-message-text.md).</span></span>
    
7. <span data-ttu-id="9752a-119">Если текст сообщения отформатирован, добавьте сведения об отображении.</span><span class="sxs-lookup"><span data-stu-id="9752a-119">If the message text is formatted, add rendering information.</span></span> <span data-ttu-id="9752a-120">Дополнительную информацию можно узнать [в статье Добавление данных отображения к форматированНому тексту](adding-rendering-information-to-formatted-text.md).</span><span class="sxs-lookup"><span data-stu-id="9752a-120">For more information, see [Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md).</span></span>
    
8. <span data-ttu-id="9752a-121">При необходимости добавьте одно или несколько вложений.</span><span class="sxs-lookup"><span data-stu-id="9752a-121">Optionally, add one or more attachments.</span></span> <span data-ttu-id="9752a-122">Дополнительную информацию можно узнать в статье [Создание вложения сообщения](creating-a-message-attachment.md).</span><span class="sxs-lookup"><span data-stu-id="9752a-122">For more information, see [Creating a Message Attachment](creating-a-message-attachment.md).</span></span>
    
9. <span data-ttu-id="9752a-123">Задайте другие свойства сообщения, а затем сохраните и отправьте сообщение, вызвав **iMessage:: субмитмессаже**.</span><span class="sxs-lookup"><span data-stu-id="9752a-123">Set other message properties as desired and then save and send the message by calling **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="9752a-124">Дополнительные сведения см. в статье [iMessage:: субмитмессаже](imessage-submitmessage.md).</span><span class="sxs-lookup"><span data-stu-id="9752a-124">For more information, see [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span>
    
10. <span data-ttu-id="9752a-125">Удаление отправленного сообщения, если **для\_свойства PR делете_афтер_субмит** ([PIDTAGDELETEAFTERSUBMIT](pidtagdeleteaftersubmit-canonical-property.md)) задано значение true, или оно перемещается в папку, указанную в свойстве **пр_сентмаил_ентрид** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9752a-125">Delete the sent message if the **PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property is set to TRUE or move it to the folder identified by the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="9752a-126">Дополнительную информацию можно узнать [в статье обработка отправленНого сообщения](processing-a-sent-message.md).</span><span class="sxs-lookup"><span data-stu-id="9752a-126">For more information, see [Processing a Sent Message](processing-a-sent-message.md).</span></span>
    
<span data-ttu-id="9752a-127">Если вы хотите, чтобы интермиттантли сохранял сообщение перед его отправкой, вызовите метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) сообщения.</span><span class="sxs-lookup"><span data-stu-id="9752a-127">If you want to intermittantly save the message before sending it, call the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="9752a-128">Дополнительные сведения см. в статье [Сохранение сообщения](saving-a-message.md) или [Отправка сообщения](sending-a-message.md).</span><span class="sxs-lookup"><span data-stu-id="9752a-128">For more information, see, [Saving a Message](saving-a-message.md) or [Sending a Message](sending-a-message.md).</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="9752a-129">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="9752a-129">In this section</span></span>

- <span data-ttu-id="9752a-130">[Создание списка получателей](creating-a-recipient-list.md): инструкции по созданию списка получателей.</span><span class="sxs-lookup"><span data-stu-id="9752a-130">[Creating a Recipient List](creating-a-recipient-list.md): Describes how to create a recipient list.</span></span>
    
- <span data-ttu-id="9752a-131">[Создание темы сообщения](creating-a-message-subject.md): в этой статье описано, как создать необязательную тему сообщения.</span><span class="sxs-lookup"><span data-stu-id="9752a-131">[Creating a Message Subject](creating-a-message-subject.md): Describes how to create an optional subject for a message.</span></span>
    
- <span data-ttu-id="9752a-132">[Создание текста сообщения](creating-message-text.md): инструкции по созданию текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="9752a-132">[Creating Message Text](creating-message-text.md): Describes how to create message text.</span></span>
    
- <span data-ttu-id="9752a-133">[Добавление данных отображения к форматированНому тексту](adding-rendering-information-to-formatted-text.md): описывает, где в форматированном тексте будет отображаться вложение.</span><span class="sxs-lookup"><span data-stu-id="9752a-133">[Adding Rendering Information to Formatted Text](adding-rendering-information-to-formatted-text.md): Describes where in formatted text an attachment is to be rendered.</span></span>
    
- <span data-ttu-id="9752a-134">[Создание вложения сообщения](creating-a-message-attachment.md): инструкции по созданию вложений.</span><span class="sxs-lookup"><span data-stu-id="9752a-134">[Creating a Message Attachment](creating-a-message-attachment.md): Describes how to create attachments.</span></span>
    
- <span data-ttu-id="9752a-135">[Сохранение сообщения](saving-a-message.md): в этой статье описано, как клиенты сохраняют сообщения.</span><span class="sxs-lookup"><span data-stu-id="9752a-135">[Saving a Message](saving-a-message.md): Describes how clients save messages.</span></span>
    
- <span data-ttu-id="9752a-136">[Отправка сообщения](sending-a-message.md): в этой статье описано, как отправить сообщение.</span><span class="sxs-lookup"><span data-stu-id="9752a-136">[Sending a Message](sending-a-message.md): Describes how to send a message.</span></span>
    
- <span data-ttu-id="9752a-137">[Обработка отправленНого сообщения](processing-a-sent-message.md): в этой статье описывается, как можно обработать отправленные сообщения.</span><span class="sxs-lookup"><span data-stu-id="9752a-137">[Processing a Sent Message](processing-a-sent-message.md): Describes how to sent messages can be processed.</span></span>
    

