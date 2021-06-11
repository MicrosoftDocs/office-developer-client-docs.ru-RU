---
title: DTCTL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTCTL
api_type:
- COM
ms.assetid: 6d1589e9-b171-427a-9a3e-b4154ee8ceb6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2a2ca1fba5dceb45b41c2f25a96e163f02c41440
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421503"
---
# <a name="dtctl"></a>DTCTL

**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает управление, которое будет использоваться в диалоговом окне, построенной из таблицы отображения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG ulCtlType;
  ULONG ulCtlFlags;
  LPBYTE lpbNotif;
  ULONG cbNotif;
  LPSTR lpszFilter;
  ULONG ulItemID;
  union
  {
    LPVOID lpv;
    LPDTBLLABEL lplabel;
    LPDTBLEDIT lpedit;
    LPDTBLLBX lplbx;
    LPDTBLCOMBOBOX lpcombobox;
    LPDTBLDDLBX lpddlbx;
    LPDTBLCHECKBOX lpcheckbox;
    LPDTBLGROUPBOX lpgroupbox;
    LPDTBLBUTTON lpbutton;
    LPDTBLRADIOBUTTON lpradiobutton;
    LPDTBLMVLISTBOX lpmvlbx;
    LPDTBLMVDDLBX lpmvddlbx;
    LPDTBLPAGE lppage;
  } ctl;
} DTCTL, FAR *LPDTCTL;

