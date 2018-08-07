---
title: Функция TEXTWIDTH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251505
localization_priority: Normal
ms.assetid: a9b8efcf-edc0-ad99-deae-21df16c58807
description: Возвращает ширину текста в фигуре.
ms.openlocfilehash: d96b9489c08ce38205f8e9ad91e361fcb643c39c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815004"
---
# <a name="textwidth-function"></a><span data-ttu-id="20743-103">Функция TEXTWIDTH</span><span class="sxs-lookup"><span data-stu-id="20743-103">TEXTWIDTH Function</span></span>

<span data-ttu-id="20743-104">Возвращает ширину текста в фигуре.</span><span class="sxs-lookup"><span data-stu-id="20743-104">Returns the width of the composed text in a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="20743-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20743-105">Syntax</span></span>

<span data-ttu-id="20743-106">TEXTWIDTH (** указанной фигуре *! TheText* ** ** *[, maximumwidth]* **)</span><span class="sxs-lookup"><span data-stu-id="20743-106">TEXTWIDTH(** *shapename!TheText* ** ** *[,maximumwidth]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="20743-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="20743-107">Parameters</span></span>

|<span data-ttu-id="20743-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="20743-108">**Name**</span></span>|<span data-ttu-id="20743-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="20743-109">**Required/Optional**</span></span>|<span data-ttu-id="20743-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="20743-110">**Data Type**</span></span>|<span data-ttu-id="20743-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="20743-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="20743-112">_указанной фигуре! theText_</span><span class="sxs-lookup"><span data-stu-id="20743-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="20743-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="20743-113">Required</span></span>  <br/> |<span data-ttu-id="20743-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="20743-114">**String**</span></span> <br/> |<span data-ttu-id="20743-115">Ссылка на ячейку с именем TheText в конечную фигуру.</span><span class="sxs-lookup"><span data-stu-id="20743-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="20743-116">_указанной фигуре!_</span><span class="sxs-lookup"><span data-stu-id="20743-116">_shapename!_</span></span> <span data-ttu-id="20743-117">— Это имя фигуры, из которого требуется получить текст.</span><span class="sxs-lookup"><span data-stu-id="20743-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="20743-118">_MaximumWidth_</span><span class="sxs-lookup"><span data-stu-id="20743-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="20743-119">Optional</span><span class="sxs-lookup"><span data-stu-id="20743-119">Optional</span></span>  <br/> |<span data-ttu-id="20743-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="20743-120">**Numeric**</span></span> <br/> |<span data-ttu-id="20743-121">Максимальная ширина блока текста.</span><span class="sxs-lookup"><span data-stu-id="20743-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="20743-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2">Return value</span></span>

<span data-ttu-id="20743-123">Строка</span><span class="sxs-lookup"><span data-stu-id="20743-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="20743-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="20743-124">Remarks</span></span>

<span data-ttu-id="20743-125">Функция TEXTWIDTH обычно используется для настройки ширины фигуры в соответствии с текстом, которые он содержит.</span><span class="sxs-lookup"><span data-stu-id="20743-125">The TEXTWIDTH function is commonly used to adjust the width of a shape to fit the text it contains.</span></span>
  
<span data-ttu-id="20743-126">Если _sheetN!_</span><span class="sxs-lookup"><span data-stu-id="20743-126">If  _sheetN!_</span></span> <span data-ttu-id="20743-127">— Этот параметр опущен, по умолчанию имеет текущей фигуры.</span><span class="sxs-lookup"><span data-stu-id="20743-127">is omitted, the default shape is the current shape.</span></span> 
  
<span data-ttu-id="20743-128">Если указан _maximumwidth_ , результатом будет длинной строки текста, которая помещается в _maximumwidth_.</span><span class="sxs-lookup"><span data-stu-id="20743-128">If  _maximumwidth_ is specified, the result is the longest line of text that fits within  _maximumwidth_.</span></span> <span data-ttu-id="20743-129">Если _maximumwidth_ опущен, результатом будет общая ширина текста.</span><span class="sxs-lookup"><span data-stu-id="20743-129">If  _maximumwidth_ is omitted, the result is the total width of the text.</span></span> 
  
## <a name="example"></a><span data-ttu-id="20743-130">Пример</span><span class="sxs-lookup"><span data-stu-id="20743-130">Example</span></span>

<span data-ttu-id="20743-131">TEXTWIDTH(TheText)</span><span class="sxs-lookup"><span data-stu-id="20743-131">TEXTWIDTH(TheText)</span></span> 
  
<span data-ttu-id="20743-132">Возвращает общее длины текста в текущей форме.</span><span class="sxs-lookup"><span data-stu-id="20743-132">Returns the total length of the text in the current shape.</span></span> 
  

