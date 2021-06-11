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
# <a name="handling-an-outgoing-message"></a>Обработка исходящего сообщения

**Область применения**: Outlook 2013 | Outlook 2016 
  
Исходяние сообщения — это сообщение, которое может быть отправлено одному или более получателям через одну или несколько систем обмена сообщениями или отправлено в папку в хранилище сообщений.
  
## <a name="create-and-send-an-outgoing-message"></a>Создание и отправка исходя из сообщения
  
1. Откройте хранилище сообщений по умолчанию. Дополнительные сведения см. в [тексте Открытие магазина сообщений](opening-a-message-store.md) и открытие магазина сообщений [по умолчанию.](opening-the-default-message-store.md)
    
2. Откройте папку "Избокс". Дополнительные сведения см. в [сообщении "Открытие папки магазина сообщений".](opening-a-message-store-folder.md)
    
3. Чтобы создать новое сообщение, вызовите метод **IMAPIFolder::CreateMessage** папки". Дополнительные сведения см. [в странице IMAPIFolder::CreateMessage](imapifolder-createmessage.md),
    
4. Создайте список получателей с одним или более разрешенными получателями. Дополнительные сведения см. в [списке "Создание списка получателей".](creating-a-recipient-list.md)
    
5. Дополнительно добавьте субъект. Дополнительные сведения см. в [тексте Создание темы сообщения.](creating-a-message-subject.md)
    
6. Добавьте текст сообщения. Дополнительные сведения см. в [сообщении Creating Message Text.](creating-message-text.md)
    
7. Если текст сообщения форматирован, добавьте сведения о отрисовки. Дополнительные сведения см. в [добавлении сведений о отрисовки в форматированный текст.](adding-rendering-information-to-formatted-text.md)
    
8. Дополнительно добавьте одно или несколько вложений. Дополнительные сведения см. в [сообщении Creating a Message Attachment](creating-a-message-attachment.md).
    
9. Установите другие свойства сообщений по желанию, а затем сохраните и отправьте сообщение, позвонив **в IMessage::SubmitMessage**. Дополнительные сведения см. [в странице IMessage::SubmitMessage](imessage-submitmessage.md).
    
10. Удалите отправленное **\_ сообщение, если** свойство PR DELETE_AFTER_SUBMIT [(PidTagDeleteAfterSubmit)](pidtagdeleteaftersubmit-canonical-property.md)настроено на TRUE или  переместите его в папку, идентифицированную свойством [PR_SENTMAIL_ENTRYID (PidTagSentMailEntryId).](pidtagsentmailentryid-canonical-property.md) Дополнительные сведения см. в [тексте Обработка отправленного сообщения.](processing-a-sent-message.md)
    
Если перед отправкой необходимо периодически сохранять сообщение, позвоните в [метод IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Дополнительные сведения см. в ["Сохранение сообщения"](saving-a-message.md) или ["Отправка сообщения".](sending-a-message.md) 
  
## <a name="in-this-section"></a>В этом разделе

- [Создание списка получателей](creating-a-recipient-list.md). Описывает, как создать список получателей.
    
- [Создание темы сообщения.](creating-a-message-subject.md)Описывает, как создать необязательный субъект для сообщения.
    
- [Создание текста сообщения](creating-message-text.md). Описывает, как создать текст сообщения.
    
- [Добавление сведений о отрисовки в форматированный текст:](adding-rendering-information-to-formatted-text.md)Описывает, где в форматном тексте должно быть отрисовка вложения.
    
- [Создание вложения сообщений.](creating-a-message-attachment.md)Описывает, как создавать вложения.
    
- [Сохранение сообщения](saving-a-message.md). Описывает, как клиенты экономят сообщения.
    
- [Отправка сообщения.](sending-a-message.md)Описывает, как отправлять сообщение.
    
- [Обработка отправленного сообщения](processing-a-sent-message.md). Описывает, как можно обрабатывать отправленные сообщения.
    

