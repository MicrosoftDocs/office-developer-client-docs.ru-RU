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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Описывает одну кнопку, которая будет частью группы. Группа radio button будет использоваться в диалоговом окне, построенного из таблицы отображения.
  
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
  
> Положение в памяти метки строки символов для радио кнопки.
    
 **ulFlags**
  
> Битовая метка флагов, используемая для обозначения формата метки, на который указывает элемент **ulbLpszLabel.** Можно установить следующий флаг: 
    
MAPI_UNICODE 
  
> Метка имеет формат Юникод. Если флаг MAPI_UNICODE не установлен, метка будет в формате ANSI.
    
 **ulcButtons**
  
> Количество кнопок в группе кнопок. Структуры **DTBLRADIOBUTTON** для других кнопок в группе должны содержаться в последовательных строках таблицы отображения. Каждая из этих строк должна содержать одинаковое значение для **члена ulcButtons.** 
    
 **ulPropTag**
  
> Тег свойства для свойства типа PT_LONG. Начальный выбор в группе radio button основан на начальном значении этого свойства. Каждая кнопка в группе должна иметь **ulPropTag** с одинаковым свойством. 
    
 **lReturnValue**
  
> Уникальный номер, идентифицирует выбранную кнопку.
    
## <a name="remarks"></a>Примечания

Структура **DTBLRADIOBUTTON** описывает кнопку с кнопкой, связанной с группой кнопок. Можно проверить только одну кнопку в группе; если установить одну кнопку, остальные кнопки в группе будут не замечены. 
  
Число кнопок — это количество кнопок в группе. Структуры других radio buttons в группе должны быть в последующих строках в таблице отображения. Каждая из этих структур должна иметь одинаковое значение для своего подсчета кнопок.
  
Обзор таблиц отображения см. в [таблице отображения.](display-tables.md) Сведения о реализации таблицы отображения см. в таблице ["Реализация таблицы отображения".](display-table-implementation.md)
  
## <a name="see-also"></a>См. также



[BuildDisplayTable](builddisplaytable.md)
  
[DTCTL](dtctl.md)
  
[SizedDtblButton](sizeddtblbutton.md)


[Структуры MAPI](mapi-structures.md)

