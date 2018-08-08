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
ms.openlocfilehash: ab293ee3813d77c3a954e8364736a89bc2330feb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808548"
---
# <a name="handling-an-outgoing-message"></a>Обработка исходящих сообщений

**Относится к**: Outlook 
  
Исходящее сообщение — это сообщение, который может быть отправлен для одного или нескольких получателей через один или несколько систем обмена сообщениями или учитываться в папку в хранилище сообщений.
  
## <a name="create-and-send-an-outgoing-message"></a>Создание и отправка исходящих сообщений
  
1. Откройте хранилище сообщений по умолчанию. Для получения дополнительных сведений см [открытии хранилища сообщений](opening-a-message-store.md) и [Открытие хранилище сообщений по умолчанию](opening-the-default-message-store.md).
    
2. Откройте папку "Исходящие". Дополнительные сведения можно [открывать папки хранения сообщений](opening-a-message-store-folder.md).
    
3. Вызов метода **IMAPIFolder::CreateMessage** папке Исходящие для создания нового сообщения. Для получения дополнительных сведений см [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)
    
4. Создание списка получателей с помощью одного или нескольких получателей возможности разрешения. [Список получателей](creating-a-recipient-list.md)для получения дополнительных сведений см.
    
5. При необходимости добавьте тему. [Тема сообщения](creating-a-message-subject.md)для получения дополнительных сведений см.
    
6. Добавление текста сообщения. Дополнительные сведения содержатся в разделе [Создание текста сообщения](creating-message-text.md).
    
7. Если формат текста сообщения, добавьте сведения о визуализации. Для получения дополнительных сведений см [Добавление отображения информации в форматированный текст](adding-rendering-information-to-formatted-text.md).
    
8. При необходимости добавьте один или несколько вложений. [Вложения сообщения](creating-a-message-attachment.md)для получения дополнительных сведений см.
    
9. При необходимости задайте другие свойства сообщений и затем сохранить и отправить сообщение путем вызова **IMessage::SubmitMessage**. Для получения дополнительных сведений см [IMessage::SubmitMessage](imessage-submitmessage.md).
    
10. Удаление отправленное сообщение, если **связей с Общественностью\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) свойству присвоено значение TRUE или перемещения его в папку определяемую свойством **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)). [Сообщение отправлено](processing-a-sent-message.md)для получения дополнительных сведений см.
    
Если вы хотите intermittantly сохранить сообщение перед отправкой, вызовите метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сообщение. Для получения дополнительных сведений см, [Сохранение сообщения](saving-a-message.md) или [Отправка сообщения](sending-a-message.md). 
  
## <a name="in-this-section"></a>В этой статье

- [Создание списка получателей](creating-a-recipient-list.md): описывает порядок создания списка получателей.
    
- [Создание тема сообщения](creating-a-message-subject.md): описывается, как создать дополнительные темы сообщения.
    
- [Создание текста сообщения](creating-message-text.md): Описание создания текста сообщения.
    
- [Добавление визуализации сведения, которые текст в формате](adding-rendering-information-to-formatted-text.md): описывается, где в форматированный текст вложения для отображения.
    
- [Создание вложения сообщения](creating-a-message-attachment.md): описывает порядок создания вложения.
    
- [Сохранение сообщения](saving-a-message.md): описывает, как клиенты сохраняются сообщения.
    
- [Отправка сообщения](sending-a-message.md): описывается, как отправить сообщение.
    
- [Обработка сообщений, отправленных](processing-a-sent-message.md): описывается, как отправлять сообщения могут быть обработаны.
    

