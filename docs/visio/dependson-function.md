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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423470"
---
# <a name="dependson-function"></a><span data-ttu-id="e0233-103">Функция DEPENDSON</span><span class="sxs-lookup"><span data-stu-id="e0233-103">DEPENDSON Function</span></span>

<span data-ttu-id="e0233-104">Создает зависимость по ссылке на ячейку.</span><span class="sxs-lookup"><span data-stu-id="e0233-104">Creates a cell reference dependency.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e0233-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0233-105">Syntax</span></span>

<span data-ttu-id="e0233-106">DEPENDSON (\* \* *целлреф* \* \* [, \* \* *cellref2* \* \*,...])</span><span class="sxs-lookup"><span data-stu-id="e0233-106">DEPENDSON(\*\* *cellref* \*\* [, \*\* *cellref2* \*\*,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e0233-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0233-107">Parameters</span></span>

|<span data-ttu-id="e0233-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="e0233-108">**Name**</span></span>|<span data-ttu-id="e0233-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="e0233-109">**Required/Optional**</span></span>|<span data-ttu-id="e0233-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="e0233-110">**Data Type**</span></span>|<span data-ttu-id="e0233-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e0233-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e0233-112">_целлреф_</span><span class="sxs-lookup"><span data-stu-id="e0233-112">_cellref_</span></span> <br/> |<span data-ttu-id="e0233-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e0233-113">Required</span></span>  <br/> |<span data-ttu-id="e0233-114">**String**</span><span class="sxs-lookup"><span data-stu-id="e0233-114">**String**</span></span> <br/> |<span data-ttu-id="e0233-115">Первая ссылка на ячейку.</span><span class="sxs-lookup"><span data-stu-id="e0233-115">The first cell reference.</span></span>  <br/> |
| <span data-ttu-id="e0233-116">_cellref2_</span><span class="sxs-lookup"><span data-stu-id="e0233-116">_cellref2_</span></span> <br/> |<span data-ttu-id="e0233-117">Необязательный</span><span class="sxs-lookup"><span data-stu-id="e0233-117">Optional</span></span>  <br/> |<span data-ttu-id="e0233-118">**String**</span><span class="sxs-lookup"><span data-stu-id="e0233-118">**String**</span></span> <br/> |<span data-ttu-id="e0233-119">Вторая ссылка на ячейку.</span><span class="sxs-lookup"><span data-stu-id="e0233-119">The second cell reference.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0233-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="e0233-120">Remarks</span></span>

<span data-ttu-id="e0233-121">Эта функция всегда возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="e0233-121">This function always returns FALSE.</span></span> <span data-ttu-id="e0233-122">Он не оказывает никакого действия при использовании в строке события или ячейке Action.</span><span class="sxs-lookup"><span data-stu-id="e0233-122">It has no effect when used in an Event row or an Action cell.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e0233-123">Пример</span><span class="sxs-lookup"><span data-stu-id="e0233-123">Example</span></span>

<span data-ttu-id="e0233-124">OPENTEXTWIN () + DEPENDSON (PinX, PinY)</span><span class="sxs-lookup"><span data-stu-id="e0233-124">OPENTEXTWIN() + DEPENDSON(PinX,PinY)</span></span> 
  
<span data-ttu-id="e0233-125">Открывает блок текста для фигуры при изменении ячеек фигуры PinX или PinY.</span><span class="sxs-lookup"><span data-stu-id="e0233-125">Opens the text block for a shape whenever the shape's PinX or PinY cells change.</span></span> 
  

