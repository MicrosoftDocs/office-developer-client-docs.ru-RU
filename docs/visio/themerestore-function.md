---
title: Функция THEMERESTORE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ca7e6621-f39b-64dd-3594-41d74da21a94
description: Сохраняет значение локального форматирования фигуры при применении темы, чтобы можно было восстановить локальное форматирование, если пользователь впоследствии удалит тему.
ms.openlocfilehash: 628e246f91172f136dd1a70807fca2abc1ff5bdd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404290"
---
# <a name="themerestore-function"></a>Функция THEMERESTORE

Сохраняет значение локального форматирования фигуры при применении темы, чтобы можно было восстановить локальное форматирование, если пользователь впоследствии удалит тему.
  
## <a name="syntax"></a>Синтаксис

THEMERESTORE()
  
## <a name="example"></a>Пример

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

Восстанавливает форматирование цвета локальной заливки, ранее примененное к фигуре при удалении текущей темы.
  

