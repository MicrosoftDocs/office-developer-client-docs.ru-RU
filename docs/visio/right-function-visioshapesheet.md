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
description: Возвращает последний символ или символ в текстовой строке в зависимости от количества символов, которые вы указываете.
ms.openlocfilehash: faf14ef55b34e51bac11129d6857e381d07357c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411458"
---
# <a name="right-function-visioshapesheet"></a><span data-ttu-id="5e33e-103">RIGHT Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="5e33e-103">RIGHT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="5e33e-104">Возвращает последний символ или символ в текстовой строке в зависимости от количества символов, которые вы указываете.</span><span class="sxs-lookup"><span data-stu-id="5e33e-104">Returns the last character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5e33e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e33e-105">Syntax</span></span>

<span data-ttu-id="5e33e-106">RIGHT(\*\* *text* \*\* [, \*\* *num_chars_opt* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="5e33e-106">RIGHT(\*\* *text* \*\* [, \*\* *num_chars_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5e33e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e33e-107">Parameters</span></span>

|<span data-ttu-id="5e33e-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="5e33e-108">**Name**</span></span>|<span data-ttu-id="5e33e-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="5e33e-109">**Required/Optional**</span></span>|<span data-ttu-id="5e33e-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="5e33e-110">**Data Type**</span></span>|<span data-ttu-id="5e33e-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5e33e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5e33e-112">_text_</span><span class="sxs-lookup"><span data-stu-id="5e33e-112">_text_</span></span> <br/> |<span data-ttu-id="5e33e-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5e33e-113">Required</span></span>  <br/> |<span data-ttu-id="5e33e-114">**String**</span><span class="sxs-lookup"><span data-stu-id="5e33e-114">**String**</span></span> <br/> | <span data-ttu-id="5e33e-115">Текстовая строка, содержащая символы, которые необходимо извлечь.</span><span class="sxs-lookup"><span data-stu-id="5e33e-115">The text string containing the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="5e33e-116">_num_chars_opt_</span><span class="sxs-lookup"><span data-stu-id="5e33e-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="5e33e-117">Необязательный</span><span class="sxs-lookup"><span data-stu-id="5e33e-117">Optional</span></span>  <br/> |<span data-ttu-id="5e33e-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="5e33e-118">**Number**</span></span> <br/> |<span data-ttu-id="5e33e-119">Количество символов, которые необходимо извлечь.</span><span class="sxs-lookup"><span data-stu-id="5e33e-119">The number of characters you want to extract.</span></span> <span data-ttu-id="5e33e-120">По умолчанию используется значение 1.</span><span class="sxs-lookup"><span data-stu-id="5e33e-120">The default is 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5e33e-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e33e-121">Return value</span></span>

<span data-ttu-id="5e33e-122">String</span><span class="sxs-lookup"><span data-stu-id="5e33e-122">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5e33e-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="5e33e-123">Remarks</span></span>

<span data-ttu-id="5e33e-124">Значение num_chars_opt  должно быть больше или равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="5e33e-124">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="5e33e-125">Если  _num_chars_opt_ больше длины текста, право возвращает весь текст.</span><span class="sxs-lookup"><span data-stu-id="5e33e-125">If  _num_chars_opt_ is greater than the length of the text, RIGHT returns all of the text.</span></span> <span data-ttu-id="5e33e-126">Если  _num_chars_opt_ опущен, предполагается, что это будет 1.</span><span class="sxs-lookup"><span data-stu-id="5e33e-126">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5e33e-127">Пример</span><span class="sxs-lookup"><span data-stu-id="5e33e-127">Example</span></span>

<span data-ttu-id="5e33e-128">RIGHT (1 января 2004 г., 4)</span><span class="sxs-lookup"><span data-stu-id="5e33e-128">RIGHT ("January 1, 2004", 4)</span></span> 
  
<span data-ttu-id="5e33e-129">Возвращает значение 2004.</span><span class="sxs-lookup"><span data-stu-id="5e33e-129">Returns the value 2004.</span></span> 
  

