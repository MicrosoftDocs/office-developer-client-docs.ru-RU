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
description: Возвращает самый левый символ или символы в текстовой строке в соответствии с указанным количеством символов.
ms.openlocfilehash: aa4141cfc53bd41a6d58e8bc666b18a06fc80245
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309466"
---
# <a name="left-function-visioshapesheet"></a><span data-ttu-id="7ddbb-103">LEFT Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="7ddbb-103">LEFT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="7ddbb-104">Возвращает самый левый символ или символы в текстовой строке в соответствии с указанным количеством символов.</span><span class="sxs-lookup"><span data-stu-id="7ddbb-104">Returns the left-most character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="7ddbb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ddbb-105">Syntax</span></span>

<span data-ttu-id="7ddbb-106">Left (\* \* *Text* \* \*, [, \* \* *нум_чарс_опт* \* \*])</span><span class="sxs-lookup"><span data-stu-id="7ddbb-106">LEFT(\*\* *text* \*\*, [, \*\* *num_chars_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7ddbb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ddbb-107">Parameters</span></span>

|<span data-ttu-id="7ddbb-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="7ddbb-108">**Name**</span></span>|<span data-ttu-id="7ddbb-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="7ddbb-109">**Required/Optional**</span></span>|<span data-ttu-id="7ddbb-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="7ddbb-110">**Data Type**</span></span>|<span data-ttu-id="7ddbb-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7ddbb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7ddbb-112">_text_</span><span class="sxs-lookup"><span data-stu-id="7ddbb-112">_text_</span></span> <br/> |<span data-ttu-id="7ddbb-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7ddbb-113">Required</span></span>  <br/> |<span data-ttu-id="7ddbb-114">**String**</span><span class="sxs-lookup"><span data-stu-id="7ddbb-114">**String**</span></span> <br/> |<span data-ttu-id="7ddbb-115">Текстовая строка, содержащая символы, которые необходимо извлечь.</span><span class="sxs-lookup"><span data-stu-id="7ddbb-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="7ddbb-116">_нум_чарс_опт_</span><span class="sxs-lookup"><span data-stu-id="7ddbb-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="7ddbb-117">Необязательный</span><span class="sxs-lookup"><span data-stu-id="7ddbb-117">Optional</span></span>  <br/> |<span data-ttu-id="7ddbb-118">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="7ddbb-118">**Numeric**</span></span> <br/> |<span data-ttu-id="7ddbb-119">Число знаков, которое необходимо извлечь.</span><span class="sxs-lookup"><span data-stu-id="7ddbb-119">The number of characters you want to extract.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="7ddbb-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ddbb-120">Return value</span></span>

<span data-ttu-id="7ddbb-121">Строка</span><span class="sxs-lookup"><span data-stu-id="7ddbb-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7ddbb-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="7ddbb-122">Remarks</span></span>

<span data-ttu-id="7ddbb-123">Значение _нум_чарс_опт_ должно быть больше или равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="7ddbb-123">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="7ddbb-124">Если _нум_чарс_опт_ больше, чем длина текста, то Left возвращает весь текст.</span><span class="sxs-lookup"><span data-stu-id="7ddbb-124">If  _num_chars_opt_ is greater than the length of the text, LEFT returns all of the text.</span></span> <span data-ttu-id="7ddbb-125">Если _нум_чарс_опт_ опущено, предполагается, что он равен 1.</span><span class="sxs-lookup"><span data-stu-id="7ddbb-125">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="7ddbb-126">Пример</span><span class="sxs-lookup"><span data-stu-id="7ddbb-126">Example</span></span>

<span data-ttu-id="7ddbb-127">LEFT ("1 января, 2004", 3)</span><span class="sxs-lookup"><span data-stu-id="7ddbb-127">LEFT ("January 1, 2004", 3)</span></span> 
  
<span data-ttu-id="7ddbb-128">Возвращает значение "Jan".</span><span class="sxs-lookup"><span data-stu-id="7ddbb-128">Returns the value "Jan".</span></span> 
  

