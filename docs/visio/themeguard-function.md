---
title: Функция THEMEGUARD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: Охраняет ячейки форматирования фигуры, чтобы убедиться, что они используют соответствующие аспекты текущей темы.
ms.openlocfilehash: c20d43f9d03296a3c529a6c8f59cf27489dcdc51
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404948"
---
# <a name="themeguard-function"></a>Функция THEMEGUARD

Охраняет ячейки форматирования фигуры, чтобы убедиться, что они используют соответствующие аспекты текущей темы.
  
## <a name="syntax"></a>Синтаксис

THEMEGUARD()
  
## <a name="remarks"></a>Примечания

Применение функции THEMEGUARD к ячейке не оградило от ручного форматирования так же, как и применение функции GUARD. Если применить форматирование к фигуре в пользовательском интерфейсе или программным способом, с помощью автоматизации формула THEMEGUARD переопределяется, если не включить функцию SETATREFEXPR в формулу для хранения значения ручного форматирования. 
  
## <a name="example"></a>Пример

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

Указывает, что форма принимает цвет Accent 2 из текущей темы, а не основной цвет заполнения темы.
  

