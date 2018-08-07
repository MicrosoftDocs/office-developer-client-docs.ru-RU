---
title: LEFT Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1021757
localization_priority: Normal
ms.assetid: 0c2f6e06-b772-2006-ec7b-8695d097f146
description: Возвращает левые знаки в текстовой строке, на основе числа символов.
ms.openlocfilehash: 4e8deb3098ce6d217dcce0cae23d07ed723d9fb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814063"
---
# <a name="left-function-visioshapesheet"></a><span data-ttu-id="3f35b-103">LEFT Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="3f35b-103">LEFT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="3f35b-104">Возвращает левые знаки в текстовой строке, на основе числа символов.</span><span class="sxs-lookup"><span data-stu-id="3f35b-104">Returns the left-most character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3f35b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f35b-105">Syntax</span></span>

<span data-ttu-id="3f35b-106">СЛЕВА (** *текст* **, [, ** *num_chars_opt* **])</span><span class="sxs-lookup"><span data-stu-id="3f35b-106">LEFT(** *text* **, [, ** *num_chars_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3f35b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f35b-107">Parameters</span></span>

|<span data-ttu-id="3f35b-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="3f35b-108">**Name**</span></span>|<span data-ttu-id="3f35b-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="3f35b-109">**Required/Optional**</span></span>|<span data-ttu-id="3f35b-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="3f35b-110">**Data Type**</span></span>|<span data-ttu-id="3f35b-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3f35b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3f35b-112">_text_</span><span class="sxs-lookup"><span data-stu-id="3f35b-112">_text_</span></span> <br/> |<span data-ttu-id="3f35b-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3f35b-113">Required</span></span>  <br/> |<span data-ttu-id="3f35b-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="3f35b-114">**String**</span></span> <br/> |<span data-ttu-id="3f35b-115">Текстовая строка, содержащая знаки, которые вы хотите извлечь.</span><span class="sxs-lookup"><span data-stu-id="3f35b-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="3f35b-116">_num_chars_opt_</span><span class="sxs-lookup"><span data-stu-id="3f35b-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="3f35b-117">Optional</span><span class="sxs-lookup"><span data-stu-id="3f35b-117">Optional</span></span>  <br/> |<span data-ttu-id="3f35b-118">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="3f35b-118">**Numeric**</span></span> <br/> |<span data-ttu-id="3f35b-119">Число знаков, которое вы хотите извлечь.</span><span class="sxs-lookup"><span data-stu-id="3f35b-119">The number of characters you want to extract.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3f35b-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0">Return value</span></span>

<span data-ttu-id="3f35b-121">Строка</span><span class="sxs-lookup"><span data-stu-id="3f35b-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3f35b-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="3f35b-122">Remarks</span></span>

<span data-ttu-id="3f35b-123">Значение _num_chars_opt_ должно быть больше или равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="3f35b-123">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="3f35b-124">Если _num_chars_opt_ больше, чем длина текста, ЛЕВСИМВ возвращает весь текст.</span><span class="sxs-lookup"><span data-stu-id="3f35b-124">If  _num_chars_opt_ is greater than the length of the text, LEFT returns all of the text.</span></span> <span data-ttu-id="3f35b-125">Если _num_chars_opt_ указан, предполагается 1.</span><span class="sxs-lookup"><span data-stu-id="3f35b-125">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="3f35b-126">Пример</span><span class="sxs-lookup"><span data-stu-id="3f35b-126">Example</span></span>

<span data-ttu-id="3f35b-127">СЛЕВА («1 января 2004», 3)</span><span class="sxs-lookup"><span data-stu-id="3f35b-127">LEFT ("January 1, 2004", 3)</span></span> 
  
<span data-ttu-id="3f35b-128">Возвращает значение «Янв».</span><span class="sxs-lookup"><span data-stu-id="3f35b-128">Returns the value "Jan".</span></span> 
  

