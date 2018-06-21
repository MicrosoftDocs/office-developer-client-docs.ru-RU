---
title: Каноническое свойство PidTagLastModificationTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLastModificationTime
api_type:
- HeaderDef
ms.assetid: a64e5300-6865-4588-8e1b-158cfd9c60c2
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: bf58e0598af6eb833b003b824be95f8fb82bd8bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/21/2018
ms.locfileid: "19811316"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a>Каноническое свойство PidTagLastModificationTime

  
  
**Применимо к**: Outlook 
  
Содержит дату и время последнего изменения объекта или вложенные объекты. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_LAST_MODIFICATION_TIME  <br/> |
|Идентификатор:  <br/> |0x3008  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Области:  <br/> |Время сообщения  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство изначально установлено значение совпадает со значением свойства **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)). Вложения вложенных можно обновить при необходимости, скопировав времени последнего изменения, задаваемые с помощью собственного файловой системы. Клиентское приложение можно задать это свойство до первого вызова метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . В дальнейшем поставщика следует обновить **PR_LAST_MODIFICATION_TIME** во время каждого вызова **IMAPIProp::SaveChanges** . 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает синхронизации обмена сообщениями объект данных между сервером и клиентом.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Каноническое свойство имена сопоставляемых именам MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI имена каноническое свойств](mapping-mapi-names-to-canonical-property-names.md)

