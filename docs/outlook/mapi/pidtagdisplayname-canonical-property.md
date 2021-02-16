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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360804"
---
# <a name="pidtagdisplayname-canonical-property"></a>Каноническое свойство PidTagDisplayName

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит отображаемую имя для заданного объекта MAPI. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DISPLAY_NAME, PR_DISPLAY_NAME_A, PR_DISPLAY_NAME_W  <br/> |
|Идентификатор:  <br/> |0x3001  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Общие MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Папки должны иметь уникальные отображаемые имена. Например, если папка содержит две вложенные папки, эти две вложенные папки не могут использовать одно и то же значение для этого свойства. Это ограничение не применяется к другим контейнерам, таким как адресные книги и списки рассылки. 
  
Поставщики услуг должны установить значение этого свойства, чтобы оно содержалось как тип поставщика, так и сведения о конфигурации. Дополнительные сведения помогают различать экземпляры поставщиков одного типа. Ненастроенные поставщики должны использовать строку с именами поставщика. Настроенные поставщики должны использовать ту же строку, за которой следует различающийся строка в скобке. Например, поставщик ненастроенного хранения сообщений может установить для этих свойств: 
  
Хранилище персональных данных
  
Затем настроенная версия может установить для этих свойств: 
  
Хранилище персональных данных (6 февраля 1998 г.)
  
Для объектов состояния эти свойства содержат имя компонента, который может отображаться в пользовательском интерфейсе. 
  
> [!NOTE]
> В сообщениях MAPI нельзя использовать 1000 000 000 получателей. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Обрабатывает операции с папками.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразуется из стандартных интернет-соглашений электронной почты в объекты сообщений.
    
[[MS-XWDVSEC]](https://msdn.microsoft.com/library/dc043d09-6b76-4392-aea3-68f8e81c64d8%28Office.15%29.aspx)
  
> Расширяет протокол WebDAV, который указывает, как запрашивать и устанавливать дескриптор безопасности Exchange с помощью методов WebDAV.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

