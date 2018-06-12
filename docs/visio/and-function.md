---
title: И функции
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251391
localization_priority: Normal
ms.assetid: 434d7ceb-1050-c667-fb3d-b6634440c18e
description: Возвращает значение TRUE (1), если все предоставленные логические выражения имеют значение TRUE. Если какие-либо из логических выражений, FALSE или 0, функция и возвращает значение FALSE (0).
ms.openlocfilehash: 27b2ef97ef1d0afde37596b18674c6de26355a1b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813163"
---
# <a name="and-function"></a><span data-ttu-id="5532e-104">И функции</span><span class="sxs-lookup"><span data-stu-id="5532e-104">AND Function</span></span>

<span data-ttu-id="5532e-105">Возвращает значение TRUE (1), если все предоставленные логические выражения имеют значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="5532e-105">Returns TRUE (1) if all of the logical expressions supplied are TRUE.</span></span> <span data-ttu-id="5532e-106">Если какие-либо из логических выражений, FALSE или 0, функция и возвращает значение FALSE (0).</span><span class="sxs-lookup"><span data-stu-id="5532e-106">If any of the logical expressions are FALSE or 0, the AND function returns FALSE (0).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5532e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5532e-107">Syntax</span></span>

<span data-ttu-id="5532e-108">И (** *логической Выражение1* **, ** *логической Выражение2* **,..., ** *логической expressionN* **)</span><span class="sxs-lookup"><span data-stu-id="5532e-108">AND(** *logical expression1* **, ** *logical expression2* **,..., ** *logical expressionN* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5532e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5532e-109">Parameters</span></span>

|<span data-ttu-id="5532e-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="5532e-110">**Name**</span></span>|<span data-ttu-id="5532e-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="5532e-111">**Required/Optional**</span></span>|<span data-ttu-id="5532e-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="5532e-112">**Data Type**</span></span>|<span data-ttu-id="5532e-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5532e-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5532e-114">_Логическое выражение_</span><span class="sxs-lookup"><span data-stu-id="5532e-114">_logical expression_</span></span> <br/> |<span data-ttu-id="5532e-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5532e-115">Required</span></span>  <br/> |<span data-ttu-id="5532e-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="5532e-116">**String**</span></span> <br/> | <span data-ttu-id="5532e-117">Комбинация константы, операторы, функции и ссылки на ячейки таблицы свойств фигуры, которая приводит к значение.</span><span class="sxs-lookup"><span data-stu-id="5532e-117">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span> <span data-ttu-id="5532e-118">Любое выражение, которое оценивается как ненулевое значение считается значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="5532e-118">Any expression that evaluates to a non-zero value is considered to be TRUE.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="5532e-119">Пример</span><span class="sxs-lookup"><span data-stu-id="5532e-119">Example</span></span>

<span data-ttu-id="5532e-120">И (высота \> 1, PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="5532e-120">AND(Height \> 1, PinX \> 1)</span></span>
  
<span data-ttu-id="5532e-121">Возвращает значение TRUE, если оба выражения имеют значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="5532e-121">Returns TRUE if both expressions are TRUE.</span></span> <span data-ttu-id="5532e-122">Возвращает значение FALSE, если выражение имеет значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="5532e-122">Returns FALSE if either expression is FALSE.</span></span>
  

