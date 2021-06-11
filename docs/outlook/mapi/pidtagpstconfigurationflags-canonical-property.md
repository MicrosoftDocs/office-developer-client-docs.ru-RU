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
ms.openlocfilehash: e881c8eeffa29706591e07113d70a3670606f2be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408945"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a>Каноническое свойство PidTagPstConfigurationFlags
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Specfies configuration flags for a personal storage table (.pst file).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PST_CONFIG_FLAGS  <br/> |
|Идентификатор:  <br/> |0x6770  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Внутренняя таблица персонального хранения (PST)  <br/> |
   
## <a name="remarks"></a>Примечания

Для этого свойства допустимы следующие значения:
  
PST_CONFIG_UNICODE
  
> Указывает файл Unicode .pst. 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
PST_CONFIG_CREATE_NOWARN
  
> При задав флажки клиента методу [IMsgServiceAdmin:::ConfigureMsgService,](imsgserviceadmin-configuremsgservice.md) можно **настроитьMsgService** как вызов [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) и пропустить предупреждение "Эта информационная служба не настроена". 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
PST_CONFIG_PRESERVE_DISPLAY_NAME
  
> Сообщает **ConfigureMsgService,** чтобы не **изменять** значение свойства [PR_DISPLAY_NAME (PidTagDisplayName),](pidtagdisplayname-canonical-property.md)даже если оно было поставлено. В этом случае она поставлялась только для новых файлов pst.
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
OST_CONFIG_POLICY_DELAY_IGNORE_OST
  
> Сообщает коду конфигурации сначала отобразить диалоговое окно, чтобы подтвердить, найден ли файл автономной папки (.ost), и в зависимости от ответа пользователя используйте найденную офлайновую папку или введите пользователю возможность просмотра другой автономной папки.
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
OST_CONFIG_CREATE_NEW_DEFAULT
  
> Копирует файл .ost с новым уникальным именем и отбрасывается текущее имя. Существующий файл .ost остается на компьютере, но больше не используется в этом профиле. Обычно это происходит, когда microsoft Outlook больше не разрешает определенный файл .ost, а политики реестра не позволяют пользователю переименовать файл. 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]] 
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
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

