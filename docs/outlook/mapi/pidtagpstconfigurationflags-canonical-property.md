---
title: Каноническое свойство PidTagPstConfigurationFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: e4234ddf-d9dc-4dc9-8eda-dbbee151b5d7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b5a3978741f7ecb871e3c3de28e52dffdcf3a74f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811598"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a>Каноническое свойство PidTagPstConfigurationFlags
  
**Относится к**: Outlook 
  
Задает флаги конфигурации для таблицы личных папок (PST-файл).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PST_CONFIG_FLAGS  <br/> |
|Идентификатор:  <br/> |0x6770  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Таблица личных папок (.pst) внутренний  <br/> |
   
## <a name="remarks"></a>Замечания

Ниже приведены допустимые значения для этого свойства:
  
PST_CONFIG_UNICODE
  
> Указывает в Unicode PST-файл. 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
PST_CONFIG_CREATE_NOWARN
  
> При набор из клиента помечает в метод [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) , обрабатывает **ConfigureMsgService** как звонок [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) и пропускает «эта служба сведения не было настроено» Предупреждение. 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
PST_CONFIG_PRESERVE_DISPLAY_NAME
  
> Указывает **ConfigureMsgService** не изменение значение свойства **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), несмотря на то, что он был предоставлен. В этом случае он был предоставлен только для новых PST-файлов.
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
OST_CONFIG_POLICY_DELAY_IGNORE_OST
  
> Указывает конфигурацию на первый экран диалоговое окно для подтверждения, была ли файл автономной папки (OST) найти и, в зависимости от ответа пользователя, либо использовать обнаруженного автономных папок или пользователь может выбрать другую папку автономный режим.
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
OST_CONFIG_CREATE_NEW_DEFAULT
  
> Копирует OST-файла с новым уникальным именем и отменяет текущее имя. Существующие OST-файла остается на компьютере, но больше не используется в этот профиль. Обычно это происходит, когда Microsoft Outlook больше не разрешает определенного OST-файла и политики реестра не разрешает пользователю переименуйте файл. 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]] 
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
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

