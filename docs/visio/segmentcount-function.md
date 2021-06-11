---
title: Функция SEGMENTCOUNT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: Возвращает количество сегментов строк, которые составляют путь.
ms.openlocfilehash: 947e37c13de638e4f281bc17376a253a8ca07e04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424499"
---
# <a name="segmentcount-function"></a><span data-ttu-id="64a95-103">Функция SEGMENTCOUNT</span><span class="sxs-lookup"><span data-stu-id="64a95-103">SEGMENTCOUNT Function</span></span>

<span data-ttu-id="64a95-104">Возвращает количество сегментов строк, которые составляют путь.</span><span class="sxs-lookup"><span data-stu-id="64a95-104">Returns the number of line segments that make up the path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="64a95-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64a95-105">Syntax</span></span>

<span data-ttu-id="64a95-106">SEGMENTCOUNT(\*\* *pathRef* \*\* )</span><span class="sxs-lookup"><span data-stu-id="64a95-106">SEGMENTCOUNT(\*\* *pathRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="64a95-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="64a95-107">Parameters</span></span>

|<span data-ttu-id="64a95-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="64a95-108">**Name**</span></span>|<span data-ttu-id="64a95-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="64a95-109">**Required/Optional**</span></span>|<span data-ttu-id="64a95-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="64a95-110">**Data Type**</span></span>|<span data-ttu-id="64a95-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="64a95-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="64a95-112">_pathRef_</span><span class="sxs-lookup"><span data-stu-id="64a95-112">_pathRef_</span></span> <br/> |<span data-ttu-id="64a95-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="64a95-113">Required</span></span>  <br/> |<span data-ttu-id="64a95-114">**Integer**</span><span class="sxs-lookup"><span data-stu-id="64a95-114">**Integer**</span></span> <br/> |<span data-ttu-id="64a95-115">Раздел Геометрия, который представляет путь, заданный ссылкой на ячейку Path (например, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="64a95-115">The Geometry section that represents the path, specified by a reference to Path cell (for example, Geometry1.Path).</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="64a95-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="64a95-116">Return value</span></span>

<span data-ttu-id="64a95-117">Целое число</span><span class="sxs-lookup"><span data-stu-id="64a95-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="64a95-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="64a95-118">Remarks</span></span>

<span data-ttu-id="64a95-119">Прыжки строки не включаются в общее число возвращаемого сегмента.</span><span class="sxs-lookup"><span data-stu-id="64a95-119">Line jumps are not included in the total number of segments returned.</span></span>
  

