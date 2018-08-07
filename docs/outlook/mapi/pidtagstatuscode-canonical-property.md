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
ms.openlocfilehash: efd0dcc8fc01fa433cbbf30936244e4818f8b14a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811961"
---
# <a name="pidtagstatuscode-canonical-property"></a>Каноническое свойство PidTagStatusCode

  
  
**Относится к**: Outlook 
  
Содержит битовую маску флагов, которые указывают текущее состояние сеанса ресурсов. Все поставщики услуг задать коды состояния как MAPI для создания отчетов о состоянии подсистема очереди MAPI и встроенная адресной книги.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_STATUS_CODE  <br/> |
|Идентификатор:  <br/> |0x3E04  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Код состояния, которые должны встречаться в файле Mapisvc.inf для всех поставщиков. 
  
Объекты состояния реализуемый MAPI и всех поставщиков услуг. Существует два набора допустимых значений для кодов состояния, один набор для всех объектов состояния и другой набор для только поставщиками транспорта. Все объекты состояния этому свойству можно задать следующие значения:
  
STATUS_AVAILABLE 
  
> Указывает, что ресурс действующие.
    
STATUS_FAILURE 
  
> Указывает, что ресурс является проблема. Для поставщиков услуг STATUS_FAILURE показывает, что поставщик может скоро будет завершена для завершения текущего сеанса.
    
STATUS_OFFLINE 
  
> Указывает, что доступны только локальные данные или служб.
    
Поставщики транспорта можно также задавать их состояние объектов **PR_STATUS_CODE** свойства следующим значениям: 
  
STATUS_INBOUND_ACTIVE 
  
> Указывает, что поставщик транспорта получает входящее сообщение. 
    
STATUS_INBOUND_ENABLED 
  
> Указывает, что входящие сообщения можно получать поставщика транспорта.
    
STATUS_INBOUND_FLUSH 
  
> Указывает, что поставщик транспорта загрузки сообщений из очереди входящих сообщений.
    
STATUS_OUTBOUND_ACTIVE 
  
> Указывает, что поставщик транспорта получает исходящих сообщений. 
    
STATUS_OUTBOUND_ENABLED 
  
> Указывает, что поставщик транспорта может обрабатывать исходящих сообщений.
    
STATUS_OUTBOUND_FLUSH 
  
> Указывает, что поставщик транспорта — это отправка сообщения из очереди исходящих.
    
STATUS_REMOTE_ACCESS 
  
> Указывает, что поставщик транспорта поддерживает удаленный доступ.
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagStatusString](pidtagstatusstring-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

