---
title: Функция PATHSEGMENT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Возвращает номер 1-based сегмента в указанную часть пометить по указанному пути.
ms.openlocfilehash: b25f43ffa3c719cfc5ffbd1e417f2da9640e483b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814363"
---
# <a name="pathsegment-function"></a><span data-ttu-id="3fe1b-103">Функция PATHSEGMENT</span><span class="sxs-lookup"><span data-stu-id="3fe1b-103">PATHSEGMENT Function</span></span>

<span data-ttu-id="3fe1b-104">Возвращает номер 1-based сегмента в указанную часть пометить по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="3fe1b-104">Returns the 1-based segment number at the specified percentage mark along the specified path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3fe1b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3fe1b-105">Syntax</span></span>

<span data-ttu-id="3fe1b-106">PATHSEGMENT (** *раздел* **, ** *путешествий* **)</span><span class="sxs-lookup"><span data-stu-id="3fe1b-106">PATHSEGMENT(** *section* **, ** *travel* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3fe1b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3fe1b-107">Parameters</span></span>

|<span data-ttu-id="3fe1b-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="3fe1b-108">**Name**</span></span>|<span data-ttu-id="3fe1b-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="3fe1b-109">**Required/Optional**</span></span>|<span data-ttu-id="3fe1b-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="3fe1b-110">**Data Type**</span></span>|<span data-ttu-id="3fe1b-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3fe1b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3fe1b-112">_section_</span><span class="sxs-lookup"><span data-stu-id="3fe1b-112">_section_</span></span> <br/> |<span data-ttu-id="3fe1b-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3fe1b-113">Required</span></span>  <br/> |<span data-ttu-id="3fe1b-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="3fe1b-114">**String**</span></span> <br/> |<span data-ttu-id="3fe1b-115">Раздел геометрии, представляющий путь, указанный с помощью ссылки на его ячейку Path (например, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="3fe1b-115">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="3fe1b-116">_поездки_</span><span class="sxs-lookup"><span data-stu-id="3fe1b-116">_travel_</span></span> <br/> |<span data-ttu-id="3fe1b-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3fe1b-117">Required</span></span>  <br/> |<span data-ttu-id="3fe1b-118">**Double**</span><span class="sxs-lookup"><span data-stu-id="3fe1b-118">**Double**</span></span> <br/> |<span data-ttu-id="3fe1b-119">Процент путь, начиная с начальной точки в конечную точку.</span><span class="sxs-lookup"><span data-stu-id="3fe1b-119">The percentage of the path traversed, from the begin point to the end point.</span></span> <span data-ttu-id="3fe1b-120">Должен быть в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="3fe1b-120">Must be between 0 and 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3fe1b-121">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="3fe1b-121">Return value</span></span>

<span data-ttu-id="3fe1b-122">Целое число</span><span class="sxs-lookup"><span data-stu-id="3fe1b-122">Integer</span></span>
  

