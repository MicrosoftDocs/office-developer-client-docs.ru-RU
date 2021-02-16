---
title: Каноническое свойство PidTagConversationKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 52c97d6c-7f4b-4522-aeac-0c1ed8475952
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 00c65dae9bc29fe9cdb310b819ba99d6d46ebfe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334701"
---
# <a name="pidtagconversationkey-canonical-property"></a>Каноническое свойство PidTagConversationKey

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит ключ беседы, используемый в Microsoft Outlook только при поиске **IPM. Сообщения MessageManager,** например сообщения, которые содержат историю загрузки для учетной записи pop3. Это свойство было неподготовлено в Microsoft Exchange Server. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONVERSATION_KEY  <br/> |
|Идентификатор:  <br/> |0x000B  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

При доступе к электронным письмам в виде бесед и преобразовании свойств сообщений в формат [TNEF](transport-neutral-encapsulation-format-tnef.md)не используйте это свойство; вместо этого используйте канонические свойства [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) и [PidTagConversationTopic.](pidtagconversationtopic-canonical-property.md) 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Microsoft Exchange Server протоколы.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Подtree IPM](ipm-subtree.md)
  
[Специальные папки MAPI](mapi-special-folders.md)
  
[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

