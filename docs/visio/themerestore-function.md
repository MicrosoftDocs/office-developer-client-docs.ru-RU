---
title: Функция THEMERESTORE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ca7e6621-f39b-64dd-3594-41d74da21a94
description: Сохраняет локальное значение формата фигуры при применении темы, чтобы можно было восстановить локальное форматирование Если пользователь удаляет впоследствии темы.
ms.openlocfilehash: f22f603cad1d310adc59d19e9b3e3882bd797fce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815032"
---
# <a name="themerestore-function"></a>Функция THEMERESTORE

Сохраняет локальное значение формата фигуры при применении темы, чтобы можно было восстановить локальное форматирование Если пользователь удаляет впоследствии темы.
  
## <a name="syntax"></a>Синтаксис

THEMERESTORE()
  
## <a name="example"></a>Пример

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

Восстанавливает форматирование цвет заливки локального ранее примененные к фигуры при удалении текущей темы.
  

