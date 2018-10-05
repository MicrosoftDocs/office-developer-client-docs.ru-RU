---
title: Каноническое свойство PidTagDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayName
api_type:
- HeaderDef
ms.assetid: bd094e00-5c60-4bb3-9a45-b943fab52876
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 834141fe3e57fde5e6404776e0ad5ce3b438450e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386420"
---
# <a name="pidtagdisplayname-canonical-property"></a>Каноническое свойство PidTagDisplayName

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит отображаемое имя для данного объекта MAPI. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W  <br/> |
|Идентификатор:  <br/> |0x3001  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Распространенные MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Папки требуют вложенных папок одноуровневого иметь уникальные отображаемые имена. Например если папка содержит два вложенных папок, два вложенных папок нельзя использовать такое же значение для этого свойства. Это ограничение не применяется к другим контейнеров, такие как адресные книги и списки рассылки. 
  
Поставщиков услуг необходимо задать значение этого свойства, чтобы он содержит оба типа и конфигурации сведения о поставщике. Дополнительная информация помогает различать экземпляры поставщиков одного типа. Ненастроенный поставщиков следует использовать строку с именем поставщика. Настроенных поставщиков следует использовать ту же строку и отличительные строки в скобки. Например поставщика хранилища ненастроенный сообщение может задать эти свойства: 
  
Личное хранилище данных
  
Затем настроенную версию может задать эти свойства: 
  
Личное хранилище данных (6 февраля 1998 г.)
  
Для объектов состояния эти свойства содержит имя компонента, который может отображаться в интерфейсе пользователя. 
  
> [!NOTE]
> Запятой нельзя использовать в рамках получателей в системе обмена сообщениями MAPI. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Обрабатывает операции папки.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для контакты и списки рассылки.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразование conventions стандартных электронной почты Интернета объекты сообщений.
    
[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)
  
> Расширяет протокол WebDAV, определяющее, как для запроса и задать дескриптор безопасности Exchange с помощью методов WebDAV.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

