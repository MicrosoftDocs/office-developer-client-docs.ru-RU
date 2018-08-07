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
ms.openlocfilehash: 7a42a3b50cfa5630ac66cb03caac06dd7cb00e6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811589"
---
# <a name="pidtagprovideruid-canonical-property"></a>Каноническое свойство PidTagProviderUid

  
  
**Относится к**: Outlook 
  
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

