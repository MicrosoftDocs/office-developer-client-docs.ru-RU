---
title: Функция BLUE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251402
localization_priority: Normal
ms.assetid: da9fb933-4e2c-3e2a-1879-6e70db0cd830
description: Возвращает синий компонент цвета. Возвращаемая величина — это набор в диапазоне от 0 до 255 включительно. Функция возвращает 0 для недействительных входных данных.
ms.openlocfilehash: adefbe0f8c2df0ead0f3e50cd5d4945501972865
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439039"
---
# <a name="blue-function"></a><span data-ttu-id="056ba-105">Функция BLUE</span><span class="sxs-lookup"><span data-stu-id="056ba-105">BLUE Function</span></span>

<span data-ttu-id="056ba-106">Возвращает синий компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="056ba-106">Returns the blue component of a color.</span></span> <span data-ttu-id="056ba-107">Возвращаемая величина — это набор в диапазоне от 0 до 255 включительно.</span><span class="sxs-lookup"><span data-stu-id="056ba-107">The return value is an integer in the range of 0 to 255, inclusive.</span></span> <span data-ttu-id="056ba-108">Функция возвращает 0 для недействительных входных данных.</span><span class="sxs-lookup"><span data-stu-id="056ba-108">The function returns 0 for invalid input.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="056ba-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="056ba-109">Syntax</span></span>

<span data-ttu-id="056ba-110">BLUE(\*\* *expression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="056ba-110">BLUE(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="056ba-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="056ba-111">Parameters</span></span>

|<span data-ttu-id="056ba-112">**Имя**</span><span class="sxs-lookup"><span data-stu-id="056ba-112">**Name**</span></span>|<span data-ttu-id="056ba-113">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="056ba-113">**Required/Optional**</span></span>|<span data-ttu-id="056ba-114">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="056ba-114">**Data Type**</span></span>|<span data-ttu-id="056ba-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="056ba-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="056ba-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="056ba-116">_expression_</span></span> <br/> |<span data-ttu-id="056ba-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="056ba-117">Required</span></span>  <br/> |<span data-ttu-id="056ba-118">**String**</span><span class="sxs-lookup"><span data-stu-id="056ba-118">**String**</span></span> <br/> |<span data-ttu-id="056ba-119">Индекс цвета в цветной таблице документа, выражение, которое решается на настраиваемый цвет (например, RGB или HSL), или ссылку на ячейку, содержаную цветной индекс или результат цвета.</span><span class="sxs-lookup"><span data-stu-id="056ba-119">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="056ba-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="056ba-120">Return value</span></span>

<span data-ttu-id="056ba-121">Целое число</span><span class="sxs-lookup"><span data-stu-id="056ba-121">Integer</span></span>
  
## <a name="example-1"></a><span data-ttu-id="056ba-122">Пример 1</span><span class="sxs-lookup"><span data-stu-id="056ba-122">Example 1</span></span>

<span data-ttu-id="056ba-123">BLUE (Sheet.4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="056ba-123">BLUE(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="056ba-124">Возвращает синий компонент цвета поля заполняемого поля Sheet.4.</span><span class="sxs-lookup"><span data-stu-id="056ba-124">Returns the blue component of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="056ba-125">Пример 2</span><span class="sxs-lookup"><span data-stu-id="056ba-125">Example 2</span></span>

<span data-ttu-id="056ba-126">BLUE (13)</span><span class="sxs-lookup"><span data-stu-id="056ba-126">BLUE(13)</span></span>
  
<span data-ttu-id="056ba-127">Возвращает 128, если в документе используется Visio цветовая палитра, где cyan — это цвет в индексе 13.</span><span class="sxs-lookup"><span data-stu-id="056ba-127">Returns 128 if the document uses the default Visio color palette, where cyan is the color at index 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="056ba-128">Пример 3</span><span class="sxs-lookup"><span data-stu-id="056ba-128">Example 3</span></span>

<span data-ttu-id="056ba-129">BLUE (RGB(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="056ba-129">BLUE(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="056ba-130">Возвращает 30.</span><span class="sxs-lookup"><span data-stu-id="056ba-130">Returns 30.</span></span>
  

