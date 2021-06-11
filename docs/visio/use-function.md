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
description: При размещении в ячейке LinePattern, FillPattern, BeginArrow или EndArrow используется шаблон строки, или конец строки, называемый именем.
ms.openlocfilehash: ddd15c1c127fafa1a230545d544c74956f5c0262
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422826"
---
# <a name="use-function"></a><span data-ttu-id="5203d-103">Функция USE</span><span class="sxs-lookup"><span data-stu-id="5203d-103">USE Function</span></span>

<span data-ttu-id="5203d-104">При размещении в ячейке LinePattern, FillPattern, BeginArrow или EndArrow используется шаблон строки, или конец строки, называемый именем. </span><span class="sxs-lookup"><span data-stu-id="5203d-104">Applies the line pattern, fill pattern, or line end called  _name_ to the shape when placed in the LinePattern, FillPattern, BeginArrow, or EndArrow cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5203d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5203d-105">Syntax</span></span>

<span data-ttu-id="5203d-106">USE(" \*\* *имя* \*\* ")</span><span class="sxs-lookup"><span data-stu-id="5203d-106">USE(" \*\* *name* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5203d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5203d-107">Parameters</span></span>

|<span data-ttu-id="5203d-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="5203d-108">**Name**</span></span>|<span data-ttu-id="5203d-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="5203d-109">**Required/Optional**</span></span>|<span data-ttu-id="5203d-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="5203d-110">**Data Type**</span></span>|<span data-ttu-id="5203d-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5203d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5203d-112">_name_</span><span class="sxs-lookup"><span data-stu-id="5203d-112">_name_</span></span> <br/> |<span data-ttu-id="5203d-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5203d-113">Required</span></span>  <br/> |<span data-ttu-id="5203d-114">**String**</span><span class="sxs-lookup"><span data-stu-id="5203d-114">**String**</span></span> <br/> |<span data-ttu-id="5203d-115">Любая строка, которая является допустимым мастер-именем.</span><span class="sxs-lookup"><span data-stu-id="5203d-115">Any string that is a valid master name.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5203d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5203d-116">Return value</span></span>

<span data-ttu-id="5203d-117">Номер</span><span class="sxs-lookup"><span data-stu-id="5203d-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5203d-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="5203d-118">Remarks</span></span>

<span data-ttu-id="5203d-119">Если на  трафарете документа присутствует имя мастера, шаблон применяется в качестве шаблона строки, шаблона заполнения, начала стрелки или конечной стрелки.</span><span class="sxs-lookup"><span data-stu-id="5203d-119">If a master named  _name_ is present on the document stencil of the document, the pattern is applied as a line pattern, fill pattern, begin arrow, or end arrow.</span></span> 
  
<span data-ttu-id="5203d-120">Эта функция всегда возвращает 254.</span><span class="sxs-lookup"><span data-stu-id="5203d-120">This function always returns 254.</span></span>
  
## <a name="example"></a><span data-ttu-id="5203d-121">Пример</span><span class="sxs-lookup"><span data-stu-id="5203d-121">Example</span></span>

<span data-ttu-id="5203d-122">USE ("Железнодорожные пути")</span><span class="sxs-lookup"><span data-stu-id="5203d-122">USE("Railroad Tracks")</span></span> 
  
<span data-ttu-id="5203d-123">Форматы формы, применяя шаблон магистрали с именем Железнодорожные пути к фигуре, содержащей формулу.</span><span class="sxs-lookup"><span data-stu-id="5203d-123">Formats the shape by applying the master pattern named Railroad Tracks to the shape containing the formula.</span></span> 
  

