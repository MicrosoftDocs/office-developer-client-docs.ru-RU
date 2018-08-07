---
title: Каноническое свойство PidTagControlType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlType
api_type:
- HeaderDef
ms.assetid: 7728fa2f-4a59-4e86-90f1-4384824598aa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fba82fef7c5330f538521d8d5fbdbcecc061ee27
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811017"
---
# <a name="pidtagcontroltype-canonical-property"></a>Каноническое свойство PidTagControlType

  
  
**Относится к**: Outlook 
  
Содержит значение, указывающее тип элемента управления для элемента управления, используемый в диалоговом окне. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTROL_TYPE  <br/> |
|Идентификатор:  <br/> |0x3F02  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Таблица отображения MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство может иметь только один из следующих значений:
  
DTCT_BUTTON 
  
> Элемент управления кнопки диалогового окна.
    
DTCT_CHECKBOX 
  
> Флажок диалогового окна.
    
DTCT_COMBOBOX 
  
> Диалоговое окно со списком.
    
DTCT_DDLBX 
  
> Диалоговое окно раскрывающегося списка.
    
DTCT_EDIT 
  
> Диалоговое окно "текст" Правка.
    
DTCT_GROUPBOX 
  
> Диалоговое окно "Группа".
    
DTCT_LABEL 
  
> Диалоговое окно подпись.
    
DTCT_LBX 
  
> Диалоговое окно списка.
    
DTCT_LISTBOX 
  
> Диалоговое окно списка.
    
DTCT_MVDDLBX 
  
> Многозначные список заполняется с несколькими значениями свойство типа string.
    
DTCT_PAGE 
  
> Диалоговое окно страницы с вкладками.
    
DTCT_RADIOBUTTON 
  
> Переключатель диалогового окна.
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

