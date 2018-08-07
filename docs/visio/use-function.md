---
title: Функция USE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251510
localization_priority: Normal
ms.assetid: 410c4187-21f3-d959-750e-9dc6095fba9a
description: Применяется шаблон линии, узора или имя для фигуры при размещении в ячейке LinePattern, узор заливки, BeginArrow или EndArrow конца строки.
ms.openlocfilehash: 0b6668e57a8f997a69fece51cbc5bd1b1574a576
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815109"
---
# <a name="use-function"></a><span data-ttu-id="7231c-103">Функция USE</span><span class="sxs-lookup"><span data-stu-id="7231c-103">USE Function</span></span>

<span data-ttu-id="7231c-104">Применяется шаблон линии, узора или именем _имя_ фигуры при размещении в ячейке LinePattern, узор заливки, BeginArrow или EndArrow конца строки.</span><span class="sxs-lookup"><span data-stu-id="7231c-104">Applies the line pattern, fill pattern, or line end called  _name_ to the shape when placed in the LinePattern, FillPattern, BeginArrow, or EndArrow cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7231c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7231c-105">Syntax</span></span>

<span data-ttu-id="7231c-106">Использование ("** *имя* **")</span><span class="sxs-lookup"><span data-stu-id="7231c-106">USE(" ** *name* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7231c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7231c-107">Parameters</span></span>

|<span data-ttu-id="7231c-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="7231c-108">**Name**</span></span>|<span data-ttu-id="7231c-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="7231c-109">**Required/Optional**</span></span>|<span data-ttu-id="7231c-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="7231c-110">**Data Type**</span></span>|<span data-ttu-id="7231c-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7231c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7231c-112">_name_</span><span class="sxs-lookup"><span data-stu-id="7231c-112">_name_</span></span> <br/> |<span data-ttu-id="7231c-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7231c-113">Required</span></span>  <br/> |<span data-ttu-id="7231c-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="7231c-114">**String**</span></span> <br/> |<span data-ttu-id="7231c-115">Любая строка, которая является допустимым именем главной.</span><span class="sxs-lookup"><span data-stu-id="7231c-115">Any string that is a valid master name.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="7231c-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6">Return value</span></span>

<span data-ttu-id="7231c-117">Number</span><span class="sxs-lookup"><span data-stu-id="7231c-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7231c-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="7231c-118">Remarks</span></span>

<span data-ttu-id="7231c-119">При наличии в документе шаблона документа с именем _name_ главный шаблон применяется как шаблон линии, узора заливки начать стрелкой, или окончания.</span><span class="sxs-lookup"><span data-stu-id="7231c-119">If a master named  _name_ is present on the document stencil of the document, the pattern is applied as a line pattern, fill pattern, begin arrow, or end arrow.</span></span> 
  
<span data-ttu-id="7231c-120">Эта функция всегда возвращает значение 254.</span><span class="sxs-lookup"><span data-stu-id="7231c-120">This function always returns 254.</span></span>
  
## <a name="example"></a><span data-ttu-id="7231c-121">Пример</span><span class="sxs-lookup"><span data-stu-id="7231c-121">Example</span></span>

<span data-ttu-id="7231c-122">Использование ("Отслеживание железных")</span><span class="sxs-lookup"><span data-stu-id="7231c-122">USE("Railroad Tracks")</span></span> 
  
<span data-ttu-id="7231c-123">Форматирует фигуры, применяя главных шаблон с именем отслеживает железных фигуру, содержащий формулу.</span><span class="sxs-lookup"><span data-stu-id="7231c-123">Formats the shape by applying the master pattern named Railroad Tracks to the shape containing the formula.</span></span> 
  

