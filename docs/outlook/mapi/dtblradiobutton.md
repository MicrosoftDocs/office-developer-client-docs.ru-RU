---
title: DTBLRADIOBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLRADIOBUTTON
api_type:
- COM
ms.assetid: 64cef938-ef6f-43bb-8f6e-d4cd4d6c9888
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 493176029be3e7b154188aa164a95a8bc9c0e7d9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569745"
---
# <a name="dtblradiobutton"></a>DTBLRADIOBUTTON

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Описание одного переключателя, который будет частью группы переключателей. В диалоговом окне, построенного из таблицы отображения будет использоваться группы переключателей.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLRADIOBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulcButtons;
  ULONG ulPropTag;
  long lReturnValue;
} DTBLRADIOBUTTON, FAR *LPDTBLRADIOBUTTON;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Положение в памяти метки строка символов для переключателя.
    
 **ulFlags**
  
> Битовая маска флагов используется для назначения формат подписи, на который указывает член **ulbLpszLabel** . Можно задать следующий флаг: 
    
MAPI_UNICODE 
  
> Метка имеет формат Юникод. Если флаг MAPI_UNICODE не установлен, в формате ANSI имеет название.
    
 **ulcButtons**
  
> Число кнопок в группе. **DTBLRADIOBUTTON** структуры для кнопки группы должны быть включены в последовательных строк в таблице отображения. Каждый из этих строк должен содержать такое же значение для элемента **ulcButtons** . 
    
 **ulPropTag**
  
> Свойство tag для свойства типа PT_LONG. Начальный выбор в группе основано на начальное значение этого свойства. Всех кнопок в группе должен иметь значение одного свойства **ulPropTag** . 
    
 **lReturnValue**
  
> Уникальный номер, идентифицирующий выбранной кнопки.
    
## <a name="remarks"></a>Замечания

Структура **DTBLRADIOBUTTON** описывает переключатель элемента управления кнопка, связанный с группой кнопок. Можно проверить только одну кнопку в группе; При указании одной кнопкой других кнопок в группе, чтобы были не заданы. 
  
Кнопка счетчик — число кнопок-переключателей в группе. В следующих строках таблицы отображения должен быть структуры для остальных переключателей в группе. Каждый из этих структур должен иметь такое же значение для его счетчик кнопка.
  
Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md). Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.
  
## <a name="see-also"></a>См. также



[BuildDisplayTable](builddisplaytable.md)
  
[DTCTL](dtctl.md)
  
[SizedDtblButton](sizeddtblbutton.md)


[Структуры MAPI](mapi-structures.md)

