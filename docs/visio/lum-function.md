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
description: Возвращает значение компонента яркости цвета.
ms.openlocfilehash: 9c9594aff0149a54d7faacdf8295e6c214c43348
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814187"
---
# <a name="lum-function"></a><span data-ttu-id="16a43-103">Функция LUM</span><span class="sxs-lookup"><span data-stu-id="16a43-103">LUM Function</span></span>

<span data-ttu-id="16a43-104">Возвращает значение компонента яркости цвета.</span><span class="sxs-lookup"><span data-stu-id="16a43-104">Returns the value of a color's luminosity component.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="16a43-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16a43-105">Syntax</span></span>

<span data-ttu-id="16a43-106">Яркость (** *выражение* **)</span><span class="sxs-lookup"><span data-stu-id="16a43-106">LUM(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="16a43-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="16a43-107">Parameters</span></span>

|<span data-ttu-id="16a43-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="16a43-108">**Name**</span></span>|<span data-ttu-id="16a43-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="16a43-109">**Required/Optional**</span></span>|<span data-ttu-id="16a43-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="16a43-110">**Data Type**</span></span>|<span data-ttu-id="16a43-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="16a43-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="16a43-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="16a43-112">_expression_</span></span> <br/> |<span data-ttu-id="16a43-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="16a43-113">Required</span></span>  <br/> |<span data-ttu-id="16a43-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="16a43-114">**Numeric**</span></span> <br/> |<span data-ttu-id="16a43-115">Индекс цвета в таблице цветов документа или ссылка на ячейку, которая содержит индекс цвета.</span><span class="sxs-lookup"><span data-stu-id="16a43-115">The index of a color in the document's color table, or a reference to a cell that contains a color index.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="16a43-116">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="16a43-116">Return value</span></span>

<span data-ttu-id="16a43-117">Number</span><span class="sxs-lookup"><span data-stu-id="16a43-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="16a43-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="16a43-118">Remarks</span></span>

<span data-ttu-id="16a43-119">Возвращаемое значение — число в диапазоне от 0 до 240 включительно.</span><span class="sxs-lookup"><span data-stu-id="16a43-119">The return value is a number in the range 0 to 240, inclusive.</span></span> <span data-ttu-id="16a43-120">Функция возвращает 0 для недопустимые данные.</span><span class="sxs-lookup"><span data-stu-id="16a43-120">The function returns 0 for invalid input.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="16a43-121">Пример 1</span><span class="sxs-lookup"><span data-stu-id="16a43-121">Example 1</span></span>

<span data-ttu-id="16a43-122">Яркость (Sheet.4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="16a43-122">LUM(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="16a43-123">Возвращает яркость цвет заливки Sheet. 4.</span><span class="sxs-lookup"><span data-stu-id="16a43-123">Returns the luminosity of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="16a43-124">Пример 2</span><span class="sxs-lookup"><span data-stu-id="16a43-124">Example 2</span></span>

<span data-ttu-id="16a43-125">LUM(6)</span><span class="sxs-lookup"><span data-stu-id="16a43-125">LUM(6)</span></span>
  
<span data-ttu-id="16a43-126">Возвращает 120, если в документе используется по умолчанию Visio цветовой палитры, в котором пурпурный цвет по индексу 6.</span><span class="sxs-lookup"><span data-stu-id="16a43-126">Returns 120 if the document uses the default Visio color palette, where magenta is the color at index 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="16a43-127">Пример 3</span><span class="sxs-lookup"><span data-stu-id="16a43-127">Example 3</span></span>

<span data-ttu-id="16a43-128">ЯРКОСТЬ (HSL (10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="16a43-128">LUM(HSL(10, 20, 30))</span></span>
  
<span data-ttu-id="16a43-129">Возвращает 30.</span><span class="sxs-lookup"><span data-stu-id="16a43-129">Returns 30.</span></span>
  

