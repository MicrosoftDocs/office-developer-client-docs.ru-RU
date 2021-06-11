---
title: Функция LUM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251460
localization_priority: Normal
ms.assetid: 38e6bba7-1bf2-3d31-0912-707002454f5d
description: Возвращает значение компонента светоносности цвета.
ms.openlocfilehash: 17fa43f8e2cd7422428f92724e351436233c2d62
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419340"
---
# <a name="lum-function"></a><span data-ttu-id="360b0-103">Функция LUM</span><span class="sxs-lookup"><span data-stu-id="360b0-103">LUM Function</span></span>

<span data-ttu-id="360b0-104">Возвращает значение компонента светоносности цвета.</span><span class="sxs-lookup"><span data-stu-id="360b0-104">Returns the value of a color's luminosity component.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="360b0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="360b0-105">Syntax</span></span>

<span data-ttu-id="360b0-106">Выражение LUM(\*\*  \*\* )</span><span class="sxs-lookup"><span data-stu-id="360b0-106">LUM(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="360b0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="360b0-107">Parameters</span></span>

|<span data-ttu-id="360b0-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="360b0-108">**Name**</span></span>|<span data-ttu-id="360b0-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="360b0-109">**Required/Optional**</span></span>|<span data-ttu-id="360b0-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="360b0-110">**Data Type**</span></span>|<span data-ttu-id="360b0-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="360b0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="360b0-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="360b0-112">_expression_</span></span> <br/> |<span data-ttu-id="360b0-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="360b0-113">Required</span></span>  <br/> |<span data-ttu-id="360b0-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="360b0-114">**Numeric**</span></span> <br/> |<span data-ttu-id="360b0-115">Индекс цвета в цветовой таблице документа или ссылка на ячейку с индексом цвета.</span><span class="sxs-lookup"><span data-stu-id="360b0-115">The index of a color in the document's color table, or a reference to a cell that contains a color index.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="360b0-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="360b0-116">Return value</span></span>

<span data-ttu-id="360b0-117">Номер</span><span class="sxs-lookup"><span data-stu-id="360b0-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="360b0-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="360b0-118">Remarks</span></span>

<span data-ttu-id="360b0-119">Возвратное значение — это число в диапазоне от 0 до 240 включительно.</span><span class="sxs-lookup"><span data-stu-id="360b0-119">The return value is a number in the range 0 to 240, inclusive.</span></span> <span data-ttu-id="360b0-120">Функция возвращает 0 для недействительных входных данных.</span><span class="sxs-lookup"><span data-stu-id="360b0-120">The function returns 0 for invalid input.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="360b0-121">Пример 1</span><span class="sxs-lookup"><span data-stu-id="360b0-121">Example 1</span></span>

<span data-ttu-id="360b0-122">LUM(Sheet.4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="360b0-122">LUM(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="360b0-123">Возвращает светоносность цвета на переднем плане заполняемого листа.4.</span><span class="sxs-lookup"><span data-stu-id="360b0-123">Returns the luminosity of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="360b0-124">Пример 2</span><span class="sxs-lookup"><span data-stu-id="360b0-124">Example 2</span></span>

<span data-ttu-id="360b0-125">LUM(6)</span><span class="sxs-lookup"><span data-stu-id="360b0-125">LUM(6)</span></span>
  
<span data-ttu-id="360b0-126">Возвращает 120, если в документе используется Visio цветовая палитра, где пурпурный цвет — это цвет в индексе 6.</span><span class="sxs-lookup"><span data-stu-id="360b0-126">Returns 120 if the document uses the default Visio color palette, where magenta is the color at index 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="360b0-127">Пример 3</span><span class="sxs-lookup"><span data-stu-id="360b0-127">Example 3</span></span>

<span data-ttu-id="360b0-128">LUM(HSL(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="360b0-128">LUM(HSL(10, 20, 30))</span></span>
  
<span data-ttu-id="360b0-129">Возвращает 30.</span><span class="sxs-lookup"><span data-stu-id="360b0-129">Returns 30.</span></span>
  

