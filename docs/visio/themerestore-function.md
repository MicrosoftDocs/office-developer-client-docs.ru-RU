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
# <a name="themerestore-function"></a><span data-ttu-id="ee92b-103">Функция THEMERESTORE</span><span class="sxs-lookup"><span data-stu-id="ee92b-103">THEMERESTORE Function</span></span>

<span data-ttu-id="ee92b-104">Сохраняет локальное значение формата фигуры при применении темы, чтобы можно было восстановить локальное форматирование Если пользователь удаляет впоследствии темы.</span><span class="sxs-lookup"><span data-stu-id="ee92b-104">Stores the local formatting value of a shape when you apply a theme so that you can restore the local formatting if the user subsequently removes the theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ee92b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee92b-105">Syntax</span></span>

<span data-ttu-id="ee92b-106">THEMERESTORE()</span><span class="sxs-lookup"><span data-stu-id="ee92b-106">THEMERESTORE()</span></span>
  
## <a name="example"></a><span data-ttu-id="ee92b-107">Пример</span><span class="sxs-lookup"><span data-stu-id="ee92b-107">Example</span></span>

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

<span data-ttu-id="ee92b-108">Восстанавливает форматирование цвет заливки локального ранее примененные к фигуры при удалении текущей темы.</span><span class="sxs-lookup"><span data-stu-id="ee92b-108">Restores local fill color formatting previously applied to a shape when the current theme is removed.</span></span>
  

