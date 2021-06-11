---
title: Функция THEMERESTORE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ca7e6621-f39b-64dd-3594-41d74da21a94
description: Сохраняет локальное значение форматирования фигуры при применении темы, чтобы можно было восстановить локальное форматирование, если пользователь впоследствии удаляет тему.
ms.openlocfilehash: 628e246f91172f136dd1a70807fca2abc1ff5bdd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404290"
---
# <a name="themerestore-function"></a><span data-ttu-id="5c863-103">Функция THEMERESTORE</span><span class="sxs-lookup"><span data-stu-id="5c863-103">THEMERESTORE Function</span></span>

<span data-ttu-id="5c863-104">Сохраняет локальное значение форматирования фигуры при применении темы, чтобы можно было восстановить локальное форматирование, если пользователь впоследствии удаляет тему.</span><span class="sxs-lookup"><span data-stu-id="5c863-104">Stores the local formatting value of a shape when you apply a theme so that you can restore the local formatting if the user subsequently removes the theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5c863-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c863-105">Syntax</span></span>

<span data-ttu-id="5c863-106">THEMERESTORE()</span><span class="sxs-lookup"><span data-stu-id="5c863-106">THEMERESTORE()</span></span>
  
## <a name="example"></a><span data-ttu-id="5c863-107">Пример</span><span class="sxs-lookup"><span data-stu-id="5c863-107">Example</span></span>

```vb
Shape.FillForegnd = THEME("FillColor") + THEMERESTORE(RGB(255,102,0)
```

<span data-ttu-id="5c863-108">Восстанавливает локальный формат цветовой заливки, который ранее применялся к фигуре при удалении текущей темы.</span><span class="sxs-lookup"><span data-stu-id="5c863-108">Restores local fill color formatting previously applied to a shape when the current theme is removed.</span></span>
  

