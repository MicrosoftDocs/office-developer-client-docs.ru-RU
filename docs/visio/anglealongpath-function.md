---
title: Функция ANGLEALONGPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Возвращает угол тангента в путь в заданной точке.
ms.openlocfilehash: a15e45ff6135972cd1cd78382147a493f8fc8d69
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160295"
---
# <a name="anglealongpath-function"></a><span data-ttu-id="d67ff-103">Функция ANGLEALONGPATH</span><span class="sxs-lookup"><span data-stu-id="d67ff-103">ANGLEALONGPATH Function</span></span>

<span data-ttu-id="d67ff-104">Возвращает угол тангента в путь в заданной точке.</span><span class="sxs-lookup"><span data-stu-id="d67ff-104">Returns the angle of the tangent to the path at a given point.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="d67ff-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="d67ff-105">Version Information</span></span>

<span data-ttu-id="d67ff-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="d67ff-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d67ff-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d67ff-107">Syntax</span></span>

<span data-ttu-id="d67ff-108">ANGLEALONGPATH(***section***, ***travel*** ***[,segment]*** )</span><span class="sxs-lookup"><span data-stu-id="d67ff-108">ANGLEALONGPATH(***section***, ***travel*** ***[,segment]*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d67ff-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d67ff-109">Parameters</span></span>

|<span data-ttu-id="d67ff-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="d67ff-110">**Name**</span></span>|<span data-ttu-id="d67ff-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="d67ff-111">**Required/Optional**</span></span>|<span data-ttu-id="d67ff-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="d67ff-112">**Data Type**</span></span>|<span data-ttu-id="d67ff-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d67ff-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d67ff-114">_section_</span><span class="sxs-lookup"><span data-stu-id="d67ff-114">_section_</span></span> <br/> |<span data-ttu-id="d67ff-115">Обязательно</span><span class="sxs-lookup"><span data-stu-id="d67ff-115">Required</span></span>  <br/> |<span data-ttu-id="d67ff-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="d67ff-116">**String**</span></span> <br/> |<span data-ttu-id="d67ff-117">Раздел "Геометрия", который представляет путь, заданный ссылкой на его ячейку Path (например, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="d67ff-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="d67ff-118">_travel_</span><span class="sxs-lookup"><span data-stu-id="d67ff-118">_travel_</span></span> <br/> |<span data-ttu-id="d67ff-119">Обязательна</span><span class="sxs-lookup"><span data-stu-id="d67ff-119">Required</span></span>  <br/> |<span data-ttu-id="d67ff-120">64-разрядное число с плавающей запятой двойной точности.</span><span class="sxs-lookup"><span data-stu-id="d67ff-120">**Double**</span></span> <br/> |<span data-ttu-id="d67ff-121">Процент вдоль пути от точки начала до конца.</span><span class="sxs-lookup"><span data-stu-id="d67ff-121">The percentage along the path from begin point to end point.</span></span> <span data-ttu-id="d67ff-122">Должно быть от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="d67ff-122">Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="d67ff-123">_segment_</span><span class="sxs-lookup"><span data-stu-id="d67ff-123">_segment_</span></span> <br/> |<span data-ttu-id="d67ff-124">Необязательна</span><span class="sxs-lookup"><span data-stu-id="d67ff-124">Optional</span></span>  <br/> |<span data-ttu-id="d67ff-125">64-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="d67ff-125">**Integer**</span></span> <br/> |<span data-ttu-id="d67ff-126">Сегмент пути на основе 1, по которому вычисляется угол тангента.</span><span class="sxs-lookup"><span data-stu-id="d67ff-126">The 1-based segment of the path at which to calculate the tangent angle.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d67ff-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d67ff-127">Return value</span></span>

 <span data-ttu-id="d67ff-128">64-разрядное число с плавающей запятой двойной точности.</span><span class="sxs-lookup"><span data-stu-id="d67ff-128">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d67ff-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="d67ff-129">Remarks</span></span>

<span data-ttu-id="d67ff-130">Если у вас есть  _значение сегмента,_ ANGLEALONGPATH возвращает значение только для этого сегмента.</span><span class="sxs-lookup"><span data-stu-id="d67ff-130">If you include a  _segment_ value, ANGLEALONGPATH returns the value for that segment only.</span></span> 
  
<span data-ttu-id="d67ff-131">Если вы _включаете_ значение сегмента, ANGLEALONGPATH определяет точку тангенса с помощью перемещения для вычисления перцеrtage вдоль _сегмента._ </span><span class="sxs-lookup"><span data-stu-id="d67ff-131">If you include a  _segment_ value, ANGLEALONGPATH determines the point of the tangent by using  _travel_ to calculate the percertage along  _segment_.</span></span>
  
<span data-ttu-id="d67ff-132">Если раздел  _или_  _сегмент_ не существует, Microsoft Visio возвращает #REF!.</span><span class="sxs-lookup"><span data-stu-id="d67ff-132">If either  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

