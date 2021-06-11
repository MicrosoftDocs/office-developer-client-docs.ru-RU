---
title: Функция ISTHEMED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: Возвращает значение Boolean, указывающее, имеет ли фигура примененную к ней тему.
ms.openlocfilehash: 49f53eaaacbdc86a633703d6ef847e38097f5122
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418122"
---
# <a name="isthemed-function"></a><span data-ttu-id="6a8db-103">Функция ISTHEMED</span><span class="sxs-lookup"><span data-stu-id="6a8db-103">ISTHEMED Function</span></span>

<span data-ttu-id="6a8db-104">Возвращает значение Boolean, указывающее, имеет ли фигура примененную к ней тему.</span><span class="sxs-lookup"><span data-stu-id="6a8db-104">Returns a Boolean value indicating whether a shape has a theme applied to it.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="6a8db-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="6a8db-105">Version Information</span></span>

<span data-ttu-id="6a8db-106">Добавлена версия: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="6a8db-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6a8db-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a8db-107">Syntax</span></span>

 <span data-ttu-id="6a8db-108">**ISTHEMED**()</span><span class="sxs-lookup"><span data-stu-id="6a8db-108">**ISTHEMED**()</span></span>
  
## <a name="return-value"></a><span data-ttu-id="6a8db-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6a8db-109">Return value</span></span>

<span data-ttu-id="6a8db-110">Boolean</span><span class="sxs-lookup"><span data-stu-id="6a8db-110">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6a8db-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="6a8db-111">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="6a8db-112">Функция **ISTHEMED** в Visio 2013 заменяет функцию **CELLISTHEMED** от предыдущих версий Visio.</span><span class="sxs-lookup"><span data-stu-id="6a8db-112">The **ISTHEMED** function in Visio 2013 replaces the **CELLISTHEMED** function from previous versions of Visio.</span></span> 
  
<span data-ttu-id="6a8db-113">Функция **ISTHEMED** позволяет назначить соответствующие части форматирования темы фигуре, но сохранит возможность переопределения других частей форматирования темы с помощью ручного форматирования.</span><span class="sxs-lookup"><span data-stu-id="6a8db-113">The **ISTHEMED** function lets you assign appropriate parts of a theme's formatting to a shape but retain the ability to override other parts of the theme formatting with manually-applied formatting.</span></span> <span data-ttu-id="6a8db-114">Если впоследствии вы повторно привнося тему, любое ручное форматирование переопределяется, и фигура принимает все форматирование темы.</span><span class="sxs-lookup"><span data-stu-id="6a8db-114">If you subsequently reapply the theme, any manual formatting is overridden and the shape takes on all of the theme's formatting.</span></span> 
  
 <span data-ttu-id="6a8db-115">**ISTHEMED** оценивает true, если [ячейка ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) в фигуре больше 0.</span><span class="sxs-lookup"><span data-stu-id="6a8db-115">**ISTHEMED** evaluates to TRUE if the [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) cell in the shape is greater than 0.</span></span> <span data-ttu-id="6a8db-116">Если эта ячейка равна 0, **ISTHEMED** оценивается как FALSE.</span><span class="sxs-lookup"><span data-stu-id="6a8db-116">If this cell is equal to 0, then **ISTHEMED** evaluates to FALSE.</span></span> <span data-ttu-id="6a8db-117">Тема таблицы documentSheet и PageSheet не повлияет на значение функции **ISTHEMED,** используемой в ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="6a8db-117">The theme of the DocumentSheet and PageSheet won't affect the value of the **ISTHEMED** function used in a ShapeSheet.</span></span> <span data-ttu-id="6a8db-118">Только если функция **ISTHEMED** появляется на странице PageSheet, тема страницы имеет значение.</span><span class="sxs-lookup"><span data-stu-id="6a8db-118">Only if the **ISTHEMED** function shows up in the PageSheet does the page's theme matter.</span></span> 
  
## <a name="example"></a><span data-ttu-id="6a8db-119">Пример</span><span class="sxs-lookup"><span data-stu-id="6a8db-119">Example</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="6a8db-120">Cell</span><span class="sxs-lookup"><span data-stu-id="6a8db-120">Cell</span></span>  <br/> |<span data-ttu-id="6a8db-121">Формула</span><span class="sxs-lookup"><span data-stu-id="6a8db-121">Formula</span></span>  <br/> |<span data-ttu-id="6a8db-122">Результат</span><span class="sxs-lookup"><span data-stu-id="6a8db-122">Result</span></span>  <br/> |
|<span data-ttu-id="6a8db-123">Char.Font</span><span class="sxs-lookup"><span data-stu-id="6a8db-123">Char.Font</span></span>  <br/> |<span data-ttu-id="6a8db-124">IF (ISTHEMED(), THEMEVAL(), FONT ("Calibri"))</span><span class="sxs-lookup"><span data-stu-id="6a8db-124">IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span></span>  <br/> |<span data-ttu-id="6a8db-125">Если фигура имеет примененную к ней тему, текст формы принимает форматирование шрифта из темы.</span><span class="sxs-lookup"><span data-stu-id="6a8db-125">If the shape has a themed applied to it, the shape text accepts the font formatting from the theme.</span></span> <span data-ttu-id="6a8db-126">Если форма не имеет тематии, текст фигуры форматирован шрифтом "Calibri".</span><span class="sxs-lookup"><span data-stu-id="6a8db-126">If the shape is not themed, the shape text is formatted with the "Calibri" font.</span></span>  <br/> |
|<span data-ttu-id="6a8db-127">LineColor</span><span class="sxs-lookup"><span data-stu-id="6a8db-127">LineColor</span></span>  <br/> |<span data-ttu-id="6a8db-128">IF (ISTHEMED, RGB (255, 0, 0), RGB (0, 255, 0))</span><span class="sxs-lookup"><span data-stu-id="6a8db-128">IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))</span></span>  <br/> |<span data-ttu-id="6a8db-129">Если фигура имеет примененную к ней темную фигуру, то цвет строки — красный.</span><span class="sxs-lookup"><span data-stu-id="6a8db-129">If the shape has a themed applied to it, the shape's line color is red.</span></span> <span data-ttu-id="6a8db-130">Если фигура не имеет темы, то цвет линии фигуры зеленый.</span><span class="sxs-lookup"><span data-stu-id="6a8db-130">If the shape is not themed, the shape's line color is green.</span></span>  <br/> |
   