```

## <a name="members"></a>"Участники"

**ulCtlType**
  
> Тип управления, который входит в состав **ctl** и соответствует свойству **PR_CONTROL_TYPE** [(PidTagControlType).](pidtagcontroltype-canonical-property.md) Возможные значения:
    
DTCT_LABEL 
  
> Управление меткой.
    
DTCT_EDIT 
  
> Изменение управления.
    
DTCT_LBX 
  
> Управление полем списка.
    
DTCT_COMBOBOX 
  
> Управление полем combo.
    
DTCT_DDLBX 
  
> Drop-down list control.
    
DTCT_CHECKBOX 
  
> Управление полем проверки.
    
DTCT_GROUPBOX 
  
> Управление групповой коробкой.
    
DTCT_BUTTON 
  
> Управление кнопками.
    
DTCT_PAGE 
  
> Управление страницей с вкладками.
    
DTCT_RADIOBUTTON 
  
> Управление кнопкой радио.
    
DTCT_MVLISTBOX 
  
> Управление списком с несколькими значениями.
    
DTCT_MVDDLBX 
  
> Управление списком с несколькими значениями.
    
**ulCtlFlags**
  
> Битмаски флагов, описывая функции управления и соответствующие свойству PR_CONTROL_FLAGS[(PidTagControlFlags).](pidtagcontrolflags-canonical-property.md)  Эти флаги можно установить только для флажков, комбо-полей, списков и элементов управления. Возможные значения:
    
DT_ACCEPT_DBCS 
  
> Принимается формат ANSI или DBCS. Этот флаг действителен только для редактирования элементов управления.
    
DT_EDITABLE 
  
> Пользователь может изменить текст в области управления. 
    
DT_MULTILINE 
  
> Управление может содержать несколько строк текста. Этот флаг действителен только для редактирования элементов управления.
    
DT_PASSWORD_EDIT 
  
> Управление содержит пароль; поэтому содержимое управления не должно отображаться пользователю. Этот флаг действителен только для редактирования элементов управления.
    
DT_REQUIRED 
  
> Требуется управление диалоговое окно. Этот флаг действителен только для элементов управления полем редактирования и комбо.
    
DT_SET_IMMEDIATE 
  
> Включает немедленный выход значения при изменении управления. Это позволяет установить связь зависимости между двумя средствами управления. 
    
**lpbNotif**
  
> Указатель на структуру, состоящую из [структуры GUID,](guid.md) для представления поставщика услуг и идентификатора для управления. Члены **lpbNotif** и **cbNotif** соответствуют свойству PR_CONTROL_ID [(PidTagControlId)](pidtagcontrolid-canonical-property.md)и используются для уведомления пользовательского интерфейса при обновлении управления. 
    
**cbNotif**
  
> Количество bytes в структуре, на который указывает член **lpbNotif.** 
    
**lpszFilter**
  
> Указатель на строку символов, которая описывает, какие символы можно вправить или комбо-поле управления. Для других типов элементов управления **член lpszFilter** может быть NULL. Для элементов управления полем редактирования и комбо оно должно быть регулярным выражением, которое применяется к одному символу одновременно. Один и тот же фильтр применяется к всем символам управления. Формат строки фильтра следующим образом: 
    
|**Символ**|**Описание**|
|:-----|:-----|
| `*` <br/> | Разрешен любой символ (например, `"*"` ).  <br/> |
| `[ ]` <br/> |Определяет набор символов (например, `"[0123456789]"` .)  <br/> |
| `-` <br/> |Указывает диапазон символов (например, `"[a-z]"` ).  <br/> |
| `~` <br/> |Указывает, что эти символы не разрешены (например, `"[~0-9]")` . <br/>|   
| `\` <br/> |Используется для цитаты любого из предыдущих символов (например, разрешены знаки `"[\-\\\[\]]"` -, \, [и ]).  <br/> |
   
**ulItemID**
  
> Значение, определяее управление в диалоговом окне ресурса. Для элементов управления страницами типа DTCT_PAGE **элемент ulItemID** необязательно используется для загрузки имени компонента для страницы из строки ресурса. Сведения о позиции и метке считыются из ресурса диалоговое окно. 
    
**ctl**
  
> Структура, которая содержит данные для управления и соответствует свойству **PR_CONTROL_STRUCTURE** [(PidTagControlStructure).](pidtagcontrolstructure-canonical-property.md) Каждый тип управления имеет другую структуру.
    
## <a name="remarks"></a>Примечания

Структура **DTCTL** описывает один контроль любого типа. Большинство его членов используются для набора свойств на пульте управления. 
  
Член **ctl** — это объединение структур, которые относятся к определенному типу управления. Если в **структуре DTCTL** описывается управление изменением, например, участник **ctl** будет указать на [структуру DTBLEDIT.](dtbledit.md) Эта структура соответствует свойству PR_CONTROL_STRUCTURE **управления.** Профсоюз имеет в качестве первого члена переменную типа LPVOID, позволяющую инициализации времени компилировать **структуру DTCTL.** 
  
Хотя функция [BuildDisplayTable](builddisplaytable.md) использует структуру **DTCTL** для построения таблицы отображения из ресурсов управления, структура **DTCTL** никогда не отображается в самой таблице отображения. Эта структура просто поставляет сведения **в BuildDisplayTable**.
  
В **члене ulCtlFlags** четыре флага DT_ACCEPT_DBCS, DT_EDITABLE, DT_MULTILINE_and DT_PASSWORD_EDIT влияют только на элементы управления редактированием. Два других DT_REQUIRED и DT_SET_IMMEDIATE могут повлиять на любой редактурируемый контроль. 
  
Элементы управления, доступные для диалогового окна: метка, текстовое поле, список, комбо-поле, контрольное окно, групповое поле, кнопка, кнопка, кнопка радио и страница вкладки.
  
Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md) Сведения о реализации таблицы отображения см. в таблице [Implementing a Display Table.](display-table-implementation.md)
  
## <a name="see-also"></a>См. также

- [BuildDisplayTable](builddisplaytable.md)
- [DTBLBUTTON](dtblbutton.md)
- [DTBLCHECKBOX](dtblcheckbox.md)
- [DTBLCOMBOBOX](dtblcombobox.md)
- [DTBLDDLBX](dtblddlbx.md)
- [DTBLEDIT](dtbledit.md)
- [DTBLGROUPBOX](dtblgroupbox.md)
- [DTBLLABEL](dtbllabel.md)
- [DTBLLBX](dtbllbx.md)
- [DTBLMVDDLBOX](dtblmvddlbox.md)
- [DTBLMVLISTBOX](dtblmvlistbox.md)
- [DTBLPAGE](dtblpage.md)
- [DTBLRADIOBUTTON](dtblradiobutton.md)
- [Структуры MAPI](mapi-structures.md)

