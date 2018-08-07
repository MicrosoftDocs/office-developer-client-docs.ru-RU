---
title: Функция EVALTEXT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251422
localization_priority: Normal
ms.assetid: c9b5b96c-d8c8-6119-e3f1-a2ce9d7c043e
description: Обрабатывает текст в указанной фигуре формулу, и возвращает результат.
ms.openlocfilehash: 69e79a23faa9d09aa2ad51f83363064b54742152
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813704"
---
# <a name="evaltext-function"></a><span data-ttu-id="eb2ff-103">Функция EVALTEXT</span><span class="sxs-lookup"><span data-stu-id="eb2ff-103">EVALTEXT Function</span></span>

<span data-ttu-id="eb2ff-104">Обрабатывает текст в _указанной фигуре_ формулу, и возвращает результат.</span><span class="sxs-lookup"><span data-stu-id="eb2ff-104">Evaluates the text in  _shapename_ as if it were a formula and returns the result.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="eb2ff-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb2ff-105">Syntax</span></span>

<span data-ttu-id="eb2ff-106">EVALTEXT (** *указанной фигуре! theText* **)</span><span class="sxs-lookup"><span data-stu-id="eb2ff-106">EVALTEXT(** *shapename!theText* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="eb2ff-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb2ff-107">Parameters</span></span>

|<span data-ttu-id="eb2ff-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="eb2ff-108">**Name**</span></span>|<span data-ttu-id="eb2ff-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="eb2ff-109">**Required/Optional**</span></span>|<span data-ttu-id="eb2ff-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="eb2ff-110">**Data Type**</span></span>|<span data-ttu-id="eb2ff-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="eb2ff-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="eb2ff-112">_указанной фигуре! theText_</span><span class="sxs-lookup"><span data-stu-id="eb2ff-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="eb2ff-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="eb2ff-113">Required</span></span>  <br/> |<span data-ttu-id="eb2ff-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="eb2ff-114">**String**</span></span> <br/> |<span data-ttu-id="eb2ff-115">Ячейка, выполняемого при изменении связанных с фигурой текстовой композиции.</span><span class="sxs-lookup"><span data-stu-id="eb2ff-115">A cell that is triggered when the associated shape's text composition changes.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="eb2ff-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6">Return value</span></span>

<span data-ttu-id="eb2ff-117">Строка</span><span class="sxs-lookup"><span data-stu-id="eb2ff-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eb2ff-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="eb2ff-118">Remarks</span></span>

 <span data-ttu-id="eb2ff-119">_указанной фигуре_ можно использовать для обращения к тексту фигуры, отличного от текущего фигуры.</span><span class="sxs-lookup"><span data-stu-id="eb2ff-119">_shapename_ can be used to refer to the text of a shape other than the current shape.</span></span> 
  
<span data-ttu-id="eb2ff-120">Если не содержит текста, результат равно нулю.</span><span class="sxs-lookup"><span data-stu-id="eb2ff-120">If there is no text, the result is zero.</span></span> <span data-ttu-id="eb2ff-121">Если не может обрабатываться в текст, функция возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="eb2ff-121">If the text cannot be evaluated, the function returns an error.</span></span>
  
## <a name="example"></a><span data-ttu-id="eb2ff-122">Пример</span><span class="sxs-lookup"><span data-stu-id="eb2ff-122">Example</span></span>

<span data-ttu-id="eb2ff-123">EVALTEXT(Line.2!theText)</span><span class="sxs-lookup"><span data-stu-id="eb2ff-123">EVALTEXT(Line.2!theText)</span></span> 
  
<span data-ttu-id="eb2ff-124">Оценивает текст, содержащийся в Line.2 фигуры.</span><span class="sxs-lookup"><span data-stu-id="eb2ff-124">Evaluates the text contained in the shape Line.2.</span></span> <span data-ttu-id="eb2ff-125">Например, если Line.2 содержит «4 ft + 0,5 ft», возвращает значение 4,5 ft.</span><span class="sxs-lookup"><span data-stu-id="eb2ff-125">For example, if Line.2 contains "4 ft + 0.5 ft", returns the value 4.5 ft.</span></span> 
  

