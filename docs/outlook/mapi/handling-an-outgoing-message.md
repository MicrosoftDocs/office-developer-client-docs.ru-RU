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

**Относится к**: Outlook 2013 | Outlook 2016 
  
Исходя сообщение — это сообщение, которое может быть отправлено одному или одному или более получателям в одной или более системах обмена сообщениями или опубликовано в папке в хранилище сообщений.
  
## <a name="create-and-send-an-outgoing-message"></a>Создание и отправка исходяного сообщения
  
1. Откройте хранилище сообщений по умолчанию. Дополнительные сведения см. в сведениях об открытии [и](opening-a-message-store.md) открытии магазина сообщений [по умолчанию.](opening-the-default-message-store.md)
    
2. Откройте папку "Outbox". Дополнительные сведения [см. в открываемой папке магазина сообщений.](opening-a-message-store-folder.md)
    
3. Вызовите метод **IMAPIFolder::CreateMessage** папки "Outbox", чтобы создать новое сообщение. Дополнительные сведения см. в подразделе [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),
    
4. Создайте список получателей с одним или более разрешенными получателями. Дополнительные сведения см. [в теме "Создание списка получателей".](creating-a-recipient-list.md)
    
5. При желании добавьте тему. Дополнительные сведения см. в [теме "Создание темы сообщения".](creating-a-message-subject.md)
    
6. Добавьте текст сообщения. Дополнительные сведения см. в [документе "Создание текста сообщения".](creating-message-text.md)
    
7. Если текст сообщения отформатирован, добавьте сведения об отрисовки. Дополнительные сведения см. в документе ["Добавление сведений об отрисовки в форматированный текст".](adding-rendering-information-to-formatted-text.md)
    
8. При желании добавьте одно или несколько вложений. Дополнительные сведения см. в [теме "Создание вложения сообщения".](creating-a-message-attachment.md)
    
9. При желании задайте другие свойства сообщения, а затем сохраните и отправьте сообщение, вызывая **IMessage::SubmitMessage.** Дополнительные сведения см. в [iMessage::SubmitMessage.](imessage-submitmessage.md)
    
10. Удалите отправленное **\_ сообщение,** если свойству PR DELETE_AFTER_SUBMIT ([PidTagDeleteAfterSubmit)](pidtagdeleteaftersubmit-canonical-property.md)задано true, или переместите его в папку, заданную свойством **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId).](pidtagsentmailentryid-canonical-property.md) Дополнительные сведения см. в [теме "Обработка отправленного сообщения".](processing-a-sent-message.md)
    
Если вы хотите периодически сохранить сообщение перед его отправкой, вызовите метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сообщения. Дополнительные сведения см. в [теме "Сохранение сообщения"](saving-a-message.md) или ["Отправка сообщения".](sending-a-message.md) 
  
## <a name="in-this-section"></a>В этом разделе:

- [Создание списка получателей](creating-a-recipient-list.md): описывает создание списка получателей.
    
- [Создание темы сообщения](creating-a-message-subject.md): описывает создание необязательной темы для сообщения.
    
- [Создание текста сообщения](creating-message-text.md): описывает создание текста сообщения.
    
- [Добавление сведений об](adding-rendering-information-to-formatted-text.md)отрисовки в форматированный текст : описывает, где в форматном тексте должно быть отрисовка вложения.
    
- [Создание вложения в сообщение](creating-a-message-attachment.md): описывает создание вложений.
    
- [Сохранение сообщения](saving-a-message.md): описывает, как клиенты сохранения сообщений.
    
- [Отправка сообщения](sending-a-message.md): описывает, как отправить сообщение.
    
- [Обработка отправленного сообщения](processing-a-sent-message.md): описывает, как можно обрабатывать отправленные сообщения.
    

