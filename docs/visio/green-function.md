---
title: Функция GREEN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251434
localization_priority: Normal
ms.assetid: eccec432-32d3-15c2-06b3-dd02b6313d4c
description: Возвращает зеленый компонент цвета.
ms.openlocfilehash: 0412e4519c2964b05d7663805d7773e8dc5deaab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438108"
---
# <a name="green-function"></a><span data-ttu-id="37ff5-103">Функция GREEN</span><span class="sxs-lookup"><span data-stu-id="37ff5-103">GREEN Function</span></span>

<span data-ttu-id="37ff5-104">Возвращает зеленый компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="37ff5-104">Returns the green component of a color.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="37ff5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37ff5-105">Syntax</span></span>

<span data-ttu-id="37ff5-106">ЗЕЛЕНЫЙ (\* \* *выражение* \* \*)</span><span class="sxs-lookup"><span data-stu-id="37ff5-106">GREEN(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="37ff5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="37ff5-107">Parameters</span></span>

|<span data-ttu-id="37ff5-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="37ff5-108">**Name**</span></span>|<span data-ttu-id="37ff5-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="37ff5-109">**Required/Optional**</span></span>|<span data-ttu-id="37ff5-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="37ff5-110">**Data Type**</span></span>|<span data-ttu-id="37ff5-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="37ff5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="37ff5-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="37ff5-112">_expression_</span></span> <br/> |<span data-ttu-id="37ff5-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="37ff5-113">Required</span></span>  <br/> |<span data-ttu-id="37ff5-114">**Разные**</span><span class="sxs-lookup"><span data-stu-id="37ff5-114">**Varies**</span></span> <br/> |<span data-ttu-id="37ff5-115">Индекс цвета в таблице цветов документа, выражение, которое разрешается в настраиваемый цвет (например, RGB или HSL), или ссылка на ячейку, содержащую цветовой индекс или цветовой результат.</span><span class="sxs-lookup"><span data-stu-id="37ff5-115">An index of a color in the document's color table, an expression that resolves to a custom color (such as RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="37ff5-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="37ff5-116">Return value</span></span>

<span data-ttu-id="37ff5-117">Целое число</span><span class="sxs-lookup"><span data-stu-id="37ff5-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="37ff5-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="37ff5-118">Remarks</span></span>

<span data-ttu-id="37ff5-119">Возвращаемое значение — число в диапазоне от 0 до 255 включительно, или ссылку на ячейку, которая разрешается в индекс.</span><span class="sxs-lookup"><span data-stu-id="37ff5-119">The return value is a number in the range 0 to 255, inclusive, or a cell reference that resolves to an index.</span></span> <span data-ttu-id="37ff5-120">Если *выражение* недопустимо, оно возвращает значение 0 (Black).</span><span class="sxs-lookup"><span data-stu-id="37ff5-120">If  *expression*  is invalid, it returns 0 (black).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="37ff5-121">Пример 1</span><span class="sxs-lookup"><span data-stu-id="37ff5-121">Example 1</span></span>

<span data-ttu-id="37ff5-122">ЗЕЛЕНЫЙ (sheet. 4! FillForegnd</span><span class="sxs-lookup"><span data-stu-id="37ff5-122">GREEN(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="37ff5-123">Возвращает зеленый компонент листа Sheet. 4's заливки цветом текста.</span><span class="sxs-lookup"><span data-stu-id="37ff5-123">Returns the green component of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="37ff5-124">Пример 2</span><span class="sxs-lookup"><span data-stu-id="37ff5-124">Example 2</span></span>

<span data-ttu-id="37ff5-125">ЗЕЛЕНЫЙ (11)</span><span class="sxs-lookup"><span data-stu-id="37ff5-125">GREEN(11)</span></span>
  
<span data-ttu-id="37ff5-126">Возвращает 128, если документ использует цветовую палитру Visio по умолчанию, где темно-желтый — цвет с индексом 11.</span><span class="sxs-lookup"><span data-stu-id="37ff5-126">Returns 128 if the document uses the default Visio color palette, where dark yellow is the color at index 11.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="37ff5-127">Пример 3</span><span class="sxs-lookup"><span data-stu-id="37ff5-127">Example 3</span></span>

<span data-ttu-id="37ff5-128">ЗЕЛЕНЫЙ (RGB (10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="37ff5-128">GREEN(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="37ff5-129">Возвращает значение 20.</span><span class="sxs-lookup"><span data-stu-id="37ff5-129">Returns 20.</span></span>
  

