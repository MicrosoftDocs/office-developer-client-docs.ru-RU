---
title: Функция SEGMENTCOUNT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: Возвращает количество сегментов линии, составляющих путь.
ms.openlocfilehash: 947e37c13de638e4f281bc17376a253a8ca07e04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326042"
---
# <a name="segmentcount-function"></a><span data-ttu-id="e99b6-103">Функция SEGMENTCOUNT</span><span class="sxs-lookup"><span data-stu-id="e99b6-103">SEGMENTCOUNT Function</span></span>

<span data-ttu-id="e99b6-104">Возвращает количество сегментов линии, составляющих путь.</span><span class="sxs-lookup"><span data-stu-id="e99b6-104">Returns the number of line segments that make up the path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e99b6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e99b6-105">Syntax</span></span>

<span data-ttu-id="e99b6-106">SEGMENTCOUNT (\* \* *пасреф* \* \*)</span><span class="sxs-lookup"><span data-stu-id="e99b6-106">SEGMENTCOUNT(\*\* *pathRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e99b6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e99b6-107">Parameters</span></span>

|<span data-ttu-id="e99b6-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="e99b6-108">**Name**</span></span>|<span data-ttu-id="e99b6-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="e99b6-109">**Required/Optional**</span></span>|<span data-ttu-id="e99b6-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="e99b6-110">**Data Type**</span></span>|<span data-ttu-id="e99b6-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e99b6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e99b6-112">_Пасреф_</span><span class="sxs-lookup"><span data-stu-id="e99b6-112">_pathRef_</span></span> <br/> |<span data-ttu-id="e99b6-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e99b6-113">Required</span></span>  <br/> |<span data-ttu-id="e99b6-114">**Integer**</span><span class="sxs-lookup"><span data-stu-id="e99b6-114">**Integer**</span></span> <br/> |<span data-ttu-id="e99b6-115">Раздел геометрии, представляющий путь, заданный с помощью ячейки ссылки на путь (например, Geometry1. Path).</span><span class="sxs-lookup"><span data-stu-id="e99b6-115">The Geometry section that represents the path, specified by a reference to Path cell (for example, Geometry1.Path).</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e99b6-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e99b6-116">Return value</span></span>

<span data-ttu-id="e99b6-117">Целое число</span><span class="sxs-lookup"><span data-stu-id="e99b6-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e99b6-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="e99b6-118">Remarks</span></span>

<span data-ttu-id="e99b6-119">Пересечения линий не включаются в общее число возвращенных сегментов.</span><span class="sxs-lookup"><span data-stu-id="e99b6-119">Line jumps are not included in the total number of segments returned.</span></span>
  

