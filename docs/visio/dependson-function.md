---
title: Функция DEPENDSON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251420
localization_priority: Normal
ms.assetid: 8fcfcfdd-69e2-b061-fdb6-d29389d14403
description: Создает зависимость адреса ячейки.
ms.openlocfilehash: 07c0d79668230cbf2b1e8d51b50e67835c87e2f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813589"
---
# <a name="dependson-function"></a><span data-ttu-id="e483e-103">Функция DEPENDSON</span><span class="sxs-lookup"><span data-stu-id="e483e-103">DEPENDSON Function</span></span>

<span data-ttu-id="e483e-104">Создает зависимость адреса ячейки.</span><span class="sxs-lookup"><span data-stu-id="e483e-104">Creates a cell reference dependency.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e483e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e483e-105">Syntax</span></span>

<span data-ttu-id="e483e-106">DEPENDSON (** *cellref* ** [, ** *cellref2* **,...])</span><span class="sxs-lookup"><span data-stu-id="e483e-106">DEPENDSON(** *cellref* ** [, ** *cellref2* **,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e483e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e483e-107">Parameters</span></span>

|<span data-ttu-id="e483e-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="e483e-108">**Name**</span></span>|<span data-ttu-id="e483e-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="e483e-109">**Required/Optional**</span></span>|<span data-ttu-id="e483e-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="e483e-110">**Data Type**</span></span>|<span data-ttu-id="e483e-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e483e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e483e-112">_cellref_</span><span class="sxs-lookup"><span data-stu-id="e483e-112">_cellref_</span></span> <br/> |<span data-ttu-id="e483e-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e483e-113">Required</span></span>  <br/> |<span data-ttu-id="e483e-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="e483e-114">**String**</span></span> <br/> |<span data-ttu-id="e483e-115">Первый ссылка на ячейку.</span><span class="sxs-lookup"><span data-stu-id="e483e-115">The first cell reference.</span></span>  <br/> |
| <span data-ttu-id="e483e-116">_cellref2_</span><span class="sxs-lookup"><span data-stu-id="e483e-116">_cellref2_</span></span> <br/> |<span data-ttu-id="e483e-117">Optional</span><span class="sxs-lookup"><span data-stu-id="e483e-117">Optional</span></span>  <br/> |<span data-ttu-id="e483e-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="e483e-118">**String**</span></span> <br/> |<span data-ttu-id="e483e-119">Вторая ссылка на ячейку.</span><span class="sxs-lookup"><span data-stu-id="e483e-119">The second cell reference.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e483e-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="e483e-120">Remarks</span></span>

<span data-ttu-id="e483e-121">Эта функция всегда возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="e483e-121">This function always returns FALSE.</span></span> <span data-ttu-id="e483e-122">Он не оказывает влияния при использовании в строку события или в действие ячейки.</span><span class="sxs-lookup"><span data-stu-id="e483e-122">It has no effect when used in an Event row or an Action cell.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e483e-123">Пример</span><span class="sxs-lookup"><span data-stu-id="e483e-123">Example</span></span>

<span data-ttu-id="e483e-124">OPENTEXTWIN() + DEPENDSON(PinX,PinY)</span><span class="sxs-lookup"><span data-stu-id="e483e-124">OPENTEXTWIN() + DEPENDSON(PinX,PinY)</span></span> 
  
<span data-ttu-id="e483e-125">Открывает блок текста фигуры при каждом изменении фигуры PinX или PinY ячеек.</span><span class="sxs-lookup"><span data-stu-id="e483e-125">Opens the text block for a shape whenever the shape's PinX or PinY cells change.</span></span> 
  

