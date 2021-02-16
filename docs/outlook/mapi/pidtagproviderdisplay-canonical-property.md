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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421594"
---
# <a name="pidtagproviderdisplay-canonical-property"></a>Каноническое свойство PidTagProviderDisplay

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит определенное поставщиком отображаемого имени поставщика услуг.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W  <br/> |
|Идентификатор:  <br/> |0x3006  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Общие mapI  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства **и** PR_PROVIDER_DLL_NAME ([PidTagProviderDllName)](pidtagproviderdllname-canonical-property.md)определяются только в разделах профиля, принадлежащих поставщикам услуг. Они должны присутствовать в MAPISVC.INF.
  
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

