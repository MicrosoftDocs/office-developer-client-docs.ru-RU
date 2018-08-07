---
title: Функция TEXTHEIGHT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251504
localization_priority: Normal
ms.assetid: 5a10892f-c8fa-c127-2f5a-564009ce5411
description: Возвращает высоту текста в фигуры, где в строке не превышает maximumwidth.
ms.openlocfilehash: 9a80dafcf80a1dcba968a0f60465aae4e2a2758b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815006"
---
# <a name="textheight-function"></a><span data-ttu-id="58b9c-103">Функция TEXTHEIGHT</span><span class="sxs-lookup"><span data-stu-id="58b9c-103">TEXTHEIGHT Function</span></span>

<span data-ttu-id="58b9c-104">Возвращает высоту текста в фигуры, где в строке не превышает _maximumwidth_.</span><span class="sxs-lookup"><span data-stu-id="58b9c-104">Returns the height of the composed text in a shape where no text line exceeds  _maximumwidth_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="58b9c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58b9c-105">Syntax</span></span>

<span data-ttu-id="58b9c-106">TEXTHEIGHT (** указанной фигуре *! TheText* ** ** *[, maximumwidth]* **)</span><span class="sxs-lookup"><span data-stu-id="58b9c-106">TEXTHEIGHT(** *shapename!TheText* ** ** *[,maximumwidth]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="58b9c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="58b9c-107">Parameters</span></span>

|<span data-ttu-id="58b9c-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="58b9c-108">**Name**</span></span>|<span data-ttu-id="58b9c-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="58b9c-109">**Required/Optional**</span></span>|<span data-ttu-id="58b9c-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="58b9c-110">**Data Type**</span></span>|<span data-ttu-id="58b9c-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="58b9c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="58b9c-112">_указанной фигуре! theText_</span><span class="sxs-lookup"><span data-stu-id="58b9c-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="58b9c-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="58b9c-113">Required</span></span>  <br/> |<span data-ttu-id="58b9c-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="58b9c-114">**String**</span></span> <br/> |<span data-ttu-id="58b9c-115">Ссылка на ячейку с именем TheText в конечную фигуру.</span><span class="sxs-lookup"><span data-stu-id="58b9c-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="58b9c-116">_указанной фигуре!_</span><span class="sxs-lookup"><span data-stu-id="58b9c-116">_shapename!_</span></span> <span data-ttu-id="58b9c-117">— Это имя фигуры, из которого требуется получить текст.</span><span class="sxs-lookup"><span data-stu-id="58b9c-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="58b9c-118">_MaximumWidth_</span><span class="sxs-lookup"><span data-stu-id="58b9c-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="58b9c-119">Optional</span><span class="sxs-lookup"><span data-stu-id="58b9c-119">Optional</span></span>  <br/> |<span data-ttu-id="58b9c-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="58b9c-120">**Numeric**</span></span> <br/> |<span data-ttu-id="58b9c-121">Максимальная ширина блока текста.</span><span class="sxs-lookup"><span data-stu-id="58b9c-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="58b9c-122">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="58b9c-122">Return value</span></span>

<span data-ttu-id="58b9c-123">Строка</span><span class="sxs-lookup"><span data-stu-id="58b9c-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="58b9c-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="58b9c-124">Remarks</span></span>

<span data-ttu-id="58b9c-125">Возвращаемое значение включает в себя высота текста, включая пробел до и после текста, междустрочным интервалом в текст и верхние и нижние поля блока текста.</span><span class="sxs-lookup"><span data-stu-id="58b9c-125">The returned value includes the height of the text including the space before and after text, the line spacing in text, and the top and bottom text block margins.</span></span> <span data-ttu-id="58b9c-126">Эта функция обычно используется для настройки высоты фигуры в соответствии с текстом, которые он содержит.</span><span class="sxs-lookup"><span data-stu-id="58b9c-126">This function is commonly used to adjust the height of a shape to fit the text it contains.</span></span>
  
## <a name="example"></a><span data-ttu-id="58b9c-127">Пример</span><span class="sxs-lookup"><span data-stu-id="58b9c-127">Example</span></span>

<span data-ttu-id="58b9c-128">TEXTHEIGHT (TheText, (ширина - 0,5))</span><span class="sxs-lookup"><span data-stu-id="58b9c-128">TEXTHEIGHT(TheText,(Width - 0.5 in))</span></span> 
  
<span data-ttu-id="58b9c-129">Возвращает высоту текста при переносятся ширину фигуры минус 0,5 дюйма.</span><span class="sxs-lookup"><span data-stu-id="58b9c-129">Returns the height of the text when wrapped to the width of the shape minus 0.5 inches.</span></span> 
  

