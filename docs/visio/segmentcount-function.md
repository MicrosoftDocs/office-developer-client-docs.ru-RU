---
title: Функция SEGMENTCOUNT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: Возвращает число отрезков, составляющих путь.
ms.openlocfilehash: 93a77d9085e6900f502a75401847ad685d25effd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814753"
---
# <a name="segmentcount-function"></a><span data-ttu-id="f39c8-103">Функция SEGMENTCOUNT</span><span class="sxs-lookup"><span data-stu-id="f39c8-103">SEGMENTCOUNT Function</span></span>

<span data-ttu-id="f39c8-104">Возвращает число отрезков, составляющих путь.</span><span class="sxs-lookup"><span data-stu-id="f39c8-104">Returns the number of line segments that make up the path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f39c8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f39c8-105">Syntax</span></span>

<span data-ttu-id="f39c8-106">SEGMENTCOUNT (** *pathRef* **)</span><span class="sxs-lookup"><span data-stu-id="f39c8-106">SEGMENTCOUNT(** *pathRef* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f39c8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f39c8-107">Parameters</span></span>

|<span data-ttu-id="f39c8-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="f39c8-108">**Name**</span></span>|<span data-ttu-id="f39c8-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="f39c8-109">**Required/Optional**</span></span>|<span data-ttu-id="f39c8-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="f39c8-110">**Data Type**</span></span>|<span data-ttu-id="f39c8-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f39c8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f39c8-112">_pathRef_</span><span class="sxs-lookup"><span data-stu-id="f39c8-112">_pathRef_</span></span> <br/> |<span data-ttu-id="f39c8-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f39c8-113">Required</span></span>  <br/> |<span data-ttu-id="f39c8-114">**Integer**</span><span class="sxs-lookup"><span data-stu-id="f39c8-114">**Integer**</span></span> <br/> |<span data-ttu-id="f39c8-115">Раздел геометрии, представляющий путь, указанный с помощью ссылки на ячейки путь (например, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="f39c8-115">The Geometry section that represents the path, specified by a reference to Path cell (for example, Geometry1.Path).</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f39c8-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6">Return value</span></span>

<span data-ttu-id="f39c8-117">Целое число</span><span class="sxs-lookup"><span data-stu-id="f39c8-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f39c8-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="f39c8-118">Remarks</span></span>

<span data-ttu-id="f39c8-119">Пересечения линий не включаются в общее число возвращаемых сегменты.</span><span class="sxs-lookup"><span data-stu-id="f39c8-119">Line jumps are not included in the total number of segments returned.</span></span>
  

