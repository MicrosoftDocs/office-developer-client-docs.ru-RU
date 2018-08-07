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
ms.openlocfilehash: 3c48ded73d924a400632a94feab65f7afca6e526
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812168"
---
# <a name="saving-a-message-in-the-inbox"></a>Сохранение сообщения в папке "Входящие"

  
  
**Относится к**: Outlook 
  
 **Для хранения сообщения в папке "Входящие" без получателей**
  
1. Вызовите [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) , чтобы получить идентификатор записи из папки «Входящие». 
    
2. Вызов [IMsgStore::OpenEntry](imsgstore-openentry.md) для открытия папки «Входящие» и получить указатель на него. 
    
3. Вызов метода [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) папке "Входящие" для создания сообщения. 
    
4. Вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) сообщения, чтобы добавить **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) или **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) и **PR_SUBJECT** ([ PidTagSubject](pidtagsubject-canonical-property.md)) свойства. 
    
5. Создание каждого вложения, задайте его свойства и сохраните его. Подробные сведения о добавлении вложений в сообщения [Вложения сообщения](creating-a-message-attachment.md)см.
    
6. Вызовите **IMessage::SaveChanges** , чтобы сохранить сообщение. На этом этапе оно будет отображаться в таблице содержимое из папки «Входящие». 
    
Если вы хотите сохранить intermittantly сообщение перед его отображаются в таблице содержимое из папки «Входящие», вместо этого создать в скрытой папке, например в корневую папку поддерева IPM и затем перетащить его в папке "Входящие". 
  

