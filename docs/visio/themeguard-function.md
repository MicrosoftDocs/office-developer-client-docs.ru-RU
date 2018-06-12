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
# <a name="themeguard-function"></a><span data-ttu-id="31f5c-103">Функция THEMEGUARD</span><span class="sxs-lookup"><span data-stu-id="31f5c-103">THEMEGUARD Function</span></span>

<span data-ttu-id="31f5c-104">Защищает ячейки форматирования фигуры, чтобы убедиться, что они используют соответствующих аспектов текущей темы.</span><span class="sxs-lookup"><span data-stu-id="31f5c-104">Guards the formatting cells of a shape to ensure that they use appropriate aspects of the current theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="31f5c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31f5c-105">Syntax</span></span>

<span data-ttu-id="31f5c-106">THEMEGUARD()</span><span class="sxs-lookup"><span data-stu-id="31f5c-106">THEMEGUARD()</span></span>
  
## <a name="remarks"></a><span data-ttu-id="31f5c-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="31f5c-107">Remarks</span></span>

<span data-ttu-id="31f5c-108">Применение функции THEMEGUARD ячейки не обеспечивает защиты вручную форматирования таким же образом, применение УСЛОВИЕ функции.</span><span class="sxs-lookup"><span data-stu-id="31f5c-108">Applying the THEMEGUARD function to a cell does not guard against manual formatting in the same way that applying the GUARD function does.</span></span> <span data-ttu-id="31f5c-109">Если применить форматирование фигур в пользовательском интерфейсе, или программным способом, с помощью автоматизации формула THEMEGUARD имеет преимущество, если не включить функцию SETATREFEXPR в формулу для хранения вручную форматирования значения.</span><span class="sxs-lookup"><span data-stu-id="31f5c-109">If you apply formatting to the shape in the user interface or programmatically, by means of Automation, the THEMEGUARD formula is overridden, unless you include the SETATREFEXPR function in the formula to store the manual formatting value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="31f5c-110">Пример</span><span class="sxs-lookup"><span data-stu-id="31f5c-110">Example</span></span>

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

<span data-ttu-id="31f5c-111">Задает цвет Акцент 2 из текущей темы, а не цвет заливки основной темы фигуры.</span><span class="sxs-lookup"><span data-stu-id="31f5c-111">Specifies that the shape take the Accent 2 color from the current theme, rather than the main theme fill color.</span></span>
  

