---
title: Каноническое свойство PidTagUrlComponentName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUrlComponentName
api_type:
- COM
ms.assetid: a21906f9-5408-41ba-a89b-273ab60eeef3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 26a9d432d98c546aefa8f511ba2c4c9bb26cfd80
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400336"
---
# <a name="pidtagurlcomponentname-canonical-property"></a>Каноническое свойство PidTagUrlComponentName

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Имя компонента URL-адрес для сообщения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W  <br/> |
|Идентификатор:  <br/> |0x10F3  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства должны быть уникальными в рамках папку. Если не задан при создании сообщения, хранилища сообщений следует задать эти свойства, на основе различных свойств сообщения, в зависимости от класса сообщения. Например **IPM. Примечание** и **IPM. Встреча** сообщения должны иметь данное свойство установлено на основе свойства **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) и **IPM. Контакт** сообщений должен иметь это свойство заданы на основании свойство **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)). Для большинства классов сообщений этого свойства необходимо основываться на свойство **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

