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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит таблицу вложений для сообщения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_МЕССАЖЕ_АТТАЧМЕНТС  <br/> |
|Идентификатор:  <br/> |0x0E13  <br/> |
|Тип данных:  <br/> |ПТ_ОБЖЕКТ  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Комментарии

Это свойство можно исключить в [IMAPIProp:: операции CopyTo](imapiprop-copyto.md) или включено в [IMAPIProp:: копипропс](imapiprop-copyprops.md) Operations. Как свойство типа ПТ_ОБЖЕКТ, оно не может быть успешно получено методом [IMAPIProp::](imapiprop-getprops.md) . К его содержимому должен получать доступ метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , запрашивающий идентификатор интерфейса **иид_имапитабле** . Поставщики услуг должны сообщить о ней методу [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) , если он задан, но при необходимости можно сообщить ему, если он не задан. 
  
Чтобы получить содержимое таблицы, клиентское приложение должно вызвать метод [iMessage:: жетаттачменттабле](imessage-getattachmenttable.md) . For more information, see [������� ��������](attachment-tables.md). 
  
Это свойство можно использовать для ограничения подобъекта, указав его в структуре [ссубрестриктион](ssubrestriction.md) . Это позволяет клиенту ограничить представление контейнера сообщениями с вложениями, которые удовлетворяют заданным условиям. Сообщение просматривается, если по крайней мере одна строка в таблице вложений, то есть одно вложение, удовлетворяет ограничению этого подобъекта. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСКДАТА]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)
  
> Определяет основные структуры данных, используемые в удаленных операциях.
    
[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Определяет основные структуры данных, используемые в удаленных операциях.
    
[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

