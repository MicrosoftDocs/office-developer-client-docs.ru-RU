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
description: Возвращает высоту составного текста в фигуре, где строка без текста не превышает максимумвидс.
ms.openlocfilehash: 7455f58f14f9a4a0ae1fcd5375dba5d5860d3852
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332367"
---
# <a name="textheight-function"></a><span data-ttu-id="1c460-103">Функция TEXTHEIGHT</span><span class="sxs-lookup"><span data-stu-id="1c460-103">TEXTHEIGHT Function</span></span>

<span data-ttu-id="1c460-104">Возвращает высоту составного текста в фигуре, где строка без текста не превышает _максимумвидс_.</span><span class="sxs-lookup"><span data-stu-id="1c460-104">Returns the height of the composed text in a shape where no text line exceeds  _maximumwidth_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1c460-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c460-105">Syntax</span></span>

<span data-ttu-id="1c460-106">TEXTHEIGHT (\* \* *шапенаме! TheText* \* \* \* \* *[, максимумвидс]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="1c460-106">TEXTHEIGHT(\*\* *shapename!TheText* \*\* \*\* *[,maximumwidth]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1c460-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c460-107">Parameters</span></span>

|<span data-ttu-id="1c460-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="1c460-108">**Name**</span></span>|<span data-ttu-id="1c460-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="1c460-109">**Required/Optional**</span></span>|<span data-ttu-id="1c460-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="1c460-110">**Data Type**</span></span>|<span data-ttu-id="1c460-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1c460-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1c460-112">_шапенаме! theText_</span><span class="sxs-lookup"><span data-stu-id="1c460-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="1c460-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1c460-113">Required</span></span>  <br/> |<span data-ttu-id="1c460-114">**String**</span><span class="sxs-lookup"><span data-stu-id="1c460-114">**String**</span></span> <br/> |<span data-ttu-id="1c460-115">Ссылка на ячейку с именем TheText в целевой фигуре.</span><span class="sxs-lookup"><span data-stu-id="1c460-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="1c460-116">_шапенаме!_</span><span class="sxs-lookup"><span data-stu-id="1c460-116">_shapename!_</span></span> <span data-ttu-id="1c460-117">— имя фигуры, из которой требуется получить текст.</span><span class="sxs-lookup"><span data-stu-id="1c460-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="1c460-118">_максимумвидс_</span><span class="sxs-lookup"><span data-stu-id="1c460-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="1c460-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="1c460-119">Optional</span></span>  <br/> |<span data-ttu-id="1c460-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="1c460-120">**Numeric**</span></span> <br/> |<span data-ttu-id="1c460-121">Максимальная ширина блока текста.</span><span class="sxs-lookup"><span data-stu-id="1c460-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="1c460-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c460-122">Return value</span></span>

<span data-ttu-id="1c460-123">Строка</span><span class="sxs-lookup"><span data-stu-id="1c460-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1c460-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c460-124">Remarks</span></span>

<span data-ttu-id="1c460-125">Возвращаемое значение включает высоту текста, включая пробел до и после текста, междустрочный интервал в тексте, а также поля блока верхнего и нижнего текста.</span><span class="sxs-lookup"><span data-stu-id="1c460-125">The returned value includes the height of the text including the space before and after text, the line spacing in text, and the top and bottom text block margins.</span></span> <span data-ttu-id="1c460-126">Эта функция обычно используется для настройки высоты фигуры в соответствии с текстом, который она содержит.</span><span class="sxs-lookup"><span data-stu-id="1c460-126">This function is commonly used to adjust the height of a shape to fit the text it contains.</span></span>
  
## <a name="example"></a><span data-ttu-id="1c460-127">Пример</span><span class="sxs-lookup"><span data-stu-id="1c460-127">Example</span></span>

<span data-ttu-id="1c460-128">TEXTHEIGHT (TheText, (Width-0,5 in))</span><span class="sxs-lookup"><span data-stu-id="1c460-128">TEXTHEIGHT(TheText,(Width - 0.5 in))</span></span> 
  
<span data-ttu-id="1c460-129">Возвращает высоту текста при переносе по ширине фигуры минус 0,5 дюйма.</span><span class="sxs-lookup"><span data-stu-id="1c460-129">Returns the height of the text when wrapped to the width of the shape minus 0.5 inches.</span></span> 
  

