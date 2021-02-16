---
title: Сохранение сообщения в почтовом ящике
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 672a9df55ce711b88451a517a2813c9ad8c599ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407895"
---
# <a name="saving-a-message-in-the-inbox"></a>Сохранение сообщения в почтовом ящике

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
 **Хранение сообщения в почтовой ящике без получателей**
  
1. Вызовите [IMsgStore::GetReceiveFolder,](imsgstore-getreceivefolder.md) чтобы получить идентификатор записи для входящих сообщений. 
    
2. Вызовите [IMsgStore::OpenEntry,](imsgstore-openentry.md) чтобы открыть "Входящие" и получить на него указатель. 
    
3. Вызовите метод [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) почтового ящика, чтобы создать сообщение. 
    
4. Вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) сообщения, чтобы добавить свойства **PR_BODY** ([PidTagBody),](pidtagbody-canonical-property.md) **PR_HTML** ([PidTagHtml)](pidtaghtml-canonical-property.md)или **PR_RTF_COMPRESSED** ([PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)и **PR_SUBJECT** ([PidTagSubject).](pidtagsubject-canonical-property.md) 
    
5. Создайте каждое вложение, установите его свойства и сохраните его. Дополнительные сведения о добавлении вложений в сообщения см. в описании [создания вложения в сообщение.](creating-a-message-attachment.md)
    
6. Вызовите **IMessage::SaveChanges,** чтобы сохранить сообщение. На этом этапе он появится в таблице содержимого в "Входящие". 
    
Если вы хотите периодически сохранять сообщение, прежде чем оно появится в таблице содержимого папки "Входящие", создайте его в скрытой папке, например в корневой папке поддерева IPM, а затем переместите его в папку "Входящие". 
  

