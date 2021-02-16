---
title: Функция SAT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251494
localization_priority: Normal
ms.assetid: 407817fb-9e4a-d2ca-6125-2440d2a417c6
description: Возвращает значение компонента насыщенности цвета.
ms.openlocfilehash: 3b3fd8e13ca9af4f0aea00d2f78c7b5c27be1932
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415007"
---
# <a name="sat-function"></a>Функция SAT

Возвращает значение компонента насыщенности цвета. 
  
## <a name="syntax"></a>Синтаксис

SAT(** *expression* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Обязательный  <br/> |**Разные** <br/> |Индекс цвета в таблице цветов документа, выражение, разрешаемого в пользовательский цвет (например, RGB или HSL) или ссылка на ячейку, содержаную индекс цвета или результат цвета.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Числовой
  
## <a name="remarks"></a>Примечания

Возвращаемая величина — это число в диапазоне от 0 до 240 включительно. Функция возвращает 0 для недопустимого ввода.
  
## <a name="example-1"></a>Пример 1

SAT(Sheet.4! FillForegnd)
  
Возвращает насыщенность цвета переднего плана заливки Sheet.4.
  
## <a name="example-2"></a>Пример 2

SAT(8)
  
Возвращает значение 240, если документ использует цветовую палитру Visio по умолчанию, где темно-красный цвет — это цвет в индексе 8.
  
## <a name="example-3"></a>Пример 3

SAT(HSL(10, 20, 30))
  
Возвращает 20.
  

