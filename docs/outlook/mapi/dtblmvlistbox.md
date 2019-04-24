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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338278"
---
# <a name="dtblmvlistbox"></a>DTBLMVLISTBOX

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает Многозначный список, который будет отображаться в диалоговом окне, созданном из таблицы отображения.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a>Элементы

 **ulFlags**
  
> Резервирования должно быть равно нулю.
    
 **Улмвпроптаг**
  
> Тег свойства с многозначным свойством типа ПТ_МВ_ТСТРИНГ.
    
## <a name="remarks"></a>Комментарии

Структура **дтблмвлистбокс** описывает стандартный Многозначный список, содержащий список элементов, предназначенный только для чтения. При использовании стандартного многозначного списка значения отображаются сразу. 
  
Отображаемые данные берутся из свойства, указанного в элементе **улмвпроптаг** . Нет необходимости считывать сведения из интерфейса свойства, связанного с таблицей отображения. Кроме того, так как пользователи не могут выбирать элементы из этих типов списков, данные не записываются в интерфейс свойств. 
  
В списке с несколькими значениями поддерживаются только многозначные строковые свойства; другие многозначные типы свойств не поддерживаются. 
  
Общие сведения о отображаемых таблицах приведены в разделе [Display Tables](display-tables.md). Сведения о том, как реализовать таблицу отображения, можно найти [в статье реализация таблицы отображения](display-table-implementation.md).
  
## <a name="see-also"></a>См. также



[DTCTL](dtctl.md)


[Структуры MAPI](mapi-structures.md)

