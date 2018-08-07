---
title: Функция RED
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251487
localization_priority: Normal
ms.assetid: a95fd86d-ebc1-66b6-e7d9-9c8ea84d23ab
description: Возвращает значение красного компонента цвета.
ms.openlocfilehash: 801ebb64564df81f72c41cb720fe53f0f1b4c10d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19814523"
---
# <a name="red-function"></a><span data-ttu-id="ceb35-103">Функция RED</span><span class="sxs-lookup"><span data-stu-id="ceb35-103">RED Function</span></span>

<span data-ttu-id="ceb35-104">Возвращает значение красного компонента цвета.</span><span class="sxs-lookup"><span data-stu-id="ceb35-104">Returns the red component of a color.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ceb35-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ceb35-105">Syntax</span></span>

<span data-ttu-id="ceb35-106">КРАСНЫЙ (** *выражение* **)</span><span class="sxs-lookup"><span data-stu-id="ceb35-106">RED(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ceb35-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ceb35-107">Parameters</span></span>

|<span data-ttu-id="ceb35-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ceb35-108">**Name**</span></span>|<span data-ttu-id="ceb35-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="ceb35-109">**Required/Optional**</span></span>|<span data-ttu-id="ceb35-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="ceb35-110">**Data Type**</span></span>|<span data-ttu-id="ceb35-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ceb35-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ceb35-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="ceb35-112">_expression_</span></span> <br/> |<span data-ttu-id="ceb35-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ceb35-113">Required</span></span>  <br/> |<span data-ttu-id="ceb35-114">**Разные**</span><span class="sxs-lookup"><span data-stu-id="ceb35-114">**Varies**</span></span> <br/> |<span data-ttu-id="ceb35-115">Индекс цвета в таблице цветов документа, выражение, которое разрешается в настраиваемый цвет (например, RGB или HSL) или ссылку на ячейку, содержащую цвет индекса или цветовой результатов.</span><span class="sxs-lookup"><span data-stu-id="ceb35-115">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ceb35-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6">Return value</span></span>

<span data-ttu-id="ceb35-117">Number</span><span class="sxs-lookup"><span data-stu-id="ceb35-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ceb35-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="ceb35-118">Remarks</span></span>

<span data-ttu-id="ceb35-119">Возвращаемое значение — это число в диапазоне от 0 до 255 включительно, или ссылка на ячейку, которая разрешается в индекс.</span><span class="sxs-lookup"><span data-stu-id="ceb35-119">The return value is a number in the range 0 to 255, inclusive, or a cell reference that resolves to an index.</span></span> <span data-ttu-id="ceb35-120">Если _выражение_ является недопустимым, эта функция возвращает 0 (черный цвет).</span><span class="sxs-lookup"><span data-stu-id="ceb35-120">If  _expression_ is invalid, this function returns 0 (black).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="ceb35-121">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ceb35-121">Example 1</span></span>

<span data-ttu-id="ceb35-122">RED(22)</span><span class="sxs-lookup"><span data-stu-id="ceb35-122">RED(22)</span></span>
  
<span data-ttu-id="ceb35-123">Возвращает 51, если в документе используется по умолчанию Microsoft Office Visio цветовой палитры, в котором темно-серый цвет по индексу 22.</span><span class="sxs-lookup"><span data-stu-id="ceb35-123">Returns 51 if the document uses the default Microsoft Office Visio color palette, where dark gray is the color at index 22.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ceb35-124">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ceb35-124">Example 2</span></span>

<span data-ttu-id="ceb35-125">Red(char.Color)</span><span class="sxs-lookup"><span data-stu-id="ceb35-125">RED(Char.Color)</span></span>
  
<span data-ttu-id="ceb35-126">Возвращает значение красного компонента текущий цвет шрифта.</span><span class="sxs-lookup"><span data-stu-id="ceb35-126">Returns the value of the red component of the current font color.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ceb35-127">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ceb35-127">Example 3</span></span>

<span data-ttu-id="ceb35-128">КРАСНЫЙ (RGB (10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="ceb35-128">RED(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="ceb35-129">Возвращает значение 10.</span><span class="sxs-lookup"><span data-stu-id="ceb35-129">Returns 10.</span></span>
  

