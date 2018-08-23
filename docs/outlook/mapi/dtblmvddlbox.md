---
title: DTBLMVDDLBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVDDLBOX
api_type:
- COM
ms.assetid: 0e6283dc-9a08-460f-9400-03f0ceb4081c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 910f779f3463ee5dccd052655a442ef24c2cce58
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570683"
---
# <a name="dtblmvddlbox"></a>DTBLMVDDLBOX

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Описывает раскрывающегося списка, который будет использоваться в диалоговом окне, построенного из таблицы отображения.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a>Members

 **ulFlags**
  
> Зарезервировано; должно быть равно нулю.
    
 **ulMVPropTag**
  
> Свойство tag для многозначного свойства типа PT_MV_TSTRING. Различные значения этого свойства отображаются в виде отдельных записей в раскрывающемся списке.
    
## <a name="remarks"></a>Замечания

Структура **DTBLMVDDLBOX** описывает многозначные раскрывающегося списка только для чтения список элементов. С помощью многозначные раскрывающегося списка, значения отображаются при щелчке полосы прокрутки. 
  
Данные, который отображается, поступающие из свойства, обнаруженных в элементе **ulMVPropTag** . Не является обязательным для чтения из интерфейса свойства, связанного с таблицей отображения. Кроме того так как пользователи не могут выбирать из этих типов списков, данные не записываются в интерфейсе свойство. 
  
Поддерживаются только те свойства, поддерживающий несколько значений string для многозначные раскрывающегося списка; другие типы многозначного свойства не поддерживаются. 
  
Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md). Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)


[Структуры MAPI](mapi-structures.md)

