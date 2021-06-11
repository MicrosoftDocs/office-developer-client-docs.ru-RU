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
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b07ea265b5dcc6b9a9abb15c6be7ac9e0f94e8ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404682"
---
# <a name="dtbledit"></a>DTBLEDIT

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает управление редактированием, которое будет использоваться в диалоговом окне, построенного из таблицы отображения.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанный макрос:  <br/> |[SizedDtblEdit](sizeddtbledit.md) <br/> |
   
```cpp
typedef struct _DTBLEDIT
{
  ULONG ulbLpszCharsAllowed;
  ULONG ulFlags;
  ULONG ulNumCharsAllowed;
  ULONG ulPropTag;
} DTBLEDIT, FAR *LPDTBLEDIT;

```

## <a name="members"></a>"Участники"

 **ulbLpszCharsAllowed**
  
> Смещение от начала структуры **DTBLEDIT** к фильтру строки символов, который описывает ограничения, если таковые есть, символам, которые можно ввести в управление редактированием. Фильтр не интерпретируется как обычное выражение, и к каждому введенному символу применяется один и тот же фильтр. Формат фильтра следующим образом: 
    
|**Символ**|**Описание**|
|:-----|:-----|
| `*` <br/> |Разрешен любой символ (например,  `"*"` ).  <br/> |
| `[ ]` <br/> |Определяет набор символов (например,  `"[0123456789]".` )  <br/> |
| `-` <br/> |Указывает диапазон символов (например,  `"[a-z]"` ).  <br/> |
| `~` <br/> |Указывает, что эти символы не разрешены (например,  `"[~0-9]"` ).  <br/> |
| `\` <br/> |Используется для цитаты любого из предыдущих символов (например, разрешены знаки  `"[\-\\\[\]]"` -, \, [и ]).  <br/> |
   
 **ulFlags**
  
> Bitmask флагов, используемых для назначить формат фильтра символов. Можно установить следующий флаг:
    
MAPI_UNICODE
  
> Фильтр находится в формате Unicode. Если флаг MAPI_UNICODE не установлен, фильтр находится в формате ANSI.
    
 **ulNumCharsAllowed**
  
> Максимальное количество символов, которые пользователь может ввести в текстовое поле.
    
 **ulPropTag**
  
> Тег свойства для свойства типа PT_TSTRING. Участник **ulPropTag** определяет свойство строки, данные которого отображаются и редактированы в области управления редактированием. 
    
## <a name="remarks"></a>Примечания

Структура **DTBLEDIT** описывает область управления редактированием в диалоговом окне с альфа-цифрами. Почти во всех диалоговом окнах есть по крайней мере одно управление редактированием. Изменение элементов управления может быть модификабельным пользователем или только для чтения. 
  
Элементы управления редактирования также могут быть одной строкой или несколькими линиями. Элементы управления несколькими линиями редактирования обычно связаны с баром прокрутки. 
  
Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md) Сведения о реализации таблицы отображения см. в таблице [Implementing a Display Table.](display-table-implementation.md)
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[Каноническое свойство PidTagControlType](pidtagcontroltype-canonical-property.md)


[Структуры MAPI](mapi-structures.md)

