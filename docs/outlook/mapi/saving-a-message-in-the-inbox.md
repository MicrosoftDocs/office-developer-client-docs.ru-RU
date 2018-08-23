---
title: Сохранение сообщения в папке "Входящие"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e79133ed4928495dcf75b59877a82d3228773883
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586286"
---
# <a name="saving-a-message-in-the-inbox"></a>Сохранение сообщения в папке "Входящие"

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
 **Для хранения сообщения в папке "Входящие" без получателей**
  
1. Вызовите [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) , чтобы получить идентификатор записи из папки «Входящие». 
    
2. Вызов [IMsgStore::OpenEntry](imsgstore-openentry.md) для открытия папки «Входящие» и получить указатель на него. 
    
3. Вызов метода [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) папке "Входящие" для создания сообщения. 
    
4. Вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) сообщения, чтобы добавить **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) или **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) и **PR_SUBJECT** ([ PidTagSubject](pidtagsubject-canonical-property.md)) свойства. 
    
5. Создание каждого вложения, задайте его свойства и сохраните его. Подробные сведения о добавлении вложений в сообщения [Вложения сообщения](creating-a-message-attachment.md)см.
    
6. Вызовите **IMessage::SaveChanges** , чтобы сохранить сообщение. На этом этапе оно будет отображаться в таблице содержимое из папки «Входящие». 
    
Если вы хотите сохранить intermittantly сообщение перед его отображаются в таблице содержимое из папки «Входящие», вместо этого создать в скрытой папке, например в корневую папку поддерева IPM и затем перетащить его в папке "Входящие". 
  

