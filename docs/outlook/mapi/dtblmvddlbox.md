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
ms.openlocfilehash: 33b4fd87f33c26db15e1a6a28f077c393168db91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420747"
---
# <a name="dtblmvddlbox"></a>DTBLMVDDLBOX

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает отбрасывной список, который будет использоваться в диалоговом окне, построенного из таблицы отображения.
  
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

## <a name="members"></a>Элементы

 **ulFlags**
  
> Зарезервировано; должно быть нулевой.
    
 **ulMVPropTag**
  
> Тег свойства для многомерного свойства типа PT_MV_TSTRING. Различные значения этого свойства отображаются в качестве отдельных записей в выпадаемом списке.
    
## <a name="remarks"></a>Примечания

Структура **DTBLMVDDLBOX** описывает многоценный список элементов только для чтения. С помощью многомерного списка выпаданий значения отображаются, когда пользователь щелкает по панели прокрутки. 
  
Отображаемая информация поступает из свойства, обнаруженного в **члене ulMVPropTag.** Не нужно читать из интерфейса свойства, связанного с таблицей отображения. Кроме того, поскольку пользователи не могут сделать выбор из этих типов полей списков, данные не записаны в интерфейс свойства. 
  
Поддерживаются только свойства строк с несколькими значениями для многомерного отсевного списка; другие типы свойств с несколькими значениями не поддерживаются. 
  
Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md) Сведения о реализации таблицы отображения см. в таблице [Implementing a Display Table.](display-table-implementation.md)
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)


[Структуры MAPI](mapi-structures.md)

