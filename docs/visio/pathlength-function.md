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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344417"
---
# <a name="pathlength-function"></a><span data-ttu-id="4c457-103">Функция PATHLENGTH</span><span class="sxs-lookup"><span data-stu-id="4c457-103">PATHLENGTH Function</span></span>

<span data-ttu-id="4c457-104">Возвращает длину пути, определенного в указанном разделе геометрии.</span><span class="sxs-lookup"><span data-stu-id="4c457-104">Returns the length of the path that is defined in the specified Geometry section.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="4c457-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="4c457-105">Version Information</span></span>

<span data-ttu-id="4c457-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="4c457-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4c457-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c457-107">Syntax</span></span>

<span data-ttu-id="4c457-108">PATHLENGTH (\* \* *раздел* \* \* \* \* *[, сегмент]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="4c457-108">PATHLENGTH(\*\* *section* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4c457-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c457-109">Parameters</span></span>

|<span data-ttu-id="4c457-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="4c457-110">**Name**</span></span>|<span data-ttu-id="4c457-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="4c457-111">**Required/Optional**</span></span>|<span data-ttu-id="4c457-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="4c457-112">**Data Type**</span></span>|<span data-ttu-id="4c457-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4c457-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4c457-114">_section_</span><span class="sxs-lookup"><span data-stu-id="4c457-114">_section_</span></span> <br/> |<span data-ttu-id="4c457-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4c457-115">Required</span></span>  <br/> |<span data-ttu-id="4c457-116">**String**</span><span class="sxs-lookup"><span data-stu-id="4c457-116">**String**</span></span> <br/> |<span data-ttu-id="4c457-117">Раздел геометрии, представляющий путь, заданный ссылкой на ячейку пути (например, Geometry1. Path).</span><span class="sxs-lookup"><span data-stu-id="4c457-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="4c457-118">_сегмент_</span><span class="sxs-lookup"><span data-stu-id="4c457-118">_segment_</span></span> <br/> |<span data-ttu-id="4c457-119">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="4c457-119">Optional</span></span>  <br/> |<span data-ttu-id="4c457-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="4c457-120">**Integer**</span></span> <br/> |<span data-ttu-id="4c457-121">Сегмент на основе единицы измерения пути для измерения.</span><span class="sxs-lookup"><span data-stu-id="4c457-121">The 1-based segment of the path to measure.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4c457-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c457-122">Return value</span></span>

 <span data-ttu-id="4c457-123">**Double**</span><span class="sxs-lookup"><span data-stu-id="4c457-123">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4c457-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c457-124">Remarks</span></span>

<span data-ttu-id="4c457-125">Если _раздел_ или _сегмент_ не существует, Microsoft Visio возвращает #REF!.</span><span class="sxs-lookup"><span data-stu-id="4c457-125">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="4c457-126">Если вы включаете значение _сегмента_ , PATHLENGTH возвращает длину только этого сегмента.</span><span class="sxs-lookup"><span data-stu-id="4c457-126">If you include a  _segment_ value, PATHLENGTH returns the length of that segment only.</span></span> 
  

