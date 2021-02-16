---
title: Каноническое свойство PidTagMessageAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageAttachments
api_type:
- HeaderDef
ms.assetid: 85762771-b823-4227-9a7b-75b6ac280b2d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 975f52e6ea0ca7a469a027565f845f9dc0f9c2cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342569"
---
# <a name="pidtagmessageattachments-canonical-property"></a>Каноническое свойство PidTagMessageAttachments

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит таблицу вложений для сообщения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MESSAGE_ATTACHMENTS  <br/> |
|Идентификатор:  <br/> |0x0E13  <br/> |
|Тип данных:  <br/> |PT_OBJECT  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство можно исключить в операциях [IMAPIProp::CopyTo](imapiprop-copyto.md) или включить в операции [IMAPIProp::CopyProps.](imapiprop-copyprops.md) В качестве свойства типа PT_OBJECT его не удается получить с помощью метода [IMAPIProp::GetProps.](imapiprop-getprops.md) Доступ к его содержимому должен получить метод [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) запрашивающий идентификатор IID_IMAPITable интерфейса.  Поставщики служб должны сообщить о нем методу [IMAPIProp::GetPropList,](imapiprop-getproplist.md) если он установлен, но при желании может сообщить о нем или нет, если он не за установлен. 
  
Чтобы получить содержимое таблицы, клиентские приложения должны вызвать [метод IMessage::GetAttachmentTable.](imessage-getattachmenttable.md) For more information, see [������� ��������](attachment-tables.md). 
  
Это свойство можно использовать для ограничения подобектов, указав его в структуре [SSubRestriction.](ssubrestriction.md) Это позволяет клиенту ограничить представление контейнера сообщениями с вложениями, которые соответствуют заданным критериям. Сообщение квалификаторы для просмотра, если по крайней мере одна строка в таблице вложений, то есть одно вложение, удовлетворяет ограничению subobject. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)
  
> Определяет основные структуры данных, используемые в удаленных операциях.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Определяет основные структуры данных, используемые в удаленных операциях.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразуется между IETF RFC2445, RFC2446 и RFC2447, а также объектами встреч и собраний.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

