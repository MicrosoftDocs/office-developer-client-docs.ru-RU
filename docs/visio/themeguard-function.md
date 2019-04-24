---
title: Функция THEMEGUARD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: Защищает ячейки форматирования фигуры, чтобы убедиться, что они используют соответствующие аспекты текущей темы.
ms.openlocfilehash: c20d43f9d03296a3c529a6c8f59cf27489dcdc51
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326756"
---
# <a name="themeguard-function"></a>Функция THEMEGUARD

Защищает ячейки форматирования фигуры, чтобы убедиться, что они используют соответствующие аспекты текущей темы.
  
## <a name="syntax"></a>Синтаксис

THEMEGUARD ()
  
## <a name="remarks"></a>Замечания

Применение функции THEMEGUARD к ячейке не защищает их от ручного форматирования точно так же, как и применение функции GUARD. Если вы применяете форматирование к фигуре в пользовательском интерфейсе или программным путем с помощью автоматизации, формула THEMEGUARD переопределяется, если не включить функцию SETATREFEXPR в формулу для хранения значения форматирования вручную. 
  
## <a name="example"></a>Пример

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

Указывает, что фигура получает цвет акцентов 2 из текущей темы, а не основной цвет заливки темы.
  

