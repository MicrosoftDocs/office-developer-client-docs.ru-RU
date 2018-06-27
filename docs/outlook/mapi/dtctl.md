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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 68c621f5f73073ed127767cc1db189769dab227d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808389"
---
# <a name="dtctl"></a>DTCTL

**Применимо к**: Outlook 
  
Описывает элемент управления, который будет использоваться в диалоговое окно, построенная на основе таблицы отображения. 
  
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

## <a name="members"></a>Элементы

**ulCtlType**
  
> Тип элемента управления, который включен в **список доверия сертификатов** член и соответствует свойству **PR_CONTROL_TYPE** ([PidTagControlType](pidtagcontroltype-canonical-property.md)) элемента управления. Ниже приведены возможные значения:
    
DTCT_LABEL 
  
> Элемент управления Label.
    
DTCT_EDIT 
  
> Изменение элемента управления.
    
DTCT_LBX 
  
> Окно списка.
    
DTCT_COMBOBOX 
  
> Элемент управления ComboBox.
    
DTCT_DDLBX 
  
> Элемент управления раскрывающегося списка.
    
DTCT_CHECKBOX 
  
> Элемент управления "флажок".
    
DTCT_GROUPBOX 
  
> Элемент управления поля группы.
    
DTCT_BUTTON 
  
> Элемент управления Button.
    
DTCT_PAGE 
  
> Элемент управления страницы с вкладками.
    
DTCT_RADIOBUTTON 
  
> Управления "переключатель".
    
DTCT_MVLISTBOX 
  
> Элемент управления, поддерживающий несколько значений списка.
    
DTCT_MVDDLBX 
  
> Элемент управления, поддерживающий несколько значений раскрывающегося списка.
    
**ulCtlFlags**
  
> Битовая маска флаги с описанием функций элемента управления и соответствует свойству **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) элемента управления. Эти флаги можно задать для флажки, поля со списками, списков и изменить только элементы управления. Ниже приведены возможные значения:
    
DT_ACCEPT_DBCS 
  
> Допускается формата ANSI или DBCS. Этот флаг является допустимым редактирования только для элементов управления.
    
DT_EDITABLE 
  
> Пользователь может изменить текст в элементе управления. 
    
DT_MULTILINE 
  
> Элемент управления может содержать несколько строк текста. Этот флаг является допустимым редактирования только для элементов управления.
    
DT_PASSWORD_EDIT 
  
> Элемент управления содержит пароль; Таким образом содержимое элемента управления не должен отображаться для пользователя. Этот флаг является допустимым редактирования только для элементов управления.
    
DT_REQUIRED 
  
> Элемент управления полем диалоговое окно является обязательным. Этот флаг является допустимым только для элементов управления редактирования и поля со списком.
    
DT_SET_IMMEDIATE 
  
> Включение Интерпретация выходных данных, значение при изменении в элементе управления. Это позволяет отношения зависимости соединения между двумя элементами управления. 
    
**lpbNotif**
  
> Указатель на структуру, которая состоит из структуру [идентификатор GUID](guid.md) для представления поставщика услуг и идентификатор для элемента управления. Члены **lpbNotif** и **cbNotif** соответствуют свойства **PR_CONTROL_ID** ([PidTagControlId](pidtagcontrolid-canonical-property.md)) и использовать для уведомления пользовательского интерфейса, когда элемент управления имеет должны обновляться.
    
**cbNotif**
  
> Число байт в структуре, на который указывает член **lpbNotif** . 
    
**lpszFilter**
  
> Указатель на строку символов, которая описывается, какие символы можно ввести в элемент управления поля со списком или изменить. Для других типов элементов управления **lpszFilter** участник может быть NULL. Для редактирования и поля со списком элементов управления следует регулярное выражение, которое применяется к один символ за раз. Тот же фильтр будет применяться ко всем символов в элементе управления. Формат строки фильтра выглядит следующим образом: 
    
|**Символ**|**Описание**|
|:-----|:-----|
| `*` <br/> | Допускается любой символ (например, `"*"`).  <br/> |
| `[ ]` <br/> |Определяет набор символов (например, `"[0123456789]"`.)  <br/> |
| `-` <br/> |Указывает диапазон символов (например, `"[a-z]"`).  <br/> |
| `~` <br/> |Указывает, что эти символы не разрешены (например, `"[~0-9]")`. <br/>|   
| `\` <br/> |Используется для любой из предыдущих символы кавычек (например, `"[\-\\\[\]]"` означает, что-, \, [, и] могут знаков).  <br/> |
   
**ulItemID**
  
> Значение, идентифицирующее элемент управления в ресурс диалогового окна. Для элементов управления страниц с вкладками типа DTCT_PAGE **ulItemID** член при необходимости используется для загрузки имя компонента страницы из строки ресурсов. Положение и сведения о метке считываются из ресурс диалогового окна. 
    
**список доверия сертификатов**
  
> Структура, которая содержит данные для элемента управления и соответствует свойству **PR_CONTROL_STRUCTURE** ([PidTagControlStructure](pidtagcontrolstructure-canonical-property.md)) элемента управления. Каждый тип элемента управления имеет другую структуру.
    
## <a name="remarks"></a>Замечания

Структура **DTCTL** описывает один элемент управления любого типа. Большая часть его члены используются для задания свойств элемента управления. 
  
Член **список доверия сертификатов** — это объединение структуры, относящиеся к определенным типом элемента управления. Если структура **DTCTL** — это описания элемента управления, например, член **список доверия сертификатов** будет наведите указатель мыши [DTBLEDIT](dtbledit.md) структуры. Эта структура соответствует свойству **PR_CONTROL_STRUCTURE** элемента управления. Объединение имеет его, входящей в первой переменной типа LPVOID, чтобы разрешить инициализацию времени компиляции **DTCTL** структуры. 
  
Несмотря на то, что функция [BuildDisplayTable](builddisplaytable.md) использует структуру **DTCTL** для построения в таблице отображения из элемента управления ресурсами, структура **DTCTL** никогда не отображается в самой таблицы отображения. Эта структура только что предоставляет сведения о **BuildDisplayTable**.
  
Элемент **ulCtlFlags** четыре флаги DT_ACCEPT_DBCS, DT_EDITABLE, влияющие на DT_MULTILINE_and DT_PASSWORD_EDIT изменить только элементы управления. Два других пользователей DT_REQUIRED и DT_SET_IMMEDIATE влияет на любой редактируемом элементе управления. 
  
Элементы управления, доступные для диалогового окна, метки, текстовое поле, принять во внимание рукописного ввода текстовое поле, список, раскрывающегося списка, поля со списком, флажок, поле группы, кнопка, переключатель и страницы с вкладками.
  
Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md). Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.
  
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
