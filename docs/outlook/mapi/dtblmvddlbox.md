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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Описание выпадаемого списка, который будет использоваться в диалоговом окне, построенного из таблицы отображения.
  
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
  
> Зарезервировано; должно быть нулем.
    
 **ulMVPropTag**
  
> Тег свойства для многомерного свойства типа PT_MV_TSTRING. Различные значения этого свойства отображаются в качестве отдельных записей в выпадаемом списке.
    
## <a name="remarks"></a>Примечания

Структура **DTBLMVDDLBOX** описывает список элементов с несколькими значениями в списке только для чтения. При использовании выпадаемого списка с несколькими значениями значения отображаются, когда пользователь щелкает удручайку. 
  
Отображаемая информация поступает из свойства, которое определено в **члене ulMVPropTag.** Не существует требований для чтения из интерфейса свойств, связанного с таблицей отображения. Кроме того, поскольку пользователи не могут выбирать из этих типов полей списков, данные не будут записаны в интерфейс свойств. 
  
В выпадаемом списке с несколькими значениями поддерживаются только свойства строк с несколькими значениями; другие типы свойств с несколькими значениями не поддерживаются. 
  
Обзор таблиц отображения см. в [таблице отображения.](display-tables.md) Сведения о реализации таблицы отображения см. в таблице ["Реализация таблицы отображения".](display-table-implementation.md)
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)


[Структуры MAPI](mapi-structures.md)

