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
ms.openlocfilehash: e816af2ce60b4c06ae14f720cf7c36d58468d09d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422889"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a>Каноническое свойство PidTagWizardNoPstPage

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Это свойство содержит TRUE, если мастер профиля должен подавить страницу магазина личных сообщений (PST).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_WIZARD_NO_PST_PAGE  <br/> |
|Идентификатор:  <br/> |0x6700  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Exchange Администрирование  <br/> |
   
## <a name="remarks"></a>Примечания

Поставщики услуг могут установить это свойство при вызове функции на основе прототипа функции [LAUNCHWIZARDENTRY.](launchwizardentry.md) Это свойство сообщает мастеру профилей, что поставщик не хочет, чтобы страница PST отображалась во время диалогов пользователя. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве связанных свойств.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

