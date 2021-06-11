---
title: Функция PATHLENGTH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Возвращает длину пути, заданного в указанном разделе Геометрия.
ms.openlocfilehash: e4f90c2bb886f54164bedab5f8d78fc528758414
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405851"
---
# <a name="pathlength-function"></a><span data-ttu-id="07a8e-103">Функция PATHLENGTH</span><span class="sxs-lookup"><span data-stu-id="07a8e-103">PATHLENGTH Function</span></span>

<span data-ttu-id="07a8e-104">Возвращает длину пути, заданного в указанном разделе Геометрия.</span><span class="sxs-lookup"><span data-stu-id="07a8e-104">Returns the length of the path that is defined in the specified Geometry section.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="07a8e-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="07a8e-105">Version Information</span></span>

<span data-ttu-id="07a8e-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="07a8e-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="07a8e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07a8e-107">Syntax</span></span>

<span data-ttu-id="07a8e-108">PATHLENGTH(\*\* *раздел* \*\* \*\*\* [,сегмент]\* \*\* )</span><span class="sxs-lookup"><span data-stu-id="07a8e-108">PATHLENGTH(\*\* *section* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="07a8e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="07a8e-109">Parameters</span></span>

|<span data-ttu-id="07a8e-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="07a8e-110">**Name**</span></span>|<span data-ttu-id="07a8e-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="07a8e-111">**Required/Optional**</span></span>|<span data-ttu-id="07a8e-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="07a8e-112">**Data Type**</span></span>|<span data-ttu-id="07a8e-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="07a8e-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="07a8e-114">_section_</span><span class="sxs-lookup"><span data-stu-id="07a8e-114">_section_</span></span> <br/> |<span data-ttu-id="07a8e-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="07a8e-115">Required</span></span>  <br/> |<span data-ttu-id="07a8e-116">**String**</span><span class="sxs-lookup"><span data-stu-id="07a8e-116">**String**</span></span> <br/> |<span data-ttu-id="07a8e-117">Раздел Геометрия, который представляет путь, заданный ссылкой на его ячейку Path (например, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="07a8e-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="07a8e-118">_segment_</span><span class="sxs-lookup"><span data-stu-id="07a8e-118">_segment_</span></span> <br/> |<span data-ttu-id="07a8e-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="07a8e-119">Optional</span></span>  <br/> |<span data-ttu-id="07a8e-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="07a8e-120">**Integer**</span></span> <br/> |<span data-ttu-id="07a8e-121">1-ый сегмент пути для измерения.</span><span class="sxs-lookup"><span data-stu-id="07a8e-121">The 1-based segment of the path to measure.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="07a8e-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07a8e-122">Return value</span></span>

 <span data-ttu-id="07a8e-123">**Double**</span><span class="sxs-lookup"><span data-stu-id="07a8e-123">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="07a8e-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="07a8e-124">Remarks</span></span>

<span data-ttu-id="07a8e-125">Если _раздел_ или _сегмент_ не существует, корпорация Майкрософт Visio возвращает #REF!.</span><span class="sxs-lookup"><span data-stu-id="07a8e-125">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="07a8e-126">Если вы включаете  _значение сегмента,_ PATHLENGTH возвращает длину только этого сегмента.</span><span class="sxs-lookup"><span data-stu-id="07a8e-126">If you include a  _segment_ value, PATHLENGTH returns the length of that segment only.</span></span> 
  

