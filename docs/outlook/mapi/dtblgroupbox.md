---
title: DTBLGROUPBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLGROUPBOX
api_type:
- COM
ms.assetid: 5e444b62-d6b6-4cfc-8601-d34aa004c1e6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ef38893c9ad44556cc9220809b5e407f86fd2642
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576318"
---
# <a name="dtblgroupbox"></a>DTBLGROUPBOX

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Описывает элемент управления поля группы, которая будет использоваться в диалоговое окно, построенная на основе таблицы отображения.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макрос:  <br/> |[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Положение в памяти, который описывается в поле Группа строки. Если отображается, метка отображается в верхней, левой части поле.
    
 **ulFlags**
  
> Битовая маска флагов используется для назначения формат подписи, на который указывает член **ulbLpszLabel** . Можно задать следующий флаг: 
    
MAPI_UNICODE 
  
> Метка имеет формат Юникод. Если флаг MAPI_UNICODE не установлен, в формате ANSI имеет название.
    
## <a name="remarks"></a>Замечания

Структура **DTBLGROUPBOX** описывает элемент управления поля группы, который используется для визуально сопоставить другие элементы управления в диалоговом окне. Метод выделения состоит из соседних другие элементы управления полем. 
  
Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md). Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)


[Структуры MAPI](mapi-structures.md)

