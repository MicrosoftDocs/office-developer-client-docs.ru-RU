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
ms.openlocfilehash: 4d71a0e26e2043bbaf961ae5096afc5789be36be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810851"
---
# <a name="pidtagattachextension-canonical-property"></a>Каноническое свойство PidTagAttachExtension

  
  
**Относится к**: Outlook 
  
Содержит расширение имени файла, которое указывает тип вложения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W  <br/> |
|Идентификатор:  <br/> |0x3703  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства задаются клиентским приложением во время отправки. 
  
Системы обмена сообщениями системы использует **PR_ATTACH_EXTENSION** при преобразовании вложений сообщений (в маршрут преобразования) или запуск приложений на основании вложений в полученных сообщениях. Если отправитель не предоставляет значение для этих свойств, хранилище сообщений, обработка вложение не обязаны создать его. Получение клиентом сначала проверить **PR_ATTACH_EXTENSION**и если этот параметр не указан следует проанализировать расширение имени файла из **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) или **PR_ATTACH_LONG_FILENAME вложения **Свойство ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)). 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
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

