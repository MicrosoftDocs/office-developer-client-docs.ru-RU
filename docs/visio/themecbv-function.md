---
title: Функция THEMECBV
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Возвращает значение RGB или integer, которое представляет индекс в цветовой палитре документа, где цвет (число), переданный в качестве аргумента, был изменен указанным значением оттенка или затенения, сохраненным в параметрах градиента активной темы.
ms.openlocfilehash: 014dc04c5114e296cd2226f3cf04dfb729817578
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429140"
---
# <a name="themecbv-function"></a><span data-ttu-id="1f654-103">Функция THEMECBV</span><span class="sxs-lookup"><span data-stu-id="1f654-103">THEMECBV Function</span></span>

<span data-ttu-id="1f654-104">Возвращает значение RGB или integer, которое представляет индекс в цветовой палитре документа, где цвет (число), переданный в качестве аргумента, был изменен указанным значением оттенка или затенения, сохраненным в параметрах градиента активной темы.</span><span class="sxs-lookup"><span data-stu-id="1f654-104">Returns an RGB value or an integer that represents an index in the document's color palette, where the color (number) passed in as an argument has been modified by the specified tint or shade value stored in the gradient settings of the active theme.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="1f654-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="1f654-105">Version Information</span></span>

<span data-ttu-id="1f654-106">Добавлена версия: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="1f654-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1f654-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f654-107">Syntax</span></span>

 <span data-ttu-id="1f654-108">**THEMECBV**( _цвет,_ _gradient_stop_number)_</span><span class="sxs-lookup"><span data-stu-id="1f654-108">**THEMECBV**( _color_,  _gradient_stop_number_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="1f654-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f654-109">Parameters</span></span>

|<span data-ttu-id="1f654-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="1f654-110">**Name**</span></span>|<span data-ttu-id="1f654-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="1f654-111">**Required/Optional**</span></span>|<span data-ttu-id="1f654-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="1f654-112">**Data Type**</span></span>|<span data-ttu-id="1f654-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1f654-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1f654-114">_color_</span><span class="sxs-lookup"><span data-stu-id="1f654-114">_color_</span></span> <br/> |<span data-ttu-id="1f654-115">Обязательна</span><span class="sxs-lookup"><span data-stu-id="1f654-115">Required</span></span>  <br/> |<span data-ttu-id="1f654-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="1f654-116">**Number**</span></span> <br/> |<span data-ttu-id="1f654-117">Число, представляющее индекс в цветовой палитре документа.</span><span class="sxs-lookup"><span data-stu-id="1f654-117">A number representing an index in the document's color palette.</span></span>  <br/> |
| <span data-ttu-id="1f654-118">_gradient_stop_number_</span><span class="sxs-lookup"><span data-stu-id="1f654-118">_gradient_stop_number_</span></span> <br/> |<span data-ttu-id="1f654-119">Обязательна</span><span class="sxs-lookup"><span data-stu-id="1f654-119">Required</span></span>  <br/> |<span data-ttu-id="1f654-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="1f654-120">**Number**</span></span> <br/> |<span data-ttu-id="1f654-121">Остановка градиента (оттенка или затенения), хранимая в параметрах градиента активной темы для применения к цвету.</span><span class="sxs-lookup"><span data-stu-id="1f654-121">The gradient stop (tint or shade) stored in the gradient settings of the active theme to apply to the color.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="1f654-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1f654-122">Return value</span></span>

 <span data-ttu-id="1f654-123">**Number**</span><span class="sxs-lookup"><span data-stu-id="1f654-123">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1f654-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="1f654-124">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="1f654-125">Функция THEMECBV не делает ничего для цвета, переданного в качестве аргумента, если quickStyle, который назначен фигуре, не имеет градиента.</span><span class="sxs-lookup"><span data-stu-id="1f654-125">The THEMECBV function does nothing to the color passed in as an argument if the QuickStyle that is assigned to the shape does not have a gradient.</span></span> 
  
<span data-ttu-id="1f654-126">Параметры градиента в теме — это ряд проклиненных остановок градиента, соответствующих "осветлке" (оттенку) или "затемнению" (теню).</span><span class="sxs-lookup"><span data-stu-id="1f654-126">The gradient settings in a theme are a series of numbered gradient stops that correspond to a "lightening" (tint) or "darkening" (shade).</span></span> <span data-ttu-id="1f654-127">Эти оттенки и оттенки применяются к базовому цвету для создания эффекта цвета градиента.</span><span class="sxs-lookup"><span data-stu-id="1f654-127">These shades and tints are applied to a base color to create a gradient color effect.</span></span>
  
<span data-ttu-id="1f654-128">Функция **THEMECBV** принимает входные данные цвета и выводит цвет после того, как он был изменен оттенком или оттенком указанной остановки градиента.</span><span class="sxs-lookup"><span data-stu-id="1f654-128">The **THEMECBV** function takes a color input and outputs the color after it has been modified by the tint or shade of the specified gradient stop.</span></span> <span data-ttu-id="1f654-129">Оттенки и оттенки налагаются определением темы, если текущий быстрый стиль содержит заливку градиента.</span><span class="sxs-lookup"><span data-stu-id="1f654-129">The tints and shades come from the theme's definition, if the current quick style contains a gradient fill.</span></span> <span data-ttu-id="1f654-130">Если активный экспресс-стиль не указывает заливку градиента или фигура имеет вид "Нет темы", эта формула просто возвращает цвет, переданный для первого аргумента.</span><span class="sxs-lookup"><span data-stu-id="1f654-130">If the active Quick Style does not specify a gradient fill or the shape is set to No Theme, then this formula simply returns the color that was passed in for the first argument.</span></span> 
  
## <a name="example"></a><span data-ttu-id="1f654-131">Пример</span><span class="sxs-lookup"><span data-stu-id="1f654-131">Example</span></span>

 `THEMECBV(FillForegnd, 5)`
  
<span data-ttu-id="1f654-132">Возвращает цвет, созданный путем применения оттенка или затенения в пятой остановке градиента к цвету, указанному в ячейке **FillForegnd.**</span><span class="sxs-lookup"><span data-stu-id="1f654-132">Returns the color created by applying the tint or shade in the fifth gradient stop of the gradient to the color specified in the **FillForegnd** cell.</span></span> 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
<span data-ttu-id="1f654-133">Возвращает оттенки красного цвета, созданные путем применения второй остановки градиента к базовому цвету красного.</span><span class="sxs-lookup"><span data-stu-id="1f654-133">Returns a shade or tint of red created by applying the second gradient stop to a base color of red.</span></span>
  

