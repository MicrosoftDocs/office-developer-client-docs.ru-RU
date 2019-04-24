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
description: Используется в параметре Set_Expression функции SETATREF, чтобы указать, что перед назначением параметра reference в SETATREF необходимо оценить значение аргумента Set_Expression.
ms.openlocfilehash: a11a7485e04d4deb31e9497476bb198d675bc68f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326161"
---
# <a name="setatrefeval-function"></a><span data-ttu-id="c0d0e-103">Функция SETATREFEVAL</span><span class="sxs-lookup"><span data-stu-id="c0d0e-103">SETATREFEVAL Function</span></span>

<span data-ttu-id="c0d0e-104">Используется в параметре _Set_Expression_ функции SETATREF, чтобы указать, что __ перед назначением параметра _Reference_ в SETATREF необходимо оценить значение аргумента Set_Expression.</span><span class="sxs-lookup"><span data-stu-id="c0d0e-104">Used in the  _set_expression_ parameter of the SETATREF function to indicate that  _set_expression_ should be evaluated before assigning to the  _reference_ parameter in SETATREF.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c0d0e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0d0e-105">Syntax</span></span>

<span data-ttu-id="c0d0e-106">SETATREFEVAL (\* \* *expr* \* \*)</span><span class="sxs-lookup"><span data-stu-id="c0d0e-106">SETATREFEVAL(\*\* *expr* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c0d0e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0d0e-107">Parameters</span></span>

|<span data-ttu-id="c0d0e-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="c0d0e-108">**Name**</span></span>|<span data-ttu-id="c0d0e-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="c0d0e-109">**Required/Optional**</span></span>|<span data-ttu-id="c0d0e-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="c0d0e-110">**Data Type**</span></span>|<span data-ttu-id="c0d0e-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c0d0e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c0d0e-112">_expr_</span><span class="sxs-lookup"><span data-stu-id="c0d0e-112">_expr_</span></span> <br/> |<span data-ttu-id="c0d0e-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c0d0e-113">Required</span></span>  <br/> |<span data-ttu-id="c0d0e-114">**Разные**</span><span class="sxs-lookup"><span data-stu-id="c0d0e-114">**Varies**</span></span> <br/> | <span data-ttu-id="c0d0e-115">Выражение, которое оценивается, когда функция SETATREF перенаправляет аргумент _Set_Expression_ в другую ячейку.</span><span class="sxs-lookup"><span data-stu-id="c0d0e-115">An expression that is evaluated when the SETATREF function redirects  _set_expression_ to another cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0d0e-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="c0d0e-116">Remarks</span></span>

<span data-ttu-id="c0d0e-117">При назначении аргумента *Set_Expression* функции SETATREF ячейке, на которую указывает ссылка, Microsoft Visio записывает аргумент *Set_Expression* в ячейку как выражение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c0d0e-117">When assigning the  *set_expression*  parameter of the SETATREF function to a referenced cell, Microsoft Visio writes  *set_expression*  to the cell as an expression by default.</span></span> <span data-ttu-id="c0d0e-118">Тем не менее, если какая-либо часть параметра *Set_Expression* упакована функцией SETATREFEVAL, Visio вычисляет выражение и заменяет функцию SETATREFEVAL на ее результат перед разрешением выражения SETATREF.</span><span class="sxs-lookup"><span data-stu-id="c0d0e-118">However, if any portion of the  *set_expression*  parameter is wrapped by the SETATREFEVAL function, Visio evaluates the expression and replaces the SETATREFEVAL function with its result prior to resolving the SETATREF expression.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c0d0e-119">Пример</span><span class="sxs-lookup"><span data-stu-id="c0d0e-119">Example</span></span>

<span data-ttu-id="c0d0e-120">Пример приведен в разделе Функция [SETATREF](setatref-function.md) .</span><span class="sxs-lookup"><span data-stu-id="c0d0e-120">For an example, see the [SETATREF](setatref-function.md) function.</span></span> 
  

