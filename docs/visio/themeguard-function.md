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
# <a name="themeguard-function"></a><span data-ttu-id="e9d9a-103">Функция THEMEGUARD</span><span class="sxs-lookup"><span data-stu-id="e9d9a-103">THEMEGUARD Function</span></span>

<span data-ttu-id="e9d9a-104">Обеспечивает безопасность ячеек форматирования фигуры, чтобы убедиться, что они используют соответствующие аспекты текущей темы.</span><span class="sxs-lookup"><span data-stu-id="e9d9a-104">Guards the formatting cells of a shape to ensure that they use appropriate aspects of the current theme.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e9d9a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9d9a-105">Syntax</span></span>

<span data-ttu-id="e9d9a-106">THEMEGUARD()</span><span class="sxs-lookup"><span data-stu-id="e9d9a-106">THEMEGUARD()</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e9d9a-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="e9d9a-107">Remarks</span></span>

<span data-ttu-id="e9d9a-108">Применение функции THEMEGUARD к ячейке не защититься от ручного форматирования так же, как при применении функции GUARD.</span><span class="sxs-lookup"><span data-stu-id="e9d9a-108">Applying the THEMEGUARD function to a cell does not guard against manual formatting in the same way that applying the GUARD function does.</span></span> <span data-ttu-id="e9d9a-109">При применении форматирования к фигуре в пользовательском интерфейсе или программным способом с помощью автоматизации формула THEMEGUARD переопределяется, если в формулу не включена функция SETATREFEXPR для хранения значения форматирования вручную.</span><span class="sxs-lookup"><span data-stu-id="e9d9a-109">If you apply formatting to the shape in the user interface or programmatically, by means of Automation, the THEMEGUARD formula is overridden, unless you include the SETATREFEXPR function in the formula to store the manual formatting value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e9d9a-110">Пример</span><span class="sxs-lookup"><span data-stu-id="e9d9a-110">Example</span></span>

```vb
Shape.FillForegnd = THEMEGUARD(THEME("AccentColor2")
```

<span data-ttu-id="e9d9a-111">Указывает, что фигура принимает цвет Accent 2 из текущей темы, а не цвета заливки основной темы.</span><span class="sxs-lookup"><span data-stu-id="e9d9a-111">Specifies that the shape take the Accent 2 color from the current theme, rather than the main theme fill color.</span></span>
  

