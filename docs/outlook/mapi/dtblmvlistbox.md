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
ms.openlocfilehash: ae8f3ab28837bf0579549ead46c28477f815f35c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439704"
---
# <a name="dtblmvlistbox"></a>DTBLMVLISTBOX

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Описывает список с несколькими значениями, который будет отображаться в диалоговом окне, построенном из таблицы отображения.
  
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

## <a name="members"></a>Элементы

 **ulFlags**
  
> Зарезервировано; должно быть нулем.
    
 **ulMVPropTag**
  
> Тег свойства для многомерного свойства типа PT_MV_TSTRING.
    
## <a name="remarks"></a>Примечания

Структура **DTBLMVLISTBOX** описывает стандартный список с несколькими значениями, который имеет список элементов только для чтения. При использовании стандартного списка с несколькими значениями значения отображаются немедленно. 
  
Отображаемая информация поступает из свойства, которое определено в **члене ulMVPropTag.** Не существует требований для чтения из интерфейса свойств, связанного с таблицей отображения. Кроме того, поскольку пользователи не могут выбирать из этих типов списков, данные не будут записаны в интерфейс свойств. 
  
Для списка с несколькими значениями поддерживаются только свойства строк с несколькими значениями; другие типы свойств с несколькими значениями не поддерживаются. 
  
Обзор таблиц отображения см. в [таблице отображения.](display-tables.md) Сведения о реализации таблицы отображения см. в таблице ["Реализация таблицы отображения".](display-table-implementation.md)
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)


[Структуры MAPI](mapi-structures.md)

