---
title: DTBLMVLISTBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVLISTBOX
api_type:
- COM
ms.assetid: 1c22f842-d0e7-44f0-a7d5-c9c2aa6b8820
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f7c1241f2ad31dee8277f3b3b77ac02137067a12
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576311"
---
# <a name="dtblmvlistbox"></a>DTBLMVLISTBOX

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Список, который будет отображаться в диалоговом окне, построенного из таблицы Отображаемое описание.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a>Members

 **ulFlags**
  
> Зарезервировано; должно быть равно нулю.
    
 **ulMVPropTag**
  
> Свойство tag для многозначного свойства типа PT_MV_TSTRING.
    
## <a name="remarks"></a>Замечания

Структура **DTBLMVLISTBOX** описывает стандартные список со списком только для чтения элементов. С помощью стандартных список, немедленно отображаются значения. 
  
Данные, который отображается, поступающие из свойства, обнаруженных в элементе **ulMVPropTag** . Не является обязательным для чтения из интерфейса свойства, связанного с таблицей отображения. Кроме того так как пользователи не смогут выбирать из этих типов списков, данные не записываются в интерфейсе свойство. 
  
Только те свойства, поддерживающий несколько значений string, поддерживаются для многозначного списка; другие типы многозначного свойства не поддерживаются. 
  
Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md). Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)


[Структуры MAPI](mapi-structures.md)

