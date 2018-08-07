---
title: Функция THEMEGUARD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: Защищает ячейки форматирования фигуры, чтобы убедиться, что они используют соответствующих аспектов текущей темы.
ms.openlocfilehash: 10a7772995b9cc22e53ff577b2f663d7c97d0816
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815019"
---
# <a name="themeguard-function"></a>Функция THEMEGUARD

Защищает ячейки форматирования фигуры, чтобы убедиться, что они используют соответствующих аспектов текущей темы.
  
## <a name="syntax"></a>Синтаксис

THEMEGUARD()
  
## <a name="remarks"></a>Замечания

Применение функции THEMEGUARD ячейки не обеспечивает защиты вручную форматирования таким же образом, применение УСЛОВИЕ функции. Если применить форматирование фигур в пользовательском интерфейсе, или программным способом, с помощью автоматизации формула THEMEGUARD имеет преимущество, если не включить функцию SETATREFEXPR в формулу для хранения вручную форматирования значения. 
  
## <a name="example"></a>Пример

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

Задает цвет Акцент 2 из текущей темы, а не цвет заливки основной темы фигуры.
  

