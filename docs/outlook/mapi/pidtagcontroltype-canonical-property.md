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
ms.openlocfilehash: 7bdb02f72ba14a36c8a4c218cd5f0631e7145e6a
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734205"
---
# <a name="pidtagcontroltype-canonical-property"></a>Каноническое свойство PidTagControlType

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит значение, указывающее тип управления для управления, используемого в диалоговом окне. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTROL_TYPE  <br/> |
|Идентификатор:  <br/> |0x3F02  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Таблица отображения MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство может иметь одно из следующих значений:
    
DTCT_LABEL (0x00000000)
  
> Метка диалогов.
   
DTCT_EDIT (0x00000001)
  
> Диалоговое окно для редактирования текста.

DTCT_LBX (0x00000002)
  
> Диалоговое поле списка.
    
DTCT_COMBOBOX (0x00000003)
  
> Диалоговое комбо поле.

DTCT_DDLBX (0x00000004)
  
> Диалоговое окно списка.

DTCT_CHECKBOX (0x00000005)
  
> Диалоговое окно.

DTCT_GROUPBOX (0x00000006)
  
> Диалоговое групповое окно.
  
DTCT_BUTTON (0x00000007)
  
> Управление кнопкой диалогов.
    
DTCT_PAGE (0x00000008)
  
> Страница на вкладке диалоговое окно.
    
DTCT_RADIOBUTTON (0x00000009)
  
> Кнопка радио диалогов.
    
DTCT_MVLISTBOX (0x0000000B)
  
> Многоценное поле списка, заполненное многоценным свойством строки типа.
    
DTCT_MVDDLBX (0x0000000C)
  
> Многооценное поле списка,заполненное многоценным свойством строки типа.
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

