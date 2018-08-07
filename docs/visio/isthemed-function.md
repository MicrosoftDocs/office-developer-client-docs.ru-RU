---
title: Функция ISTHEMED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Возвращает логическое значение, указывающее, имеет ли фигуры темы, примененной к нему.
ms.openlocfilehash: 4311780d8686b5792e999c204ec182d23efb723c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814023"
---
# <a name="isthemed-function"></a><span data-ttu-id="6c989-103">Функция ISTHEMED</span><span class="sxs-lookup"><span data-stu-id="6c989-103">ISTHEMED Function</span></span>

<span data-ttu-id="6c989-104">Возвращает логическое значение, указывающее, имеет ли фигуры темы, примененной к нему.</span><span class="sxs-lookup"><span data-stu-id="6c989-104">Returns a Boolean value indicating whether a shape has a theme applied to it.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="6c989-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="6c989-105">Version Information</span></span>

<span data-ttu-id="6c989-106">Добавлена версия: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="6c989-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6c989-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c989-107">Syntax</span></span>

 <span data-ttu-id="6c989-108">**ISTHEMED** ()</span><span class="sxs-lookup"><span data-stu-id="6c989-108">**ISTHEMED**()</span></span>
  
## <a name="return-value"></a><span data-ttu-id="6c989-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9">Return value</span></span>

<span data-ttu-id="6c989-110">Логический</span><span class="sxs-lookup"><span data-stu-id="6c989-110">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6c989-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="6c989-111">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="6c989-112">Функция **ISTHEMED** в Visio 2013 заменяет функцию **CELLISTHEMED** из предыдущих версий Visio.</span><span class="sxs-lookup"><span data-stu-id="6c989-112">The **ISTHEMED** function in Visio 2013 replaces the **CELLISTHEMED** function from previous versions of Visio.</span></span> 
  
<span data-ttu-id="6c989-113">**ISTHEMED** функция позволяет назначить соответствующие части форматирование темы фигуры, но сохранить возможность переопределить другим частям форматирования с помощью вручную применить форматирование темы.</span><span class="sxs-lookup"><span data-stu-id="6c989-113">The **ISTHEMED** function lets you assign appropriate parts of a theme's formatting to a shape but retain the ability to override other parts of the theme formatting with manually-applied formatting.</span></span> <span data-ttu-id="6c989-114">Если впоследствии применения темы, вручную форматирования имеет преимущество и фигуры принимает все форматирование темы.</span><span class="sxs-lookup"><span data-stu-id="6c989-114">If you subsequently reapply the theme, any manual formatting is overridden and the shape takes on all of the theme's formatting.</span></span> 
  
 <span data-ttu-id="6c989-115">**ISTHEMED** имеет значение TRUE, если ячейка [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) в фигуре больше 0.</span><span class="sxs-lookup"><span data-stu-id="6c989-115">**ISTHEMED** evaluates to TRUE if the [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) cell in the shape is greater than 0.</span></span> <span data-ttu-id="6c989-116">Если эта ячейка равно 0, **ISTHEMED** принимает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="6c989-116">If this cell is equal to 0, then **ISTHEMED** evaluates to FALSE.</span></span> <span data-ttu-id="6c989-117">Темы DocumentSheet и PageSheet не влияет на значение **ISTHEMED** функции, используемые в таблице свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="6c989-117">The theme of the DocumentSheet and PageSheet won't affect the value of the **ISTHEMED** function used in a ShapeSheet.</span></span> <span data-ttu-id="6c989-118">Только в том случае, если функция **ISTHEMED** отображаемым на PageSheet не данному темы страницы.</span><span class="sxs-lookup"><span data-stu-id="6c989-118">Only if the **ISTHEMED** function shows up in the PageSheet does the page's theme matter.</span></span> 
  
## <a name="example"></a><span data-ttu-id="6c989-119">Пример</span><span class="sxs-lookup"><span data-stu-id="6c989-119">Example</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="6c989-120">Cell</span><span class="sxs-lookup"><span data-stu-id="6c989-120">Cell</span></span>  <br/> |<span data-ttu-id="6c989-121">Формула</span><span class="sxs-lookup"><span data-stu-id="6c989-121">Formula</span></span>  <br/> |<span data-ttu-id="6c989-122">Результат</span><span class="sxs-lookup"><span data-stu-id="6c989-122">Result</span></span>  <br/> |
|<span data-ttu-id="6c989-123">Char.Font</span><span class="sxs-lookup"><span data-stu-id="6c989-123">Char.Font</span></span>  <br/> |<span data-ttu-id="6c989-124">IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span><span class="sxs-lookup"><span data-stu-id="6c989-124">IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span></span>  <br/> |<span data-ttu-id="6c989-125">Если фигура имеет темой применяется к нему, текст фигуры принимает параметры темы шрифта.</span><span class="sxs-lookup"><span data-stu-id="6c989-125">If the shape has a themed applied to it, the shape text accepts the font formatting from the theme.</span></span> <span data-ttu-id="6c989-126">Если фигура не является темой, с помощью шрифта «Calibri» форматирования текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="6c989-126">If the shape is not themed, the shape text is formatted with the "Calibri" font.</span></span>  <br/> |
|<span data-ttu-id="6c989-127">Цвет линии</span><span class="sxs-lookup"><span data-stu-id="6c989-127">LineColor</span></span>  <br/> |<span data-ttu-id="6c989-128">ЕСЛИ (ISTHEMED, RGB (255, 0, 0), RGB (0, 255, 0))</span><span class="sxs-lookup"><span data-stu-id="6c989-128">IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))</span></span>  <br/> |<span data-ttu-id="6c989-129">Если фигура имеет темой применяется к нему, красный цвет линии фигуры.</span><span class="sxs-lookup"><span data-stu-id="6c989-129">If the shape has a themed applied to it, the shape's line color is red.</span></span> <span data-ttu-id="6c989-130">Если фигура не является темой, зеленый цвет линии фигуры.</span><span class="sxs-lookup"><span data-stu-id="6c989-130">If the shape is not themed, the shape's line color is green.</span></span>  <br/> |
   

