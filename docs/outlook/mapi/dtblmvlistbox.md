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
ms.openlocfilehash: 0de5bf5d5bb4d8c5606e97bdbc6e70493609a05f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808365"
---
# <a name="dtblmvlistbox"></a>DTBLMVLISTBOX

  
  
**Относится к**: Outlook 
  
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

