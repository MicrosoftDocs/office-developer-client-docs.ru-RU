---
title: Каноническое свойство PidTagControlFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlFlags
api_type:
- HeaderDef
ms.assetid: b97a9e72-fbb7-49ab-a19d-5e9bd1b8a80d
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: f6947efe1aa6866efb7a5a3d96262d021c68013f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811015"
---
# <a name="pidtagcontrolflags-canonical-property"></a>Каноническое свойство PidTagControlFlags

  
  
**Применимо к**: Outlook 
  
Содержит битовую маску флагов регулирующих поведение элемента управления, используемые в диалоговое окно, построенная на основе таблицы отображения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTROL_FLAGS  <br/> |
|Идентификатор:  <br/> |0x3F00  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Области:  <br/> |Таблица отображения MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Для этого свойства может быть установлено одно или несколько из следующих флагов:
  
DT_ACCEPT_DBCS 
  
> Элемент управления может иметь значение двухбайтовых знаков (DBCS) символов в нем. Этот флаг используется с элементами управления Правка. Он обеспечивает наборы символов несколько байтов.
    
DT_EDITABLE 
  
> Элемент управления можно редактировать; можно изменить значение, связанное с элементом управления. Если этот флаг не задан, элемент управления доступен только для чтения. Это значение игнорируется на метку, группа, стандартной кнопки, многозначных раскрывающегося списка и элемента управления списка полей.
    
DT_MULTILINE 
  
> Элемент управления для редактирования может содержать несколько строк. Это означает, что возвращаемый символ можно ввести в элементе управления. Этот флаг является допустимым редактирования только для элементов управления.
    
DT_PASSWORD_EDIT 
  
> Применяется для редактирования элементов управления. Элемент управления для редактирования рассматривается как пароль. Значение отображается с помощью звездочки вместо вывода вводимых символов.
    
DT_REQUIRED 
  
> Если элемент управления позволяет изменения (DT_EDITABLE), он должен иметь значение до вызова [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . 
    
DT_SET_IMMEDIATE 
  
> Позволяет интерпретации параметр значение; как только изменяет значение в элементе управления MAPI вызывает метод **SetProps** для свойства, связанного с этим элементом управления. Если этот флаг не задан, значения устанавливаются при диалоговое окно закрывается. 
    
DT_SET_SELECTION 
  
> При выбора в поле списка в столбце индекса из этого списка устанавливается как свойство. Всегда использовать совместно с DT_SET_IMMEDIATE.
    
Это свойство хранится в член ulCtlFlags структуры [DTCTL](dtctl.md) элемента управления. Большая часть флаги управления применяются ко всем элементам управления, которые позволяют пользователям вводить данные; несколько применяются только к элемент управления для редактирования. Элементы управления, которые не позволяют пользователям вводить данные, такие как кнопки или метки, задайте 0 для их флаги элемента управления. 
  
Многие из значений флаг очевидны. Например когда DT_REQUIRED для элемента управления, он должен содержать значение перед диалоговое окно может быть закрыт. Поставщик услуг можно указать значение его реализации **IMAPIProp** либо пользователь может ввести один. DT_EDITABLE указывает, что значение для элемента управления может быть изменено. DT_MULTILINE позволяет значение для ввода нескольких строк. 
  
Некоторые флаги управления не столь очевидно в их значения. Когда элемент управления устанавливает флаг DT_SET_IMMEDIATE, все изменения, необходимо выполнить его значение влияет на сразу же пользователь перемещается на новый элемент управления. MAPI делает один вызов метода [IMAPIProp::SetProps](imapiprop-setprops.md) интерфейса свойств для свойства элемента управления. Это отличается от поведения по умолчанию, являющийся откладывать необходимости изменения значения элемента управления вступают в силу только после пользователь выбирает кнопку **ОК** или закрывает диалоговое окно. Флаг DT_SET_IMMEDIATE часто используется в сочетании с отображения таблицы уведомлений. 
  
В следующей таблице перечислены типы элементов управления и всех флаг значения, которые можно задать для каждого типа.
  
|**Control**|**Допустимые значения для этого свойства**|
|:-----|:-----|
|Кнопка  <br/> |Должно быть равно нулю  <br/> |
|Флажок  <br/> |DT_EDITABLE DT_SET_IMMEDIATE  <br/> |
|Поле со списком  <br/> |DT_EDITABLE, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Поле раскрывающегося списка  <br/> |DT_EDITABLE DT_SET_IMMEDIATE  <br/> |
|Изменить  <br/> |DT_ACCEPT_DBCS, DT_MULTILINE, DT_EDITABLE, DT_PASSWORD_EDIT, DT_REQUIRED, DT_SET_IMMEDIATE  <br/> |
|Группа  <br/> |Должно быть равно нулю  <br/> |
|Метка  <br/> |Должно быть равно нулю  <br/> |
|Список  <br/> |Должно быть равно нулю  <br/> |
|Для нескольких значений раскрывающегося списка  <br/> |Должно быть равно нулю  <br/> |
|Поле список с несколькими значениями  <br/> |Должно быть равно нулю  <br/> |
|Страницы с вкладками  <br/> |Должно быть равно нулю  <br/> |
|Переключатель  <br/> |Должно быть равно нулю  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Каноническое свойство имена сопоставляемых именам MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI имена каноническое свойств](mapping-mapi-names-to-canonical-property-names.md)
