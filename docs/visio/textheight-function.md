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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427411"
---
# <a name="textheight-function"></a><span data-ttu-id="60d32-103">Функция TEXTHEIGHT</span><span class="sxs-lookup"><span data-stu-id="60d32-103">TEXTHEIGHT Function</span></span>

<span data-ttu-id="60d32-104">Возвращает высоту составного текста в фигуре, где строка без текста не превышает _максимумвидс_.</span><span class="sxs-lookup"><span data-stu-id="60d32-104">Returns the height of the composed text in a shape where no text line exceeds  _maximumwidth_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="60d32-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60d32-105">Syntax</span></span>

<span data-ttu-id="60d32-106">TEXTHEIGHT (\* \* *шапенаме! TheText* \* \* \* \* *[, максимумвидс]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="60d32-106">TEXTHEIGHT(\*\* *shapename!TheText* \*\* \*\* *[,maximumwidth]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="60d32-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="60d32-107">Parameters</span></span>

|<span data-ttu-id="60d32-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="60d32-108">**Name**</span></span>|<span data-ttu-id="60d32-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="60d32-109">**Required/Optional**</span></span>|<span data-ttu-id="60d32-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="60d32-110">**Data Type**</span></span>|<span data-ttu-id="60d32-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="60d32-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="60d32-112">_шапенаме! theText_</span><span class="sxs-lookup"><span data-stu-id="60d32-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="60d32-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="60d32-113">Required</span></span>  <br/> |<span data-ttu-id="60d32-114">**String**</span><span class="sxs-lookup"><span data-stu-id="60d32-114">**String**</span></span> <br/> |<span data-ttu-id="60d32-115">Ссылка на ячейку с именем TheText в целевой фигуре.</span><span class="sxs-lookup"><span data-stu-id="60d32-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="60d32-116">_шапенаме!_</span><span class="sxs-lookup"><span data-stu-id="60d32-116">_shapename!_</span></span> <span data-ttu-id="60d32-117">— имя фигуры, из которой требуется получить текст.</span><span class="sxs-lookup"><span data-stu-id="60d32-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="60d32-118">_максимумвидс_</span><span class="sxs-lookup"><span data-stu-id="60d32-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="60d32-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="60d32-119">Optional</span></span>  <br/> |<span data-ttu-id="60d32-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="60d32-120">**Numeric**</span></span> <br/> |<span data-ttu-id="60d32-121">Максимальная ширина блока текста.</span><span class="sxs-lookup"><span data-stu-id="60d32-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="60d32-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60d32-122">Return value</span></span>

<span data-ttu-id="60d32-123">String</span><span class="sxs-lookup"><span data-stu-id="60d32-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="60d32-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="60d32-124">Remarks</span></span>

<span data-ttu-id="60d32-125">Возвращаемое значение включает высоту текста, включая пробел до и после текста, междустрочный интервал в тексте, а также поля блока верхнего и нижнего текста.</span><span class="sxs-lookup"><span data-stu-id="60d32-125">The returned value includes the height of the text including the space before and after text, the line spacing in text, and the top and bottom text block margins.</span></span> <span data-ttu-id="60d32-126">Эта функция обычно используется для настройки высоты фигуры в соответствии с текстом, который она содержит.</span><span class="sxs-lookup"><span data-stu-id="60d32-126">This function is commonly used to adjust the height of a shape to fit the text it contains.</span></span>
  
## <a name="example"></a><span data-ttu-id="60d32-127">Пример</span><span class="sxs-lookup"><span data-stu-id="60d32-127">Example</span></span>

<span data-ttu-id="60d32-128">TEXTHEIGHT (TheText, (Width-0,5 in))</span><span class="sxs-lookup"><span data-stu-id="60d32-128">TEXTHEIGHT(TheText,(Width - 0.5 in))</span></span> 
  
<span data-ttu-id="60d32-129">Возвращает высоту текста при переносе по ширине фигуры минус 0,5 дюйма.</span><span class="sxs-lookup"><span data-stu-id="60d32-129">Returns the height of the text when wrapped to the width of the shape minus 0.5 inches.</span></span> 
  

