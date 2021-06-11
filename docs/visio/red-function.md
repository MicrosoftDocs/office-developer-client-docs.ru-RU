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
| _expression_ <br/> |Обязательный  <br/> |**Разные** <br/> |Индекс цвета в цветной таблице документа, выражение, которое решается на настраиваемый цвет (например, RGB или HSL), или ссылку на ячейку, содержаную цветной индекс или результат цвета.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Номер
  
## <a name="remarks"></a>Примечания

Возвращаемая величина — это число в диапазоне от 0 до 255 включительно или ссылка на ячейку, которая решается на индекс. Если  _выражение_ является недействительным, эта функция возвращает 0 (черный). 
  
## <a name="example-1"></a>Пример 1

RED (22)
  
Возвращает 51, если в документе используется Microsoft Office Visio цветовая палитра, где темно-серый — это цвет в индексе 22.
  
## <a name="example-2"></a>Пример 2

RED (Char.Color)
  
Возвращает значение красного компонента текущего цвета шрифта.
  
## <a name="example-3"></a>Пример 3

RED (RGB(10, 20, 30))
  
Возвращает 10.
  

