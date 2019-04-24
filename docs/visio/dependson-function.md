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
description: Создает зависимость по ссылке на ячейку.
ms.openlocfilehash: 26e7f5fb0620a5f1812d878f02d5bedd43afe524
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360236"
---
# <a name="dependson-function"></a><span data-ttu-id="74dea-103">Функция DEPENDSON</span><span class="sxs-lookup"><span data-stu-id="74dea-103">DEPENDSON Function</span></span>

<span data-ttu-id="74dea-104">Создает зависимость по ссылке на ячейку.</span><span class="sxs-lookup"><span data-stu-id="74dea-104">Creates a cell reference dependency.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="74dea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74dea-105">Syntax</span></span>

<span data-ttu-id="74dea-106">DEPENDSON (\* \* *целлреф* \* \* [, \* \* *cellref2* \* \*,...])</span><span class="sxs-lookup"><span data-stu-id="74dea-106">DEPENDSON(\*\* *cellref* \*\* [, \*\* *cellref2* \*\*,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="74dea-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="74dea-107">Parameters</span></span>

|<span data-ttu-id="74dea-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="74dea-108">**Name**</span></span>|<span data-ttu-id="74dea-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="74dea-109">**Required/Optional**</span></span>|<span data-ttu-id="74dea-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="74dea-110">**Data Type**</span></span>|<span data-ttu-id="74dea-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="74dea-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="74dea-112">_целлреф_</span><span class="sxs-lookup"><span data-stu-id="74dea-112">_cellref_</span></span> <br/> |<span data-ttu-id="74dea-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="74dea-113">Required</span></span>  <br/> |<span data-ttu-id="74dea-114">**String**</span><span class="sxs-lookup"><span data-stu-id="74dea-114">**String**</span></span> <br/> |<span data-ttu-id="74dea-115">Первая ссылка на ячейку.</span><span class="sxs-lookup"><span data-stu-id="74dea-115">The first cell reference.</span></span>  <br/> |
| <span data-ttu-id="74dea-116">_cellref2_</span><span class="sxs-lookup"><span data-stu-id="74dea-116">_cellref2_</span></span> <br/> |<span data-ttu-id="74dea-117">Необязательно</span><span class="sxs-lookup"><span data-stu-id="74dea-117">Optional</span></span>  <br/> |<span data-ttu-id="74dea-118">**String**</span><span class="sxs-lookup"><span data-stu-id="74dea-118">**String**</span></span> <br/> |<span data-ttu-id="74dea-119">Вторая ссылка на ячейку.</span><span class="sxs-lookup"><span data-stu-id="74dea-119">The second cell reference.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74dea-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="74dea-120">Remarks</span></span>

<span data-ttu-id="74dea-121">Эта функция всегда возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="74dea-121">This function always returns FALSE.</span></span> <span data-ttu-id="74dea-122">Он не оказывает никакого действия при использовании в строке события или ячейке Action.</span><span class="sxs-lookup"><span data-stu-id="74dea-122">It has no effect when used in an Event row or an Action cell.</span></span> 
  
## <a name="example"></a><span data-ttu-id="74dea-123">Пример</span><span class="sxs-lookup"><span data-stu-id="74dea-123">Example</span></span>

<span data-ttu-id="74dea-124">OPENTEXTWIN () + DEPENDSON (PinX, PinY)</span><span class="sxs-lookup"><span data-stu-id="74dea-124">OPENTEXTWIN() + DEPENDSON(PinX,PinY)</span></span> 
  
<span data-ttu-id="74dea-125">Открывает блок текста для фигуры при изменении ячеек фигуры PinX или PinY.</span><span class="sxs-lookup"><span data-stu-id="74dea-125">Opens the text block for a shape whenever the shape's PinX or PinY cells change.</span></span> 
  

