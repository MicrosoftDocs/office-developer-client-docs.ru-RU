---
title: Каноническое свойство PidTagTransmittableDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTransmittableDisplayName
api_type:
- COM
ms.assetid: aadd9086-b936-4067-bf7d-f54fc50e3c83
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e66fe8d3621c122ccc19bdde169f20f7d47a148d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396885"
---
# <a name="pidtagtransmittabledisplayname-canonical-property"></a>Каноническое свойство PidTagTransmittableDisplayName

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит отображаемое имя получателя в безопасной формы, которая не может быть изменено.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W  <br/> |
|Идентификатор:  <br/> |0x3A20  <br/> |
|Тип данных:  <br/> |PT_UNICODE PT_STRING8  <br/> |
|Область:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства должны реализовывать все поставщиками адресной книги. Они содержат версии отображаемое имя получателя, который передается с сообщением. Для большинства поставщиками адресных книг эти свойства имеют совпадает со значением свойства **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Поставщики, которые не имеют безопасных отображаемое имя возврата PT_ERROR и MAPI изменения отображаемого имени, добавив имя в кавычки.
  
Это свойство можно использовать клиентское приложение для предотвращения изменения или «спуфинг» записей. Пример спуфинг передает Иван Петров как (что Guy) Иван Петров.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Обрабатывает клиентами с сервером интерфейса поставщика имя службы (NSPI).
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и поток для передачи данных между клиентом и сервером.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

