---
title: Функция RED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251487
localization_priority: Normal
ms.assetid: a95fd86d-ebc1-66b6-e7d9-9c8ea84d23ab
description: Возвращает красный компонент цвета.
ms.openlocfilehash: e8c6115ac0441b25ce8333485828e8ef0f615459
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359985"
---
# <a name="red-function"></a>Функция RED

Возвращает красный компонент цвета. 
  
## <a name="syntax"></a>Синтаксис

RED (* * *Expression* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Обязательный  <br/> |**Разные** <br/> |Индекс цвета в таблице цветов документа, выражение, которое разрешается в настраиваемый цвет (например, RGB или HSL), или ссылка на ячейку, содержащую цветовой индекс или цветовой результат.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Номер
  
## <a name="remarks"></a>Примечания

Возвращаемое значение — число в диапазоне от 0 до 255 включительно, или ссылку на ячейку, которая разрешается в индекс. Если _выражение_ недопустимо, эта функция возвращает значение 0 (Black). 
  
## <a name="example-1"></a>Пример 1

КРАСНЫЙ (22)
  
Возвращает 51, если в документе используется цветовая палитра Microsoft Office Visio по умолчанию, где темно-серый — цвет с индексом 22.
  
## <a name="example-2"></a>Пример 2

КРАСНЫЙ (char. Color)
  
Возвращает значение красного компонента текущего цвета шрифта.
  
## <a name="example-3"></a>Пример 3

RED (RGB (10, 20, 30))
  
Возвращает 10.
  

