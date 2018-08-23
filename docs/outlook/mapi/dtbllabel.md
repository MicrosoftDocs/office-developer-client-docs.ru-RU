---
title: DTBLLABEL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLABEL
api_type:
- COM
ms.assetid: 5837facf-acd3-48fe-9610-f88085d99aef
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 09f0d7988f85a6d6018c45cb64245ab331cda052
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582814"
---
# <a name="dtbllabel"></a>DTBLLABEL

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Описание метки, который будет использоваться в диалоговом окне, построенного из таблицы отображения.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макросов  <br/> |[SizedDtblLabel](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a>Members

 **ulbLpszLabelName**
  
> Положение в памяти метки строка символов.
    
 **ulFlags**
  
> Битовая маска флагов используется для назначения формат подписи, на который указывает член **ulbLpszLabelName** . Можно задать следующий флаг: 
    
MAPI_UNICODE 
  
> Метка имеет формат Юникод. Если флаг MAPI_UNICODE не установлен, в формате ANSI имеет название.
    
## <a name="remarks"></a>Замечания

Структура **DTBLLABEL** описывает текст элемента управления метки, который будет отображаться с другой тип элемента управления для добавления значение для этого элемента управления. Например изменить элементы управления располагаются рядом с пунктом меток для оповещения пользователя тип данных, который должен быть введен. Некоторые элементы управления, такие как группа полей и кнопок-переключателей, нажмите и удерживайте собственные метки. 
  
Метка может включать ускорителя Windows, определенные как символ, следующий амперсанд (&amp;). Нажав сочетание клавиш перемещает фокус в первом nonlabel nonbutton управления версиями в этой метки в таблице отображения.
  
Multiline меток не поддерживается. Отображение нескольких строк требует нескольких метки.
  
Не поддерживается для использования в качестве элемента управления только для чтения изменить метку. Разница —, что элемента управления можно выделить и скопировать в то время как метка не удается. 
  
Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md). Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)


[Структуры MAPI](mapi-structures.md)

