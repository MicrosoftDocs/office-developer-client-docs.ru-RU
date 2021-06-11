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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает многомерный список, который будет отображаться в диалоговом окне, построенном из таблицы отображения.
  
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
  
> Зарезервировано; должно быть нулевой.
    
 **ulMVPropTag**
  
> Тег свойства для многомерного свойства типа PT_MV_TSTRING.
    
## <a name="remarks"></a>Примечания

Структура **DTBLMVLISTBOX** описывает стандартный многоценный список, который имеет список элементов только для чтения. С помощью стандартного многомерного списка значения отображаются немедленно. 
  
Отображаемая информация поступает из свойства, обнаруженного в **члене ulMVPropTag.** Не нужно читать из интерфейса свойства, связанного с таблицей отображения. Кроме того, поскольку пользователи не могут сделать выбор из этих типов списков, данные не записаны в интерфейс свойства. 
  
Для многомерного списка поддерживаются только свойства строк с несколькими значениями; другие типы свойств с несколькими значениями не поддерживаются. 
  
Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md) Сведения о реализации таблицы отображения см. в таблице [Implementing a Display Table.](display-table-implementation.md)
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)


[Структуры MAPI](mapi-structures.md)

