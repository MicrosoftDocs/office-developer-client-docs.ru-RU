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
ms.openlocfilehash: 672a9df55ce711b88451a517a2813c9ad8c599ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357535"
---
# <a name="saving-a-message-in-the-inbox"></a>Сохранение сообщения в папке "Входящие"

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
 **Сохранение сообщения в папке "Входящие" без получателей**
  
1. Call [IMsgStore:: жетрецеивефолдер](imsgstore-getreceivefolder.md) для получения идентификатора записи папки "Входящие". 
    
2. Call [IMsgStore:: OpenEntry](imsgstore-openentry.md) , чтобы открыть папку "Входящие" и получить указатель на него. 
    
3. ВыЗовите метод [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) для создания сообщения. 
    
4. ВыЗовите метод [IMAPIProp:: SetProps](imapiprop-setprops.md) , чтобы добавить **пр_боди** ([PidTagBody](pidtagbody-canonical-property.md)), **пр_хтмл** ([PidTagHtml](pidtaghtml-canonical-property.md)) или **пр_ртф_компрессед** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) и **пр_субжект** ([ Свойства PidTagSubject](pidtagsubject-canonical-property.md)). 
    
5. Создайте каждое вложение, задайте его свойства и сохраните. Более подробную информацию о добавлении вложений в сообщения можно узнать в статье [Создание вложения сообщения](creating-a-message-attachment.md).
    
6. Call **iMessage:: SaveChanges** для сохранения сообщения. На этом шаге он будет отображаться в таблице содержимое папки "Входящие". 
    
Если вы хотите сохранить сообщение интермиттантли, прежде чем оно будет отображаться в таблице содержимого папки "Входящие", создайте его, а не в скрытой папке, такой как корневая папка поддерева IPM, а затем переместите его в папку "Входящие". 
  

