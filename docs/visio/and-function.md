---
title: Функция AND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251391
localization_priority: Normal
ms.assetid: 434d7ceb-1050-c667-fb3d-b6634440c18e
description: Возвращает true (1), если все предоставленные логические выражения имеют true. Если любое из логических выражений false или 0, функция AND возвращает false (0).
ms.openlocfilehash: 74e8301718e69a2ab61f6bf9992d0d6855bbc6f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422014"
---
# <a name="and-function"></a><span data-ttu-id="d5140-104">Функция AND</span><span class="sxs-lookup"><span data-stu-id="d5140-104">AND Function</span></span>

<span data-ttu-id="d5140-105">Возвращает true (1), если все логические выражения имеют true.</span><span class="sxs-lookup"><span data-stu-id="d5140-105">Returns TRUE (1) if all of the logical expressions supplied are TRUE.</span></span> <span data-ttu-id="d5140-106">Если любое из логических выражений — FALSE или 0, функция AND возвращает false (0).</span><span class="sxs-lookup"><span data-stu-id="d5140-106">If any of the logical expressions are FALSE or 0, the AND function returns FALSE (0).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d5140-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5140-107">Syntax</span></span>

<span data-ttu-id="d5140-108">AND(\*\* *logical expression1* \*\*, \*\* *logical expression2* \*\*,..., \*\* *logical expressionN* \*\* )</span><span class="sxs-lookup"><span data-stu-id="d5140-108">AND(\*\* *logical expression1* \*\*, \*\* *logical expression2* \*\*,..., \*\* *logical expressionN* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d5140-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5140-109">Parameters</span></span>

|<span data-ttu-id="d5140-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="d5140-110">**Name**</span></span>|<span data-ttu-id="d5140-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="d5140-111">**Required/Optional**</span></span>|<span data-ttu-id="d5140-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="d5140-112">**Data Type**</span></span>|<span data-ttu-id="d5140-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d5140-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d5140-114">_логическое выражение_</span><span class="sxs-lookup"><span data-stu-id="d5140-114">_logical expression_</span></span> <br/> |<span data-ttu-id="d5140-115">Обязательно</span><span class="sxs-lookup"><span data-stu-id="d5140-115">Required</span></span>  <br/> |<span data-ttu-id="d5140-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="d5140-116">**String**</span></span> <br/> | <span data-ttu-id="d5140-117">Сочетание констант, операторов, функций и ссылок на ячейки ShapeSheet, которое приводит к значению.</span><span class="sxs-lookup"><span data-stu-id="d5140-117">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span> <span data-ttu-id="d5140-118">Любое выражение, которое оценивается как ненулевой, считается TRUE.</span><span class="sxs-lookup"><span data-stu-id="d5140-118">Any expression that evaluates to a non-zero value is considered to be TRUE.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="d5140-119">Пример</span><span class="sxs-lookup"><span data-stu-id="d5140-119">Example</span></span>

<span data-ttu-id="d5140-120">AND(Height \> 1, PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="d5140-120">AND(Height \> 1, PinX \> 1)</span></span>
  
<span data-ttu-id="d5140-121">Возвращает true, если оба выражения имеют true.</span><span class="sxs-lookup"><span data-stu-id="d5140-121">Returns TRUE if both expressions are TRUE.</span></span> <span data-ttu-id="d5140-122">Возвращает false, если для любого из выражений запроизведется false.</span><span class="sxs-lookup"><span data-stu-id="d5140-122">Returns FALSE if either expression is FALSE.</span></span>
  

