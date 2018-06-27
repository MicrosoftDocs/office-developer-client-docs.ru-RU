---
title: DTBLEDIT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLEDIT
api_type:
- COM
ms.assetid: ec3566a0-75ad-466d-a61e-f7d61ccb946d
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: d0418ac2ec5d01d58c63e4ad48a1066cc386e946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808357"
---
# <a name="dtbledit"></a>DTBLEDIT

  
  
**Применимо к**: Outlook 
  
Описывает элемент управления редактирования, которая будет использоваться в диалоговое окно, построенная на основе таблицы отображения.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макрос:  <br/> |[SizedDtblEdit](sizeddtbledit.md) <br/> |
   
```cpp
typedef struct _DTBLEDIT
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPropTag;
} DTBLEDIT, FAR *LPDTBLEDIT;

```

## <a name="members"></a>Элементы

 **ulbLpszCharsAllowed**
  
> Смещение от начала структуры **DTBLEDIT** в фильтр символ строка, описывающая ограничения, если оно нужно символов, которые можно ввести в элемент управления. Фильтр не обрабатывается как регулярное выражение и тот же фильтр применяется к каждый символ, введенный. Формат фильтр выглядит следующим образом: 
    
|**Символ**|**Описание**|
|:-----|:-----|
| `*` <br/> |Допускается любой символ (например, `"*"`).  <br/> |
| `[ ]` <br/> |Определяет набор символов (например, `"[0123456789]".`)  <br/> |
| `-` <br/> |Указывает диапазон символов (например, `"[a-z]"`).  <br/> |
| `~` <br/> |Указывает, что эти символы не разрешены (например, `"[~0-9]"`).  <br/> |
| `\` <br/> |Используется для любой из предыдущих символы кавычек (например, `"[\-\\\[\]]"` означает, что-, \, [, и] могут знаков).  <br/> |
   
 **ulFlags**
  
> Битовая маска флаги, используемые для обозначения формата фильтра знаков. Можно задать следующий флаг:
    
MAPI_UNICODE
  
> Фильтр — в формате Юникод. Если флаг MAPI_UNICODE не установлен, в формате ANSI — фильтра.
    
 **ulNumCharsAllowed**
  
> Максимальное число символов, которые пользователь может ввести в текстовом поле.
    
 **ulPropTag**
  
> Свойство tag для свойства типа PT_TSTRING. Элемент **ulPropTag** определяет свойство строки, данные которого отображается и редактируется в элементе управления. 
    
## <a name="remarks"></a>Замечания

Структура **DTBLEDIT** описывает элемент управления редактирования область на диалоговое окно, которое содержит буквенно-цифровой информации. Почти все диалоговые окна имеют по крайней мере один элемент управления. Редактирование элементов управления может быть изменяемым пользователем, или только для чтения. 
  
Элементы управления поля ввода также может быть одной строки или multiline. Элементы управления многострочный текст обычно содержат полосы прокрутки, связанных с ними. 
  
Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md). Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[Каноническое свойство PidTagControlType](pidtagcontroltype-canonical-property.md)


[Структуры MAPI](mapi-structures.md)
