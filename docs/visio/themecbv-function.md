---
title: Функция THEMECBV
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: Возвращает значение RGB или целое число, представляющее индекс в документе цветовой палитры, в которых был изменен цвет (число), переданной в качестве аргумента по указанному значению tint или тень, хранящиеся в параметры градиента активной темы.
ms.openlocfilehash: 878da505a840234445d3e16d3b8a68e31eaf5fda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815026"
---
# <a name="themecbv-function"></a><span data-ttu-id="7ea3a-103">Функция THEMECBV</span><span class="sxs-lookup"><span data-stu-id="7ea3a-103">THEMECBV Function</span></span>

<span data-ttu-id="7ea3a-104">Возвращает значение RGB или целое число, представляющее индекс в документе цветовой палитры, в которых был изменен цвет (число), переданной в качестве аргумента по указанному значению tint или тень, хранящиеся в параметры градиента активной темы.</span><span class="sxs-lookup"><span data-stu-id="7ea3a-104">Returns an RGB value or an integer that represents an index in the document's color palette, where the color (number) passed in as an argument has been modified by the specified tint or shade value stored in the gradient settings of the active theme.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="7ea3a-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="7ea3a-105">Version Information</span></span>

<span data-ttu-id="7ea3a-106">Добавлена версия: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="7ea3a-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7ea3a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ea3a-107">Syntax</span></span>

 <span data-ttu-id="7ea3a-108">**THEMECBV** ( _цвет_, _gradient_stop_number_)</span><span class="sxs-lookup"><span data-stu-id="7ea3a-108">**THEMECBV**( _color_,  _gradient_stop_number_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="7ea3a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ea3a-109">Parameters</span></span>

|<span data-ttu-id="7ea3a-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="7ea3a-110">**Name**</span></span>|<span data-ttu-id="7ea3a-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="7ea3a-111">**Required/Optional**</span></span>|<span data-ttu-id="7ea3a-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="7ea3a-112">**Data Type**</span></span>|<span data-ttu-id="7ea3a-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7ea3a-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7ea3a-114">_Цвет_</span><span class="sxs-lookup"><span data-stu-id="7ea3a-114">_color_</span></span> <br/> |<span data-ttu-id="7ea3a-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7ea3a-115">Required</span></span>  <br/> |<span data-ttu-id="7ea3a-116">**Число**</span><span class="sxs-lookup"><span data-stu-id="7ea3a-116">**Number**</span></span> <br/> |<span data-ttu-id="7ea3a-117">Число, представляющее индекса в документе цветовой палитры.</span><span class="sxs-lookup"><span data-stu-id="7ea3a-117">A number representing an index in the document's color palette.</span></span>  <br/> |
| <span data-ttu-id="7ea3a-118">_gradient_stop_number_</span><span class="sxs-lookup"><span data-stu-id="7ea3a-118">_gradient_stop_number_</span></span> <br/> |<span data-ttu-id="7ea3a-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7ea3a-119">Required</span></span>  <br/> |<span data-ttu-id="7ea3a-120">**Число**</span><span class="sxs-lookup"><span data-stu-id="7ea3a-120">**Number**</span></span> <br/> |<span data-ttu-id="7ea3a-121">Градиента (tint или тень) хранятся в параметры градиента активной темы для применения к цвет.</span><span class="sxs-lookup"><span data-stu-id="7ea3a-121">The gradient stop (tint or shade) stored in the gradient settings of the active theme to apply to the color.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="7ea3a-122">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="7ea3a-122">Return value</span></span>

 <span data-ttu-id="7ea3a-123">**Число**</span><span class="sxs-lookup"><span data-stu-id="7ea3a-123">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7ea3a-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="7ea3a-124">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="7ea3a-125">Функция THEMECBV не выполняет никаких действий на цвет, переданное как аргумент Если QuickStyle, назначенная фигуры не имеет градиент.</span><span class="sxs-lookup"><span data-stu-id="7ea3a-125">The THEMECBV function does nothing to the color passed in as an argument if the QuickStyle that is assigned to the shape does not have a gradient.</span></span> 
  
<span data-ttu-id="7ea3a-126">Параметры градиента в теме — это серии нумерованный градиента, которые соответствуют «осветляющего» (tint) или «затемняющего» (тень).</span><span class="sxs-lookup"><span data-stu-id="7ea3a-126">The gradient settings in a theme are a series of numbered gradient stops that correspond to a "lightening" (tint) or "darkening" (shade).</span></span> <span data-ttu-id="7ea3a-127">Эти тени и оттенки применяются к основной цвет для создания эффекта градиента.</span><span class="sxs-lookup"><span data-stu-id="7ea3a-127">These shades and tints are applied to a base color to create a gradient color effect.</span></span>
  
<span data-ttu-id="7ea3a-128">Функция **THEMECBV** принимает ввод цвета и выводит цвет после изменения с помощью tint или тень указанного градиента.</span><span class="sxs-lookup"><span data-stu-id="7ea3a-128">The **THEMECBV** function takes a color input and outputs the color after it has been modified by the tint or shade of the specified gradient stop.</span></span> <span data-ttu-id="7ea3a-129">Оттенки и тени поступают из определения темы, если текущий экспресс-стилей содержит градиентной заливки.</span><span class="sxs-lookup"><span data-stu-id="7ea3a-129">The tints and shades come from the theme's definition, if the current quick style contains a gradient fill.</span></span> <span data-ttu-id="7ea3a-130">Если active экспресс-стилей не определяет, что градиентной заливки или фигуры задано значение Нет темы, эту формулу просто возвращает цвета, которое было передано в качестве первого аргумента.</span><span class="sxs-lookup"><span data-stu-id="7ea3a-130">If the active Quick Style does not specify a gradient fill or the shape is set to No Theme, then this formula simply returns the color that was passed in for the first argument.</span></span> 
  
## <a name="example"></a><span data-ttu-id="7ea3a-131">Пример</span><span class="sxs-lookup"><span data-stu-id="7ea3a-131">Example</span></span>

 `THEMECBV(FillForegnd, 5)`
  
<span data-ttu-id="7ea3a-132">Возвращает цвет, с помощью tint или тень в пятый градиента градиента цвет, определенный в ячейке **FillForegnd** .</span><span class="sxs-lookup"><span data-stu-id="7ea3a-132">Returns the color created by applying the tint or shade in the fifth gradient stop of the gradient to the color specified in the **FillForegnd** cell.</span></span> 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
<span data-ttu-id="7ea3a-133">Возвращает тень или tint красного, с помощью второй градиента основной цвет красный.</span><span class="sxs-lookup"><span data-stu-id="7ea3a-133">Returns a shade or tint of red created by applying the second gradient stop to a base color of red.</span></span>
  

