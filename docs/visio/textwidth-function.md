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
description: Возвращает ширину составленного текста в форме.
ms.openlocfilehash: 43848bba4d24a0c31a3a084d123cd56140bf0709
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422035"
---
# <a name="textwidth-function"></a><span data-ttu-id="96ef4-103">Функция TEXTWIDTH</span><span class="sxs-lookup"><span data-stu-id="96ef4-103">TEXTWIDTH Function</span></span>

<span data-ttu-id="96ef4-104">Возвращает ширину составленного текста в форме.</span><span class="sxs-lookup"><span data-stu-id="96ef4-104">Returns the width of the composed text in a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="96ef4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96ef4-105">Syntax</span></span>

<span data-ttu-id="96ef4-106">TEXTWIDTH(\*\* *shapename! TheText* \*\* \*\* *[,maximumwidth]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="96ef4-106">TEXTWIDTH(\*\* *shapename!TheText* \*\* \*\* *[,maximumwidth]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="96ef4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="96ef4-107">Parameters</span></span>

|<span data-ttu-id="96ef4-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="96ef4-108">**Name**</span></span>|<span data-ttu-id="96ef4-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="96ef4-109">**Required/Optional**</span></span>|<span data-ttu-id="96ef4-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="96ef4-110">**Data Type**</span></span>|<span data-ttu-id="96ef4-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="96ef4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="96ef4-112">_shapename!theText_</span><span class="sxs-lookup"><span data-stu-id="96ef4-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="96ef4-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="96ef4-113">Required</span></span>  <br/> |<span data-ttu-id="96ef4-114">**String**</span><span class="sxs-lookup"><span data-stu-id="96ef4-114">**String**</span></span> <br/> |<span data-ttu-id="96ef4-115">Ссылка на ячейку с именем TheText в целевой форме.</span><span class="sxs-lookup"><span data-stu-id="96ef4-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="96ef4-116">_shapename!_</span><span class="sxs-lookup"><span data-stu-id="96ef4-116">_shapename!_</span></span> <span data-ttu-id="96ef4-117">это имя фигуры, из которой нужно получить текст.</span><span class="sxs-lookup"><span data-stu-id="96ef4-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="96ef4-118">_maximumwidth_</span><span class="sxs-lookup"><span data-stu-id="96ef4-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="96ef4-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="96ef4-119">Optional</span></span>  <br/> |<span data-ttu-id="96ef4-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="96ef4-120">**Numeric**</span></span> <br/> |<span data-ttu-id="96ef4-121">Максимальная ширина текстового блока.</span><span class="sxs-lookup"><span data-stu-id="96ef4-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="96ef4-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96ef4-122">Return value</span></span>

<span data-ttu-id="96ef4-123">String</span><span class="sxs-lookup"><span data-stu-id="96ef4-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="96ef4-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="96ef4-124">Remarks</span></span>

<span data-ttu-id="96ef4-125">Функция TEXTWIDTH обычно используется для настройки ширины фигуры, чтобы соответствовать тексту, который она содержит.</span><span class="sxs-lookup"><span data-stu-id="96ef4-125">The TEXTWIDTH function is commonly used to adjust the width of a shape to fit the text it contains.</span></span>
  
<span data-ttu-id="96ef4-126">Если  _sheetN!_</span><span class="sxs-lookup"><span data-stu-id="96ef4-126">If  _sheetN!_</span></span> <span data-ttu-id="96ef4-127">опущен, фигура по умолчанию — это текущая форма.</span><span class="sxs-lookup"><span data-stu-id="96ef4-127">is omitted, the default shape is the current shape.</span></span> 
  
<span data-ttu-id="96ef4-128">Если _задано_ максимальное значение, результат — это самая длинная строка текста, которая соответствует _максимальному объему._</span><span class="sxs-lookup"><span data-stu-id="96ef4-128">If  _maximumwidth_ is specified, the result is the longest line of text that fits within  _maximumwidth_.</span></span> <span data-ttu-id="96ef4-129">Если  _значение maximumwidth_ пропущено, результатом является общая ширина текста.</span><span class="sxs-lookup"><span data-stu-id="96ef4-129">If  _maximumwidth_ is omitted, the result is the total width of the text.</span></span> 
  
## <a name="example"></a><span data-ttu-id="96ef4-130">Пример</span><span class="sxs-lookup"><span data-stu-id="96ef4-130">Example</span></span>

<span data-ttu-id="96ef4-131">TEXTWIDTH (TheText)</span><span class="sxs-lookup"><span data-stu-id="96ef4-131">TEXTWIDTH(TheText)</span></span> 
  
<span data-ttu-id="96ef4-132">Возвращает общую длину текста в текущей форме.</span><span class="sxs-lookup"><span data-stu-id="96ef4-132">Returns the total length of the text in the current shape.</span></span> 
  

