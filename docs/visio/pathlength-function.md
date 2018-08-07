---
title: Функция PATHLENGTH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Возвращает длину пути, который определен в указанном раздел геометрии.
ms.openlocfilehash: 37cabbde9fc0782bc1fde46f3065d0c945c9dada
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814358"
---
# <a name="pathlength-function"></a><span data-ttu-id="57dc3-103">Функция PATHLENGTH</span><span class="sxs-lookup"><span data-stu-id="57dc3-103">PATHLENGTH Function</span></span>

<span data-ttu-id="57dc3-104">Возвращает длину пути, который определен в указанном раздел геометрии.</span><span class="sxs-lookup"><span data-stu-id="57dc3-104">Returns the length of the path that is defined in the specified Geometry section.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="57dc3-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="57dc3-105">Version Information</span></span>

<span data-ttu-id="57dc3-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="57dc3-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="57dc3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57dc3-107">Syntax</span></span>

<span data-ttu-id="57dc3-108">PATHLENGTH (** *раздел* ** ** *[, сегмент]* **)</span><span class="sxs-lookup"><span data-stu-id="57dc3-108">PATHLENGTH(** *section* ** ** *[,segment]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="57dc3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="57dc3-109">Parameters</span></span>

|<span data-ttu-id="57dc3-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="57dc3-110">**Name**</span></span>|<span data-ttu-id="57dc3-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="57dc3-111">**Required/Optional**</span></span>|<span data-ttu-id="57dc3-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="57dc3-112">**Data Type**</span></span>|<span data-ttu-id="57dc3-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="57dc3-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="57dc3-114">_section_</span><span class="sxs-lookup"><span data-stu-id="57dc3-114">_section_</span></span> <br/> |<span data-ttu-id="57dc3-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="57dc3-115">Required</span></span>  <br/> |<span data-ttu-id="57dc3-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="57dc3-116">**String**</span></span> <br/> |<span data-ttu-id="57dc3-117">Раздел геометрии, представляющий путь, указанный с помощью ссылки на его ячейку Path (например, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="57dc3-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="57dc3-118">_сегмента_</span><span class="sxs-lookup"><span data-stu-id="57dc3-118">_segment_</span></span> <br/> |<span data-ttu-id="57dc3-119">Optional</span><span class="sxs-lookup"><span data-stu-id="57dc3-119">Optional</span></span>  <br/> |<span data-ttu-id="57dc3-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="57dc3-120">**Integer**</span></span> <br/> |<span data-ttu-id="57dc3-121">На основе 1 сегментом пути для измерения.</span><span class="sxs-lookup"><span data-stu-id="57dc3-121">The 1-based segment of the path to measure.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="57dc3-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2">Return value</span></span>

 <span data-ttu-id="57dc3-123">**Double**</span><span class="sxs-lookup"><span data-stu-id="57dc3-123">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="57dc3-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="57dc3-124">Remarks</span></span>

<span data-ttu-id="57dc3-125">Если _раздел_ или _Сегмент_ не существует, Microsoft Visio возвращает #REF!.</span><span class="sxs-lookup"><span data-stu-id="57dc3-125">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="57dc3-126">Если включить значение _сегмента_ PATHLENGTH возвращает длина сегмента только.</span><span class="sxs-lookup"><span data-stu-id="57dc3-126">If you include a  _segment_ value, PATHLENGTH returns the length of that segment only.</span></span> 
  

