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

**Относится к**: Outlook 2013 | Outlook 2016 
  
Описывается управление, которое будет использоваться в диалоговом окне, построенного из таблицы отображения. 
  
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
  
> Тип управления, включенный в член **ctl** и соответствующий  свойству PR_CONTROL_TYPE [(PidTagControlType).](pidtagcontroltype-canonical-property.md) Возможные значения:
    
DTCT_LABEL 
  
> Управление меткой.
    
DTCT_EDIT 
  
> Изменение управления.
    
DTCT_LBX 
  
> Управление списком.
    
DTCT_COMBOBOX 
  
> Управление полем со combo.
    
DTCT_DDLBX 
  
> Drop-down list control.
    
DTCT_CHECKBOX 
  
> Контрольный окне.
    
DTCT_GROUPBOX 
  
> Групповое поле.
    
DTCT_BUTTON 
  
> Кнопка управления.
    
DTCT_PAGE 
  
> Tabbed page control.
    
DTCT_RADIOBUTTON 
  
> Управление кнопками.
    
DTCT_MVLISTBOX 
  
> Много значений для управления списком.
    
DTCT_MVDDLBX 
  
> Много значений для выпадаемого списка.
    
**ulCtlFlags**
  
> Битовая маской флагов, которая описывает функции управления и соответствует свойству **PR_CONTROL_FLAGS** ([PidTagControlFlags).](pidtagcontrolflags-canonical-property.md) Эти флаги можно установить только для флажков, полей со списком, списков и элементов управления редактированием. Возможные значения:
    
DT_ACCEPT_DBCS 
  
> Принимается формат ANSI или DBCS. Этот флаг действителен только для элементов управления редактированием.
    
DT_EDITABLE 
  
> Пользователь может изменить текст в окнах. 
    
DT_MULTILINE 
  
> Этот контроль может содержать несколько текстовых строк. Этот флаг действителен только для элементов управления редактированием.
    
DT_PASSWORD_EDIT 
  
> Этот контроль содержит пароль; Следовательно, содержимое этого управления не должно отображаться для пользователя. Этот флаг действителен только для элементов управления редактированием.
    
DT_REQUIRED 
  
> Необходимое поле управления диалоговое окно. Этот флаг действителен только для элементов управления "Изменить" и "Поле со combo".
    
DT_SET_IMMEDIATE 
  
> Включает немедленные выходные данные значения при изменении в контроле. Это позволяет установить отношение зависимостей между двумя средствами управления. 
    
**lpbNotif**
  
> Указатель на структуру, состоящую из [структуры GUID,](guid.md) которая представляет поставщика услуг и идентификатор для управления. Члены **lpbNotif** и **cbNotif** соответствуют свойству **PR_CONTROL_ID** [(PidTagControlId)](pidtagcontrolid-canonical-property.md)и используются для уведомления пользовательского интерфейса о том, что необходимо обновить этот объект.
    
**cbNotif**
  
> Количествобайтов в структуре, на который указывает **член lpbNotif.** 
    
**lpszFilter**
  
> Указатель на строку символов, описываемую, какие символы можно вказать в поле редактирования или со полем со combo. Для других типов элементов управления элемент **lpszFilter** может иметь NULL. Для элементов управления полем редактирования и сомеда это должно быть регулярное выражение, которое применяется к отдельному символу за раз. Один и тот же фильтр применяется к всем символам в этом контроле. Формат строки фильтра: 
    
|**Символ**|**Описание**|
|:-----|:-----|
| `*` <br/> | Любой символ разрешен (например, `"*"` ).  <br/> |
| `[ ]` <br/> |Определяет набор символов (например, `"[0123456789]"` .)  <br/> |
| `-` <br/> |Указывает диапазон символов (например, `"[a-z]"` ).  <br/> |
| `~` <br/> |Указывает, что эти символы не разрешены (например, `"[~0-9]")` . <br/>|   
| `\` <br/> |Используется для кавычка любых из предыдущих символов (например, `"[\-\\\[\]]"` знаки -, \, [и ] разрешены).  <br/> |
   
**ulItemID**
  
> Значение, определя которое определяет управление в ресурсе диалоговых окно. Для страниц вкладок элементы управления типа DTCT_PAGE **элемент ulItemID** при желании используется для загрузки имени компонента страницы из строки ресурса. Сведения о положении и метке считыются из ресурса диалоговых окно. 
    
**ctl**
  
> Структура, которая содержит данные для управления и соответствует свойству **PR_CONTROL_STRUCTURE** [(PidTagControlStructure).](pidtagcontrolstructure-canonical-property.md) Каждый тип управления имеет разную структуру.
    
## <a name="remarks"></a>Примечания

Структура **DTCTL** описывает один из типов. Большинство его членов используются для того, чтобы установить свойства в этом объекте управления. 
  
Член **ctl** — это объединение структур, которые связаны с определенным типом управления. Если структура **DTCTL** описывает, например, изменение, член **ctl** будет указать на [структуру DTBLEDIT.](dtbledit.md) Эта структура соответствует свойству PR_CONTROL_STRUCTURE **управления.** В качестве первого члена объединения имеется переменная типа LPVOID, позволяющая инициализации времени компиляции **структуры DTCTL.** 
  
Хотя функция [BuildDisplayTable](builddisplaytable.md) использует структуру **DTCTL** для построения таблицы отображения из ресурсов управления, **структура DTCTL** никогда не отображается в самой таблице отображения. Эта структура просто сообщает сведения **в BuildDisplayTable.**
  
В **элементе ulCtlFlags** четыре флага DT_ACCEPT_DBCS, DT_EDITABLE и DT_MULTILINE_and DT_PASSWORD_EDIT только на элементы управления редактированием. Два других DT_REQUIRED и DT_SET_IMMEDIATE любого редактируемого управления. 
  
Элементы управления, доступные для диалогового окна: метка, текстовое поле, список, выпадаичный список, поле со списком, поле со списком, поле группы, кнопка, кнопка, кнопка и страница вкладок.
  
Обзор таблиц отображения см. в [таблице отображения.](display-tables.md) Сведения о реализации таблицы отображения см. в таблице ["Реализация таблицы отображения".](display-table-implementation.md)
  
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

