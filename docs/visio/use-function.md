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
description: Применяет шаблон строки, шаблон заливки или название конца строки, называемое именем, к фигуре при размещении в ячейках LinePattern, FillPattern, BeginArrow или EndArrow.
ms.openlocfilehash: ddd15c1c127fafa1a230545d544c74956f5c0262
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422826"
---
# <a name="use-function"></a><span data-ttu-id="8ba27-103">Функция USE</span><span class="sxs-lookup"><span data-stu-id="8ba27-103">USE Function</span></span>

<span data-ttu-id="8ba27-104">Применяет шаблон строки, шаблон заливки  или название конца строки, называемое именем, к фигуре при размещении в ячейках LinePattern, FillPattern, BeginArrow или EndArrow.</span><span class="sxs-lookup"><span data-stu-id="8ba27-104">Applies the line pattern, fill pattern, or line end called  _name_ to the shape when placed in the LinePattern, FillPattern, BeginArrow, or EndArrow cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8ba27-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ba27-105">Syntax</span></span>

<span data-ttu-id="8ba27-106">USE(" \*\* *name* \*\* ")</span><span class="sxs-lookup"><span data-stu-id="8ba27-106">USE(" \*\* *name* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8ba27-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ba27-107">Parameters</span></span>

|<span data-ttu-id="8ba27-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="8ba27-108">**Name**</span></span>|<span data-ttu-id="8ba27-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="8ba27-109">**Required/Optional**</span></span>|<span data-ttu-id="8ba27-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="8ba27-110">**Data Type**</span></span>|<span data-ttu-id="8ba27-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8ba27-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8ba27-112">_name_</span><span class="sxs-lookup"><span data-stu-id="8ba27-112">_name_</span></span> <br/> |<span data-ttu-id="8ba27-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="8ba27-113">Required</span></span>  <br/> |<span data-ttu-id="8ba27-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="8ba27-114">**String**</span></span> <br/> |<span data-ttu-id="8ba27-115">Любая строка, которая является допустимым именем хозяина.</span><span class="sxs-lookup"><span data-stu-id="8ba27-115">Any string that is a valid master name.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8ba27-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ba27-116">Return value</span></span>

<span data-ttu-id="8ba27-117">Числовой</span><span class="sxs-lookup"><span data-stu-id="8ba27-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8ba27-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ba27-118">Remarks</span></span>

<span data-ttu-id="8ba27-119">Если в  трафарете документа присутствует имя хозяина, шаблон применяется в качестве шаблона линии, шаблона заливки, стрелки начала или стрелки конца.</span><span class="sxs-lookup"><span data-stu-id="8ba27-119">If a master named  _name_ is present on the document stencil of the document, the pattern is applied as a line pattern, fill pattern, begin arrow, or end arrow.</span></span> 
  
<span data-ttu-id="8ba27-120">Эта функция всегда возвращает 254.</span><span class="sxs-lookup"><span data-stu-id="8ba27-120">This function always returns 254.</span></span>
  
## <a name="example"></a><span data-ttu-id="8ba27-121">Пример</span><span class="sxs-lookup"><span data-stu-id="8ba27-121">Example</span></span>

<span data-ttu-id="8ba27-122">USE("Tracks")</span><span class="sxs-lookup"><span data-stu-id="8ba27-122">USE("Railroad Tracks")</span></span> 
  
<span data-ttu-id="8ba27-123">Форматирование фигуры путем применения образца шаблона с именем "Замещая дорожки" к фигуре, содержащей формулу.</span><span class="sxs-lookup"><span data-stu-id="8ba27-123">Formats the shape by applying the master pattern named Railroad Tracks to the shape containing the formula.</span></span> 
  

