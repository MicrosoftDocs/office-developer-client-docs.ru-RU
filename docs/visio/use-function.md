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
description: Применяет к фигуре шаблон линии, узор заливки или конец строки, вызываемый в ячейке в ячейке LinePattern, FillPattern, BeginArrow или EndArrow.
ms.openlocfilehash: ddd15c1c127fafa1a230545d544c74956f5c0262
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422826"
---
# <a name="use-function"></a><span data-ttu-id="28413-103">Функция USE</span><span class="sxs-lookup"><span data-stu-id="28413-103">USE Function</span></span>

<span data-ttu-id="28413-104">Применяет к фигуре шаблон линии, узор заливки или конец строки, _вызываемый_ в ячейке в ячейке LinePattern, FillPattern, BeginArrow или EndArrow.</span><span class="sxs-lookup"><span data-stu-id="28413-104">Applies the line pattern, fill pattern, or line end called  _name_ to the shape when placed in the LinePattern, FillPattern, BeginArrow, or EndArrow cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="28413-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28413-105">Syntax</span></span>

<span data-ttu-id="28413-106">USE ("\* \* *Name* \* \*")</span><span class="sxs-lookup"><span data-stu-id="28413-106">USE(" \*\* *name* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="28413-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="28413-107">Parameters</span></span>

|<span data-ttu-id="28413-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="28413-108">**Name**</span></span>|<span data-ttu-id="28413-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="28413-109">**Required/Optional**</span></span>|<span data-ttu-id="28413-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="28413-110">**Data Type**</span></span>|<span data-ttu-id="28413-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="28413-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="28413-112">_name_</span><span class="sxs-lookup"><span data-stu-id="28413-112">_name_</span></span> <br/> |<span data-ttu-id="28413-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="28413-113">Required</span></span>  <br/> |<span data-ttu-id="28413-114">**String**</span><span class="sxs-lookup"><span data-stu-id="28413-114">**String**</span></span> <br/> |<span data-ttu-id="28413-115">Любая строка, которая является допустимым именем образца.</span><span class="sxs-lookup"><span data-stu-id="28413-115">Any string that is a valid master name.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="28413-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28413-116">Return value</span></span>

<span data-ttu-id="28413-117">Номер</span><span class="sxs-lookup"><span data-stu-id="28413-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="28413-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="28413-118">Remarks</span></span>

<span data-ttu-id="28413-119">Если в трафарете документа имеется шаблон именованного _имени_ , шаблон применяется как узор линии, узор заливки, стрелка начала или стрелка конца.</span><span class="sxs-lookup"><span data-stu-id="28413-119">If a master named  _name_ is present on the document stencil of the document, the pattern is applied as a line pattern, fill pattern, begin arrow, or end arrow.</span></span> 
  
<span data-ttu-id="28413-120">Эта функция всегда возвращает значение 254.</span><span class="sxs-lookup"><span data-stu-id="28413-120">This function always returns 254.</span></span>
  
## <a name="example"></a><span data-ttu-id="28413-121">Пример</span><span class="sxs-lookup"><span data-stu-id="28413-121">Example</span></span>

<span data-ttu-id="28413-122">ИСПОЛЬЗОВАНИЕ ("Раилроадных дорожек")</span><span class="sxs-lookup"><span data-stu-id="28413-122">USE("Railroad Tracks")</span></span> 
  
<span data-ttu-id="28413-123">Форматирует фигуру, применяя к фигуре, содержащей формулу, шаблон образца с именем Раилроад.</span><span class="sxs-lookup"><span data-stu-id="28413-123">Formats the shape by applying the master pattern named Railroad Tracks to the shape containing the formula.</span></span> 
  

