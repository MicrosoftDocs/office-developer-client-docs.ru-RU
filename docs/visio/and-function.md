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
description: Возвращает значение TRUE (1), если все предоставленные логические выражения имеют значение TRUE. Если любое из логических выражений имеет значение FALSE или 0, функция и возвращает значение FALSE (0).
ms.openlocfilehash: 74e8301718e69a2ab61f6bf9992d0d6855bbc6f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341561"
---
# <a name="and-function"></a><span data-ttu-id="dd87c-104">Функция AND</span><span class="sxs-lookup"><span data-stu-id="dd87c-104">AND Function</span></span>

<span data-ttu-id="dd87c-105">Возвращает значение TRUE (1), если все предоставленные логические выражения имеют значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="dd87c-105">Returns TRUE (1) if all of the logical expressions supplied are TRUE.</span></span> <span data-ttu-id="dd87c-106">Если любое из логических выражений имеет значение FALSE или 0, функция и возвращает значение FALSE (0).</span><span class="sxs-lookup"><span data-stu-id="dd87c-106">If any of the logical expressions are FALSE or 0, the AND function returns FALSE (0).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="dd87c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd87c-107">Syntax</span></span>

<span data-ttu-id="dd87c-108">AND (\* \* *logical выражение1* \* \*, \* \* *logical выражение2* \* \*,..., \* \* *логический експрессионн* \* \*)</span><span class="sxs-lookup"><span data-stu-id="dd87c-108">AND(\*\* *logical expression1* \*\*, \*\* *logical expression2* \*\*,..., \*\* *logical expressionN* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dd87c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd87c-109">Parameters</span></span>

|<span data-ttu-id="dd87c-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="dd87c-110">**Name**</span></span>|<span data-ttu-id="dd87c-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="dd87c-111">**Required/Optional**</span></span>|<span data-ttu-id="dd87c-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="dd87c-112">**Data Type**</span></span>|<span data-ttu-id="dd87c-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dd87c-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dd87c-114">_Логическое выражение_</span><span class="sxs-lookup"><span data-stu-id="dd87c-114">_logical expression_</span></span> <br/> |<span data-ttu-id="dd87c-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="dd87c-115">Required</span></span>  <br/> |<span data-ttu-id="dd87c-116">**String**</span><span class="sxs-lookup"><span data-stu-id="dd87c-116">**String**</span></span> <br/> | <span data-ttu-id="dd87c-117">Сочетание констант, операторов, функций и ссылок на ячейки таблицы свойств фигуры, в результате чего получается значение.</span><span class="sxs-lookup"><span data-stu-id="dd87c-117">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span> <span data-ttu-id="dd87c-118">Любое выражение, результатом которого является ненулевое значение, считается ИСТИНным.</span><span class="sxs-lookup"><span data-stu-id="dd87c-118">Any expression that evaluates to a non-zero value is considered to be TRUE.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="dd87c-119">Пример</span><span class="sxs-lookup"><span data-stu-id="dd87c-119">Example</span></span>

<span data-ttu-id="dd87c-120">AND (Height \> 1, PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="dd87c-120">AND(Height \> 1, PinX \> 1)</span></span>
  
<span data-ttu-id="dd87c-121">Возвращает значение TRUE, если оба выражения имеют значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="dd87c-121">Returns TRUE if both expressions are TRUE.</span></span> <span data-ttu-id="dd87c-122">Возвращает значение FALSE, если любое выражение имеет значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="dd87c-122">Returns FALSE if either expression is FALSE.</span></span>
  

