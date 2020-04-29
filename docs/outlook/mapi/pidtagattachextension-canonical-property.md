---
title: Каноническое свойство PidTagAttachExtension
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachExtension
api_type:
- HeaderDef
ms.assetid: 667da30b-e11c-4040-aecf-bb35eed23722
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 26efa868de29bc8a6a180b717230951b76da26a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319763"
---
# <a name="pidtagattachextension-canonical-property"></a>Каноническое свойство PidTagAttachExtension

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит расширение имени файла, которое указывает тип документа вложения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A PR_ATTACH_EXTENSION_W  <br/> |
|Идентификатор:  <br/> |0x3703  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства задаются клиентским приложением во время отправки. 
  
Система обмена сообщениями использует **PR_ATTACH_EXTENSION** при преобразовании вложений в сообщениях (преобразования in-Route) или запуске приложений на основе вложений в полученных сообщениях. Если клиент-отправитель не предоставляет значение для этих свойств, то обработка хранилища сообщений с вложением не имеет обязательств по его созданию. Принимающий клиент должен сначала проверить наличие **PR_ATTACH_EXTENSION**, а если он не указан, следует проанализировать расширение имени файла из свойства **PR_ATTACH_FILENAME** вложения ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) или **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)). 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

