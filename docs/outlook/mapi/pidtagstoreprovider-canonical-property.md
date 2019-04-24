---
title: Каноническое свойство PidTagStoreProvider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreProvider
api_type:
- COM
ms.assetid: 6f6cc66f-a08e-4f8e-b33a-d3674319248e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6266c9293f54ce764c5b5b0e41d43767490abcf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278710"
---
# <a name="pidtagstoreprovider-canonical-property"></a>Каноническое свойство PidTagStoreProvider

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит определенную поставщиком структуру [мапиуид](mapiuid.md) , которая указывает тип хранилища сообщений. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_МДБ_ПРОВИДЕР  <br/> |
|Идентификатор:  <br/> |0x3414  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Свойства идентификатора  <br/> |
   
## <a name="remarks"></a>Замечания

Структура [мапиуид](mapiuid.md) определяет тип хранилища сообщений. Значение вычисляется поставщиками хранилища сообщений в объектах хранилища сообщений и является уникальным для каждого поставщика. Обычно он используется для просмотра таблицы хранилища сообщений, чтобы найти магазин требуемого типа, например общедоступные папки. 
  
Это свойство является аналогом свойства **пр_аб_провидер_ид** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) для адресных книг. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

