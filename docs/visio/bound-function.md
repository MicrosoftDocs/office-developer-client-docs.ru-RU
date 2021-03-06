---
title: Функция BOUND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60099
localization_priority: Normal
ms.assetid: 36374d78-1028-bd7f-6282-66555ee31306
description: Ограничивает значение ячейки диапазоном или набором диапазонов.
ms.openlocfilehash: 85fbe66d4e458ac4e42c9eb3c65b9a3a1d8211df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425962"
---
# <a name="bound-function"></a>Функция BOUND

Ограничивает значение ячейки диапазоном или набором диапазонов.
  
## <a name="syntax"></a>Синтаксис

BOUND (** *значение* **, **** тип **, **** игнорировать **, ** *значение1* **, ** *значение2* ** ** * [,игнорировать(n), value1(n), value2(n),...] * ** 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _value_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Текущее ограниченное значение.  <br/> |
| _type_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Является ли ограничение включено (0), эксклюзивно (1) или отключено (2).  <br/> |
| _игнорировать_ <br/> |Обязательный  <br/> |**Логический** <br/> | TRUE, чтобы игнорировать диапазон; FALSE, чтобы ограничить значение ячейки в диапазоне.  <br/> |
| _value1_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Первое значение в диапазоне.  <br/> |
| _value2_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Второе значение в диапазоне.  <br/> |
   
## <a name="remarks"></a>Примечания

Используйте функцию BOUND, чтобы ограничить значение ячейки верхней и нижней частью, например, для управления объектами, которые не должны растягиваться выше или ниже минимальной или максимальной высоты. Ограничение может быть инклюзивным или эксклюзивным по отношению к диапазону или диапазонам. Если текущее значение не должно быть ограничено, установите параметр  _типа_ 2 (отключен). 
  
Вы можете определить несколько диапазонов, поставляя несколько вхождений параметров _ignore,_ _value1_ и _value2._ Используйте параметр  _ignore_ для отключения ограничений определенным диапазоном. 
  
Формула, содержащая функцию BOUND, не перезаписывается при изменениях ее значения; вместо этого формула сохраняется и новое значение помещается в _параметр значения._ 
  
## <a name="example-1"></a>Пример 1

В этом примере функция BOUND использует функцию BOUND, чтобы заставить ручку управления оставаться в границах фигуры. 
  
Controls.X1 = BOUND(Width \* 0.5, 0, FALSE, Width \* 0, Width \* 1)
  
Controls.Y1 = BOUND(Height \* 0.5, 0, FALSE, Height \* 0, Height \* 1)
  
## <a name="example-2"></a>Пример 2

В этом примере функция BOUND ограничивает ширину фигуры до 2 дюймов, 4 дюймов или 6 дюймов. 
  
Ширина = BOUND(, 0, FALSE, 2 в, 2 в, FALSE, 4 в, 4, FALSE, 6 in, 6 in)
  

