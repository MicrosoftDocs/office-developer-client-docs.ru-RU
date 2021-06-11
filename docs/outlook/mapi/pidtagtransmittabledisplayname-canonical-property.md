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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331859"
---
# <a name="pidtagtransmittabledisplayname-canonical-property"></a>Каноническое свойство PidTagTransmittableDisplayName

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит имя отображения получателя в безопасной форме, которую невозможно изменить.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_TRANSMITABLE_DISPLAY_NAME, PR_TRANSMITABLE_DISPLAY_NAME_A, PR_TRANSMITABLE_DISPLAY_NAME_W  <br/> |
|Идентификатор:  <br/> |0x3A20  <br/> |
|Тип данных:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Область:  <br/> |Адрес  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства должны быть реализованы всеми поставщиками адресных книг. Они содержат версию отображаемого имени получателя, которое передается с сообщением. Для большинства поставщиков адресных книг эти свойства имеют такое же значение, как **и PR_DISPLAY_NAME** [(PidTagDisplayName).](pidtagdisplayname-canonical-property.md) Поставщики, у них нет безопасного возврата имени отображения PT_ERROR MAPI изменяет имя отображения, добавляя кавычка вокруг имени.
  
Клиентские приложения могут использовать это свойство для предотвращения изменений или "подмены" записей. Пример спуфинга — передача Джону Доу в качестве Доу Джона (Что такое парень) Doe.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Обрабатывает сообщения клиента с сервером интерфейса поставщика служб имени (NSPI).
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и поток передачи данных между клиентом и сервером.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве связанных свойств.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

