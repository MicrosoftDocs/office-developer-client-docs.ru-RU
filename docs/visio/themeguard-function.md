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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404948"
---
# <a name="themeguard-function"></a><span data-ttu-id="5f211-103">Функция THEMEGUARD</span><span class="sxs-lookup"><span data-stu-id="5f211-103">THEMEGUARD Function</span></span>

<span data-ttu-id="5f211-104">Защищает ячейки форматирования фигуры, чтобы убедиться, что они используют соответствующие аспекты текущей темы.</span><span class="sxs-lookup"><span data-stu-id="5f211-104">Guards the formatting cells of a shape to ensure that they use appropriate aspects of the current theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5f211-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f211-105">Syntax</span></span>

<span data-ttu-id="5f211-106">THEMEGUARD ()</span><span class="sxs-lookup"><span data-stu-id="5f211-106">THEMEGUARD()</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5f211-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="5f211-107">Remarks</span></span>

<span data-ttu-id="5f211-108">Применение функции THEMEGUARD к ячейке не защищает их от ручного форматирования точно так же, как и применение функции GUARD.</span><span class="sxs-lookup"><span data-stu-id="5f211-108">Applying the THEMEGUARD function to a cell does not guard against manual formatting in the same way that applying the GUARD function does.</span></span> <span data-ttu-id="5f211-109">Если вы применяете форматирование к фигуре в пользовательском интерфейсе или программным путем с помощью автоматизации, формула THEMEGUARD переопределяется, если не включить функцию SETATREFEXPR в формулу для хранения значения форматирования вручную.</span><span class="sxs-lookup"><span data-stu-id="5f211-109">If you apply formatting to the shape in the user interface or programmatically, by means of Automation, the THEMEGUARD formula is overridden, unless you include the SETATREFEXPR function in the formula to store the manual formatting value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5f211-110">Пример</span><span class="sxs-lookup"><span data-stu-id="5f211-110">Example</span></span>

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

<span data-ttu-id="5f211-111">Указывает, что фигура получает цвет акцентов 2 из текущей темы, а не основной цвет заливки темы.</span><span class="sxs-lookup"><span data-stu-id="5f211-111">Specifies that the shape take the Accent 2 color from the current theme, rather than the main theme fill color.</span></span>
  

