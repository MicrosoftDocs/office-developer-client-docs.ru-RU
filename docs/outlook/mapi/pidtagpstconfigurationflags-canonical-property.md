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
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Флаги конфигурации Спекфиес для таблицы личных запоминающих устройств (PST-файла).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ПСТ_КОНФИГ_ФЛАГС  <br/> |
|Идентификатор:  <br/> |0x6770  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Внутренняя таблица хранения личных данных (PST)  <br/> |
   
## <a name="remarks"></a>Примечания

Ниже приведены допустимые значения для этого свойства.
  
ПСТ_КОНФИГ_УНИКОДЕ
  
> Указывает PST-файл в формате Юникод. 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
ПСТ_КОНФИГ_КРЕАТЕ_НОВАРН
  
> При задании из флагов клиента в метод [имсгсервицеадмин:: конфигуремсгсервице](imsgserviceadmin-configuremsgservice.md) обрабатывает **Конфигуремсгсервице** , как [имсгсервицеадмин:: креатемсгсервице](imsgserviceadmin-createmsgservice.md) Call и пропускает "Эта информационная служба не настроена". предупреждение. 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
ПСТ_КОНФИГ_ПРЕСЕРВЕ_ДИСПЛАЙ_НАМЕ
  
> Указывает **конфигуремсгсервице** не изменять значение свойства **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), несмотря на то, что оно было предоставлено. В этом случае он был предоставлен только для новых PST-файлов.
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
ОСТ_КОНФИГ_ПОЛИЦИ_ДЕЛАЙ_ИГНОРЕ_ОСТ
  
> Указывает коду конфигурации сначала отобразить диалоговое окно, чтобы убедиться, что файл автономных папок (OST) найден, и в зависимости от ответа пользователя либо использовать найденную автономную папку, либо разрешить пользователю просматривать другую автономную папку.
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
ОСТ_КОНФИГ_КРЕАТЕ_НЕВ_ДЕФАУЛТ
  
> Копирует OST-файл с новым уникальным именем и отменяет текущее имя. Существующий OST-файл остается на компьютере, но больше не используется в этом профиле. Обычно это происходит в том случае, если Microsoft Outlook больше не разрешает определенный OST-файл, а политики реестра запрещают пользователю переименовывать файл. 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]] 
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

