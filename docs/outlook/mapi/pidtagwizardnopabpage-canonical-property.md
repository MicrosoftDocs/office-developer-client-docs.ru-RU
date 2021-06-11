---
title: Каноническое свойство PidTagWizardNoPabPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagWizardNoPabPage
api_type:
- COM
ms.assetid: 9cec22cd-798d-41f6-9ebd-c7354f2162c2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fc971be76dbaa83176f207411f9f125ffee386cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424464"
---
# <a name="pidtagwizardnopabpage-canonical-property"></a>Каноническое свойство PidTagWizardNoPabPage

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Это свойство содержит TRUE, если мастер профиля должен подавить страницу личной адресной книги (PAB).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_WIZARD_NO_PAB_PAGE  <br/> |
|Идентификатор:  <br/> |0x6701  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Exchange Администрирование  <br/> |
   
## <a name="remarks"></a>Примечания

Поставщики услуг могут установить это свойство при вызове функции на основе прототипа функции [LAUNCHWIZARDENTRY.](launchwizardentry.md) Это свойство сообщает мастеру профиля, что поставщик не хочет, чтобы страница PAB отображалась во время диалогов пользователя. 
  
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

