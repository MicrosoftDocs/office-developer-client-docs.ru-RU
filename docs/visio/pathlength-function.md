---
title: Функция PATHLENGTH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Возвращает длину пути, определенного в указанном разделе геометрии.
ms.openlocfilehash: e4f90c2bb886f54164bedab5f8d78fc528758414
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405851"
---
# <a name="pathlength-function"></a><span data-ttu-id="2fd9d-103">Функция PATHLENGTH</span><span class="sxs-lookup"><span data-stu-id="2fd9d-103">PATHLENGTH Function</span></span>

<span data-ttu-id="2fd9d-104">Возвращает длину пути, определенного в указанном разделе геометрии.</span><span class="sxs-lookup"><span data-stu-id="2fd9d-104">Returns the length of the path that is defined in the specified Geometry section.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="2fd9d-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="2fd9d-105">Version Information</span></span>

<span data-ttu-id="2fd9d-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="2fd9d-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2fd9d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2fd9d-107">Syntax</span></span>

<span data-ttu-id="2fd9d-108">PATHLENGTH (\* \* *раздел* \* \* \* \* *[, сегмент]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="2fd9d-108">PATHLENGTH(\*\* *section* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2fd9d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2fd9d-109">Parameters</span></span>

|<span data-ttu-id="2fd9d-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="2fd9d-110">**Name**</span></span>|<span data-ttu-id="2fd9d-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="2fd9d-111">**Required/Optional**</span></span>|<span data-ttu-id="2fd9d-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="2fd9d-112">**Data Type**</span></span>|<span data-ttu-id="2fd9d-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2fd9d-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2fd9d-114">_section_</span><span class="sxs-lookup"><span data-stu-id="2fd9d-114">_section_</span></span> <br/> |<span data-ttu-id="2fd9d-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="2fd9d-115">Required</span></span>  <br/> |<span data-ttu-id="2fd9d-116">**String**</span><span class="sxs-lookup"><span data-stu-id="2fd9d-116">**String**</span></span> <br/> |<span data-ttu-id="2fd9d-117">Раздел геометрии, представляющий путь, заданный ссылкой на ячейку пути (например, Geometry1. Path).</span><span class="sxs-lookup"><span data-stu-id="2fd9d-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="2fd9d-118">_сегмент_</span><span class="sxs-lookup"><span data-stu-id="2fd9d-118">_segment_</span></span> <br/> |<span data-ttu-id="2fd9d-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="2fd9d-119">Optional</span></span>  <br/> |<span data-ttu-id="2fd9d-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="2fd9d-120">**Integer**</span></span> <br/> |<span data-ttu-id="2fd9d-121">Сегмент на основе единицы измерения пути для измерения.</span><span class="sxs-lookup"><span data-stu-id="2fd9d-121">The 1-based segment of the path to measure.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2fd9d-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2fd9d-122">Return value</span></span>

 <span data-ttu-id="2fd9d-123">**Double**</span><span class="sxs-lookup"><span data-stu-id="2fd9d-123">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2fd9d-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="2fd9d-124">Remarks</span></span>

<span data-ttu-id="2fd9d-125">Если _раздел_ или _сегмент_ не существует, Microsoft Visio возвращает #REF!.</span><span class="sxs-lookup"><span data-stu-id="2fd9d-125">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="2fd9d-126">Если вы включаете значение _сегмента_ , PATHLENGTH возвращает длину только этого сегмента.</span><span class="sxs-lookup"><span data-stu-id="2fd9d-126">If you include a  _segment_ value, PATHLENGTH returns the length of that segment only.</span></span> 
  

