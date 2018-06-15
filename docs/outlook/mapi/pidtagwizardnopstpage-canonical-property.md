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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: b94e1f2d66f89d680cc738968342de0fbcee5cda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19812047"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a>Каноническое свойство PidTagWizardNoPstPage

  
  
**Применимо к**: Outlook 
  
Это свойство содержит значение TRUE, если мастер профиля для отмены вывода страницы личное сообщение store (PST).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_WIZARD_NO_PST_PAGE  <br/> |
|Идентификатор:  <br/> |0x6700  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Области:  <br/> |Администрирования Exchange  <br/> |
   
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
  
[Каноническое свойство имена сопоставляемых именам MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI имена каноническое свойств](mapping-mapi-names-to-canonical-property-names.md)

