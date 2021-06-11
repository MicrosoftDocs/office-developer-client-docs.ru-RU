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
ms.openlocfilehash: 94e412f2f542298adcedf4414c19b5303330cf2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434601"
---
# <a name="dtblradiobutton"></a>DTBLRADIOBUTTON

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает одну кнопку радио, которая будет частью группы кнопок радио. Группа кнопок радио будет использоваться в диалоговом окне, построенной из таблицы отображения.
  
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

## <a name="members"></a>"Участники"

 **ulbLpszLabel**
  
> Положение в памяти метки строки символов для кнопки радио.
    
 **ulFlags**
  
> Bitmask флагов, используемых для обозначения формата метки, указанной членом **ulbLpszLabel.** Можно установить следующий флаг: 
    
MAPI_UNICODE 
  
> Метка находится в формате Unicode. Если флаг MAPI_UNICODE не установлен, метка находится в формате ANSI.
    
 **ulcButtons**
  
> Количество кнопок в группе кнопки радио. Структуры **DTBLRADIOBUTTON** для других кнопок в группе должны содержаться в последовательных строках таблицы отображения. Каждая из этих строк должна содержать одинаковое значение для **члена ulcButtons.** 
    
 **ulPropTag**
  
> Тег свойства для свойства типа PT_LONG. Начальный выбор в группе кнопок радио основан на начальном значении этого свойства. Каждая кнопка в группе должна иметь **набор ulPropTag** к одному свойству. 
    
 **lReturnValue**
  
> Уникальный номер, идентифицирует выбранную кнопку.
    
## <a name="remarks"></a>Примечания

Структура **DTBLRADIOBUTTON** описывает кнопку радио кнопку управления кнопкой, которая связана с группой кнопок. Проверить можно только одну кнопку в группе; установка одной кнопки приводит к отсечению других кнопок в группе. 
  
Количество кнопок — это количество кнопок радио в группе. Структуры для других кнопок радио в группе должны быть в последующих строках в таблице отображения. Каждая из этих структур должна иметь одинаковое значение для подсчета кнопок.
  
Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md) Сведения о реализации таблицы отображения см. в таблице [Implementing a Display Table.](display-table-implementation.md)
  
## <a name="see-also"></a>См. также



[BuildDisplayTable](builddisplaytable.md)
  
[DTCTL](dtctl.md)
  
[SizedDtblButton](sizeddtblbutton.md)


[Структуры MAPI](mapi-structures.md)

