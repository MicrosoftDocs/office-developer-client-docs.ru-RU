---
title: Функция SETATREFEVAL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1042150
localization_priority: Normal
ms.assetid: b3f3a0a0-7b14-0b71-d247-ada81b93b66b
description: Используется в параметре ВЫРАЖЕНИЕ_МНОЖЕСТВА функции указывает, что этот set_expression должно оцениваться перед назначением параметру ссылки в функции SETATREF.
ms.openlocfilehash: 0826ef9ca91e180576c0b2611452758b238736a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814743"
---
# <a name="setatrefeval-function"></a><span data-ttu-id="821dc-103">Функция SETATREFEVAL</span><span class="sxs-lookup"><span data-stu-id="821dc-103">SETATREFEVAL Function</span></span>

<span data-ttu-id="821dc-104">Используется в _параметре ВЫРАЖЕНИЕ_МНОЖЕСТВА функции_ указывает, что этот _set_expression_ должно оцениваться перед назначением параметру _ссылки_ в функции SETATREF.</span><span class="sxs-lookup"><span data-stu-id="821dc-104">Used in the  _set_expression_ parameter of the SETATREF function to indicate that  _set_expression_ should be evaluated before assigning to the  _reference_ parameter in SETATREF.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="821dc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="821dc-105">Syntax</span></span>

<span data-ttu-id="821dc-106">SETATREFEVAL (** *expr* **)</span><span class="sxs-lookup"><span data-stu-id="821dc-106">SETATREFEVAL(** *expr* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="821dc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="821dc-107">Parameters</span></span>

|<span data-ttu-id="821dc-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="821dc-108">**Name**</span></span>|<span data-ttu-id="821dc-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="821dc-109">**Required/Optional**</span></span>|<span data-ttu-id="821dc-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="821dc-110">**Data Type**</span></span>|<span data-ttu-id="821dc-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="821dc-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="821dc-112">_expr_</span><span class="sxs-lookup"><span data-stu-id="821dc-112">_expr_</span></span> <br/> |<span data-ttu-id="821dc-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="821dc-113">Required</span></span>  <br/> |<span data-ttu-id="821dc-114">**Разные**</span><span class="sxs-lookup"><span data-stu-id="821dc-114">**Varies**</span></span> <br/> | <span data-ttu-id="821dc-115">Выражение, которое оценивается при ВЫРАЖЕНИЕ_МНОЖЕСТВА функции перенаправляет _set_expression_ на другую ячейку.</span><span class="sxs-lookup"><span data-stu-id="821dc-115">An expression that is evaluated when the SETATREF function redirects  _set_expression_ to another cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="821dc-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="821dc-116">Remarks</span></span>

<span data-ttu-id="821dc-117">При назначении *параметре ВЫРАЖЕНИЕ_МНОЖЕСТВА функции* на ячейку, который указывает ссылка, Microsoft Visio записывает *set_expression* ячейки как выражение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="821dc-117">When assigning the  *set_expression*  parameter of the SETATREF function to a referenced cell, Microsoft Visio writes  *set_expression*  to the cell as an expression by default.</span></span> <span data-ttu-id="821dc-118">Тем не менее если любой части *параметре* переносится с помощью функции SETATREFEVAL, Visio применяет выражение и заменяет функции SETATREFEVAL результат перед разрешением выражение функции SETATREF.</span><span class="sxs-lookup"><span data-stu-id="821dc-118">However, if any portion of the  *set_expression*  parameter is wrapped by the SETATREFEVAL function, Visio evaluates the expression and replaces the SETATREFEVAL function with its result prior to resolving the SETATREF expression.</span></span> 
  
## <a name="example"></a><span data-ttu-id="821dc-119">Пример</span><span class="sxs-lookup"><span data-stu-id="821dc-119">Example</span></span>

<span data-ttu-id="821dc-120">Пример в разделе [ВЫРАЖЕНИЕ_МНОЖЕСТВА](setatref-function.md) функции.</span><span class="sxs-lookup"><span data-stu-id="821dc-120">For an example, see the [SETATREF](setatref-function.md) function.</span></span> 
  

