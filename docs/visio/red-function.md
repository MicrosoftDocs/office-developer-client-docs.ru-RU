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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415525"
---
# <a name="red-function"></a>Функция RED

Возвращает красный компонент цвета. 
  
## <a name="syntax"></a>Синтаксис

RED(** *expression* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Обязательный  <br/> |**Разные** <br/> |Индекс цвета в таблице цветов документа, выражение, которое соеется с пользовательским цветом (например, RGB или HSL) или ссылку на ячейку, которая содержит индекс цвета или результат цвета.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Числовой
  
## <a name="remarks"></a>Примечания

Возвращаемая величина — это число в диапазоне от 0 до 255 включительно или ссылка на ячейку, разрешаемая в индекс. Если  _выражение_ недопустимо, эта функция возвращает 0 (черный). 
  
## <a name="example-1"></a>Пример 1

RED(22)
  
Возвращает значение 51, если документ использует Microsoft Office Visio по умолчанию, где темно-серый цвет — это цвет в индексе 22.
  
## <a name="example-2"></a>Пример 2

RED(Char.Color)
  
Возвращает значение красного компонента текущего цвета шрифта.
  
## <a name="example-3"></a>Пример 3

RED(RGB(10, 20, 30))
  
Возвращает 10.
  

