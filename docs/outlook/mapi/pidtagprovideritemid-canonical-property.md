---
title: Каноническое свойство PidTagProviderItemId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderItemId
api_type:
- COM
ms.assetid: fadbf1af-32c2-43ea-8475-15b31b2a9e68
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 48653b86d625da963b655dbd1acc01a46f4687dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412123"
---
# <a name="pidtagprovideritemid-canonical-property"></a>Каноническое свойство PidTagProviderItemId

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает идентификатор для папки или элемента в хранилище.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROVIDER_ITEMID  <br/> |
|Идентификатор:  <br/> |0x0EA3  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |мапинонтрансмиттабле  <br/> |
   
## <a name="remarks"></a>Примечания

Поставщики хранилища могут указывать значение этого свойства для папки или элемента, но должны поддерживать одинаковое значение между сеансами. Поставщики магазина это свойство используется для определения результатов поиска, возвращаемых из поисковой системы.
  
## <a name="related-resources"></a>Связанные ресурсы

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

