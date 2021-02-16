---
title: Функция THEMEGUARD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a556eadc-9ee6-7a29-ca05-6250b612790c
description: Обеспечивает безопасность ячеек форматирования фигуры, чтобы убедиться, что они используют соответствующие аспекты текущей темы.
ms.openlocfilehash: c20d43f9d03296a3c529a6c8f59cf27489dcdc51
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404948"
---
# <a name="themeguard-function"></a>Функция THEMEGUARD

Обеспечивает безопасность ячеек форматирования фигуры, чтобы убедиться, что они используют соответствующие аспекты текущей темы.
  
## <a name="syntax"></a>Синтаксис

THEMEGUARD()
  
## <a name="remarks"></a>Примечания

Применение функции THEMEGUARD к ячейке не защититься от ручного форматирования так же, как при применении функции GUARD. При применении форматирования к фигуре в пользовательском интерфейсе или программным способом с помощью автоматизации формула THEMEGUARD переопределяется, если в формулу не включена функция SETATREFEXPR для хранения значения форматирования вручную. 
  
## <a name="example"></a>Пример

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

Указывает, что фигура принимает цвет Accent 2 из текущей темы, а не цвета заливки основной темы.
  

