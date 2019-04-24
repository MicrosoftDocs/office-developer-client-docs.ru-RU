---
title: Функция ISTHEMED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Возвращает логическое значение, указывающее, применена ли к фигуре тема.
ms.openlocfilehash: 49f53eaaacbdc86a633703d6ef847e38097f5122
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357514"
---
# <a name="isthemed-function"></a><span data-ttu-id="462d3-103">Функция ISTHEMED</span><span class="sxs-lookup"><span data-stu-id="462d3-103">ISTHEMED Function</span></span>

<span data-ttu-id="462d3-104">Возвращает логическое значение, указывающее, применена ли к фигуре тема.</span><span class="sxs-lookup"><span data-stu-id="462d3-104">Returns a Boolean value indicating whether a shape has a theme applied to it.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="462d3-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="462d3-105">Version Information</span></span>

<span data-ttu-id="462d3-106">Добавлена версия: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="462d3-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="462d3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="462d3-107">Syntax</span></span>

 <span data-ttu-id="462d3-108">\*\*\*\* С учетом ()</span><span class="sxs-lookup"><span data-stu-id="462d3-108">**ISTHEMED**()</span></span>
  
## <a name="return-value"></a><span data-ttu-id="462d3-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="462d3-109">Return value</span></span>

<span data-ttu-id="462d3-110">Boolean</span><span class="sxs-lookup"><span data-stu-id="462d3-110">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="462d3-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="462d3-111">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="462d3-112">Функция \*\*\*\* Целлиссемед в Visio 2013 заменяет функцию \*\*\*\* из предыдущих версий Visio.</span><span class="sxs-lookup"><span data-stu-id="462d3-112">The **ISTHEMED** function in Visio 2013 replaces the **CELLISTHEMED** function from previous versions of Visio.</span></span> 
  
<span data-ttu-id="462d3-113">Функция \*\*\*\* "вопорции" позволяет назначать подходящие части форматирования темы фигуре, но сохранять возможность переопределения других частей форматирования темы с форматированием, примененным вручную.</span><span class="sxs-lookup"><span data-stu-id="462d3-113">The **ISTHEMED** function lets you assign appropriate parts of a theme's formatting to a shape but retain the ability to override other parts of the theme formatting with manually-applied formatting.</span></span> <span data-ttu-id="462d3-114">При повторном применении темы любое ручное форматирование переопределяется, а фигура принимает все форматирование темы.</span><span class="sxs-lookup"><span data-stu-id="462d3-114">If you subsequently reapply the theme, any manual formatting is overridden and the shape takes on all of the theme's formatting.</span></span> 
  
 <span data-ttu-id="462d3-115">\*\*\*\* ВОЗВРАЩАЕТ значение true, если ячейка [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) в фигуре больше 0.</span><span class="sxs-lookup"><span data-stu-id="462d3-115">**ISTHEMED** evaluates to TRUE if the [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) cell in the shape is greater than 0.</span></span> <span data-ttu-id="462d3-116">Если ячейка равна 0, то выдается значение FALSE. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="462d3-116">If this cell is equal to 0, then **ISTHEMED** evaluates to FALSE.</span></span> <span data-ttu-id="462d3-117">Тема DocumentSheet и PageSheet не влияет на значение функции, используемой \*\*\*\* в таблице свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="462d3-117">The theme of the DocumentSheet and PageSheet won't affect the value of the **ISTHEMED** function used in a ShapeSheet.</span></span> <span data-ttu-id="462d3-118">Только в том \*\*\*\* случае, если функция PageSheet содержит тему страницы.</span><span class="sxs-lookup"><span data-stu-id="462d3-118">Only if the **ISTHEMED** function shows up in the PageSheet does the page's theme matter.</span></span> 
  
## <a name="example"></a><span data-ttu-id="462d3-119">Пример</span><span class="sxs-lookup"><span data-stu-id="462d3-119">Example</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="462d3-120">Cell</span><span class="sxs-lookup"><span data-stu-id="462d3-120">Cell</span></span>  <br/> |<span data-ttu-id="462d3-121">Формула</span><span class="sxs-lookup"><span data-stu-id="462d3-121">Formula</span></span>  <br/> |<span data-ttu-id="462d3-122">Результат</span><span class="sxs-lookup"><span data-stu-id="462d3-122">Result</span></span>  <br/> |
|<span data-ttu-id="462d3-123">Char. Font</span><span class="sxs-lookup"><span data-stu-id="462d3-123">Char.Font</span></span>  <br/> |<span data-ttu-id="462d3-124">Если (in (), THEMEVAL (), FONT ("Calibri"))</span><span class="sxs-lookup"><span data-stu-id="462d3-124">IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span></span>  <br/> |<span data-ttu-id="462d3-125">Если к фигуре применены темы, текст фигуры принимает форматирование шрифта из темы.</span><span class="sxs-lookup"><span data-stu-id="462d3-125">If the shape has a themed applied to it, the shape text accepts the font formatting from the theme.</span></span> <span data-ttu-id="462d3-126">Если фигура не имеет темы, текст фигуры форматируется с использованием шрифта "Calibri".</span><span class="sxs-lookup"><span data-stu-id="462d3-126">If the shape is not themed, the shape text is formatted with the "Calibri" font.</span></span>  <br/> |
|<span data-ttu-id="462d3-127">LineColor</span><span class="sxs-lookup"><span data-stu-id="462d3-127">LineColor</span></span>  <br/> |<span data-ttu-id="462d3-128">IF (IN, RGB (255, 0, 0), RGB (0, 255, 0))</span><span class="sxs-lookup"><span data-stu-id="462d3-128">IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))</span></span>  <br/> |<span data-ttu-id="462d3-129">Если к фигуре применены темы, то цвет линии фигуры — красный.</span><span class="sxs-lookup"><span data-stu-id="462d3-129">If the shape has a themed applied to it, the shape's line color is red.</span></span> <span data-ttu-id="462d3-130">Если фигура не имеет темы, то цвет линии фигуры — зеленый.</span><span class="sxs-lookup"><span data-stu-id="462d3-130">If the shape is not themed, the shape's line color is green.</span></span>  <br/> |
   

