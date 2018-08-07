---
title: RIGHT Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027314
localization_priority: Normal
ms.assetid: 910f0297-d588-2048-f308-03f3c2389bba
description: Возвращает последние знаки текстовой строки, на основе числа символов.
ms.openlocfilehash: e35cc4918809d5f134f9519c01cb3c93407258e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814609"
---
# <a name="right-function-visioshapesheet"></a><span data-ttu-id="bdee4-103">RIGHT Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="bdee4-103">RIGHT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="bdee4-104">Возвращает последние знаки текстовой строки, на основе числа символов.</span><span class="sxs-lookup"><span data-stu-id="bdee4-104">Returns the last character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="bdee4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bdee4-105">Syntax</span></span>

<span data-ttu-id="bdee4-106">СПРАВА (** *текст* ** [, ** *num_chars_opt* **])</span><span class="sxs-lookup"><span data-stu-id="bdee4-106">RIGHT(** *text* ** [, ** *num_chars_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bdee4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bdee4-107">Parameters</span></span>

|<span data-ttu-id="bdee4-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="bdee4-108">**Name**</span></span>|<span data-ttu-id="bdee4-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="bdee4-109">**Required/Optional**</span></span>|<span data-ttu-id="bdee4-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="bdee4-110">**Data Type**</span></span>|<span data-ttu-id="bdee4-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bdee4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bdee4-112">_text_</span><span class="sxs-lookup"><span data-stu-id="bdee4-112">_text_</span></span> <br/> |<span data-ttu-id="bdee4-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bdee4-113">Required</span></span>  <br/> |<span data-ttu-id="bdee4-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="bdee4-114">**String**</span></span> <br/> | <span data-ttu-id="bdee4-115">Текстовая строка, содержащая знаки, которые нужно извлечь.</span><span class="sxs-lookup"><span data-stu-id="bdee4-115">The text string containing the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="bdee4-116">_num_chars_opt_</span><span class="sxs-lookup"><span data-stu-id="bdee4-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="bdee4-117">Optional</span><span class="sxs-lookup"><span data-stu-id="bdee4-117">Optional</span></span>  <br/> |<span data-ttu-id="bdee4-118">**Число**</span><span class="sxs-lookup"><span data-stu-id="bdee4-118">**Number**</span></span> <br/> |<span data-ttu-id="bdee4-119">Число знаков, которое вы хотите извлечь.</span><span class="sxs-lookup"><span data-stu-id="bdee4-119">The number of characters you want to extract.</span></span> <span data-ttu-id="bdee4-120">Значение по умолчанию — 1.</span><span class="sxs-lookup"><span data-stu-id="bdee4-120">The default is 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="bdee4-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1">Return value</span></span>

<span data-ttu-id="bdee4-122">Строка</span><span class="sxs-lookup"><span data-stu-id="bdee4-122">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bdee4-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="bdee4-123">Remarks</span></span>

<span data-ttu-id="bdee4-124">Значение _num_chars_opt_ должно быть больше или равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="bdee4-124">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="bdee4-125">Если _num_chars_opt_ больше, чем длина текста, ПРАВСИМВ возвращает весь текст.</span><span class="sxs-lookup"><span data-stu-id="bdee4-125">If  _num_chars_opt_ is greater than the length of the text, RIGHT returns all of the text.</span></span> <span data-ttu-id="bdee4-126">Если _num_chars_opt_ указан, предполагается 1.</span><span class="sxs-lookup"><span data-stu-id="bdee4-126">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="bdee4-127">Пример</span><span class="sxs-lookup"><span data-stu-id="bdee4-127">Example</span></span>

<span data-ttu-id="bdee4-128">СПРАВА («1 января 2004», 4)</span><span class="sxs-lookup"><span data-stu-id="bdee4-128">RIGHT ("January 1, 2004", 4)</span></span> 
  
<span data-ttu-id="bdee4-129">Возвращает значение 2004 г.</span><span class="sxs-lookup"><span data-stu-id="bdee4-129">Returns the value 2004.</span></span> 
  

