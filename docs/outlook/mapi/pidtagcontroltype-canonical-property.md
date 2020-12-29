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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение, указывающее тип управления для используемого в диалоговом окне. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTROL_TYPE  <br/> |
|Идентификатор:  <br/> |0x3F02  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Таблица отображения MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство может иметь одно из следующих значений:
    
DTCT_LABEL (0x000000000)
  
> Метка диалогового окна.
   
DTCT_EDIT (0x00000001)
  
> Текстовое поле для редактирования диалогового окна.

DTCT_LBX (0x00000002)
  
> Диалоговое окно со списком.
    
DTCT_COMBOBOX (0x00000003)
  
> Диалоговое окно со combo.

DTCT_DDLBX (0x00000004)
  
> Диалоговое окно в выпадаемом списке.

DTCT_CHECKBOX (0x00000005)
  
> Диалоговое окно.

DTCT_GROUPBOX (0x00000006)
  
> Диалоговое окно группы.
  
DTCT_BUTTON (0x00000007)
  
> Диалоговое окно с кнопкой управления.
    
DTCT_PAGE (0x00000008)
  
> Страница вкладки диалоговое окно.
    
DTCT_RADIOBUTTON (0x00000009)
  
> Радиоприемник диалогового окна.
    
DTCT_MVLISTBOX (0x0000000B)
  
> Многооценное поле списка, заполненное многоценным свойством строки типа.
    
DTCT_MVDDLBX (0x00000000C)
  
> Многоценное поле в списке, заполненное многоценным свойством строки типа.
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

