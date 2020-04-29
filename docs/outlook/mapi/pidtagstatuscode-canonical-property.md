---
title: Каноническое свойство PidTagStatusCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusCode
api_type:
- COM
ms.assetid: e29190c5-52c3-4ef7-98db-699487c54325
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 751be8abe02dfb1d5bab2bcbbbc0cbd2a8243f85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418516"
---
# <a name="pidtagstatuscode-canonical-property"></a>Каноническое свойство PidTagStatusCode

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит битовую маску флагов, указывающих текущее состояние ресурса сеанса. Все поставщики услуг устанавливают коды состояния как MAPI для создания отчетов о состоянии подсистемы, диспетчере очереди MAPI и интегрированной адресной книге.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_STATUS_CODE  <br/> |
|Идентификатор:  <br/> |0x3E04  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Код состояния должен быть указан в файле Mapisvc. INF для всех поставщиков. 
  
Объекты Status реализуются с помощью MAPI и всех поставщиков услуг. Существует два набора допустимых значений для кодов состояния, один набор для всех объектов status и другой набор для поставщиков транспорта. Все объекты Status могут устанавливать для этого свойства следующие значения:
  
STATUS_AVAILABLE 
  
> Указывает, что ресурс работает.
    
STATUS_FAILURE 
  
> Указывает, что в ресурсе возникла проблема. Для поставщиков услуг STATUS_FAILURE указывает, что поставщик скоро может завершить работу, чтобы завершить текущий сеанс.
    
STATUS_OFFLINE 
  
> Указывает, что доступны только локальные данные или службы.
    
Поставщики транспорта могут также задать следующие значения свойству объектов состояния ' **PR_STATUS_CODE** : 
  
STATUS_INBOUND_ACTIVE 
  
> Указывает, что поставщик транспорта получает входящее сообщение. 
    
STATUS_INBOUND_ENABLED 
  
> Указывает, что поставщик транспорта может принимать входящие сообщения.
    
STATUS_INBOUND_FLUSH 
  
> Указывает, что поставщик транспорта скачивает сообщения из входящей очереди.
    
STATUS_OUTBOUND_ACTIVE 
  
> Указывает, что поставщик транспорта получает исходящее сообщение. 
    
STATUS_OUTBOUND_ENABLED 
  
> Указывает, что поставщик транспорта может обрабатывать исходящие сообщения.
    
STATUS_OUTBOUND_FLUSH 
  
> Указывает на то, что поставщик транспорта отправляет сообщения из исходящей очереди.
    
STATUS_REMOTE_ACCESS 
  
> Указывает, что поставщик транспорта поддерживает удаленный доступ.
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagStatusString](pidtagstatusstring-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

