---
title: Каноническое свойство PidTagResourceType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceType
api_type:
- COM
ms.assetid: 48b634d7-deea-422b-8944-a8d929d83838
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5d494577721feba01dd9cb93f344308251a8ed33
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811756"
---
# <a name="pidtagresourcetype-canonical-property"></a>Каноническое свойство PidTagResourceType

  
  
**Относится к**: Outlook 
  
Содержит значение, которое указывает тип поставщика услуг.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RESOURCE_TYPE  <br/> |
|Идентификатор:  <br/> |0x3E03  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство может иметь только один из следующих значений:
  
MAPI_AB 
  
> Адресная книга
    
MAPI_AB_PROVIDER 
  
> Поставщик адресной книги
    
MAPI_HOOK_PROVIDER 
  
> Поставщик обработчик очереди
    
MAPI_PROFILE_PROVIDER 
  
> Поставщик профиля
    
MAPI_SPOOLER 
  
> Очереди сообщений
    
MAPI_STORE_PROVIDER 
  
> Поставщик хранилища сообщений
    
MAPI_SUBSYSTEM 
  
> Внутренняя Подсистема MAPI
    
MAPI_TRANSPORT_PROVIDER 
  
> Поставщик транспорта
    
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

