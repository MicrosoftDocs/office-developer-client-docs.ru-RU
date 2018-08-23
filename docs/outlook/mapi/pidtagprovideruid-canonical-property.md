---
title: Каноническое свойство PidTagProviderUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderUid
api_type:
- COM
ms.assetid: 993f5bca-58a6-455d-8a25-6e08b441ad31
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cca22b466b1e0d2da9ca9cc009586df08316270c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581057"
---
# <a name="pidtagprovideruid-canonical-property"></a>Каноническое свойство PidTagProviderUid

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит структуру **MAPIUID** поставщика услуг, который обрабатывает сообщение. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROVIDER_UID  <br/> |
|Идентификатор:  <br/> |0x300C  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Распространенные MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство вычисляется по всем поставщикам услуг. Структура [MAPIUID](mapiuid.md) связанных с и обычно жестко поставщиком, в нем. Обычно используется приложением клиента и интересует только адресной книги контейнеры конкретной службы. 
  
Это свойство отображается только в качестве записи в столбце в таблице поставщика.
  
## <a name="related-resources"></a>Связанные ресурсы

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

