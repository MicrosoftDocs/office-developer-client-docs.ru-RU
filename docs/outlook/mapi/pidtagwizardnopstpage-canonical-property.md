---
title: Каноническое свойство PidTagWizardNoPstPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagWizardNoPstPage
api_type:
- COM
ms.assetid: 1ac09578-892b-4c72-92f6-c2419ac2efe8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ae1f5b62c59c2e9a1c02c1a2fc0ee91ef1e19387
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562983"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a>Каноническое свойство PidTagWizardNoPstPage

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Это свойство содержит значение TRUE, если мастер профиля для отмены вывода страницы личное сообщение store (PST).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_WIZARD_NO_PST_PAGE  <br/> |
|Идентификатор:  <br/> |0x6700  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Администрирования Exchange  <br/> |
   
## <a name="remarks"></a>Замечания

При вызове функции, основанной на прототип функции [LAUNCHWIZARDENTRY](launchwizardentry.md) этому свойству можно задать поставщиков услуг. Это свойство сообщает мастер профилей, что поставщик не нужно странице PST-файлов будет отображаться во время диалоговое окно user. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

