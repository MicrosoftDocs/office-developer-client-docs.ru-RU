---
title: Каноническое свойство PidTagProviderDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDisplay
api_type:
- COM
ms.assetid: 62e96db8-4c3e-4f73-b695-99eb4b2396fd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 58db944720817491420f2bcb1774e51e3842b4a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286469"
---
# <a name="pidtagproviderdisplay-canonical-property"></a>Каноническое свойство PidTagProviderDisplay

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит отображаемое имя, определенное поставщиком услуг.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ПРОВИДЕР_ДИСПЛАЙ, ПР_ПРОВИДЕР_ДИСПЛАЙ_А, ПР_ПРОВИДЕР_ДИСПЛАЙ_В  <br/> |
|Идентификатор:  <br/> |0x3006  <br/> |
|Тип данных:  <br/> |PT_STRING8, ПТ_УНИКОДЕ  <br/> |
|Область:  <br/> |Общие протоколы MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства и **пр_провидер_длл_наме** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) определяются только в разделах профиля, относящихся к поставщикам услуг. Они должны присутствовать в MAPISVC. INF.
  
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

