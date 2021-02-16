---
title: Каноническое свойство PidTagProviderOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderOrdinal
api_type:
- COM
ms.assetid: d062b54d-7c32-4369-ab69-f7193773a1c0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fbeb63bbae23f8f7f78c92d3abed6bea1c3ac85d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438353"
---
# <a name="pidtagproviderordinal-canonical-property"></a>Каноническое свойство PidTagProviderOrdinal

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит индекс позиции поставщика услуг на основе нуля в таблице поставщиков.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROVIDER_ORDINAL  <br/> |
|Идентификатор:  <br/> |0x300D  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Общие MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство вычисляется с помощью MAPI.
  
Получите таблицу поставщика, вызывая метод [IMsgServiceAdmin::GetProviderTable.](imsgserviceadmin-getprovidertable.md) Отсортировать таблицу поставщика по этому свойству, чтобы отобразить порядок транспорта. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

