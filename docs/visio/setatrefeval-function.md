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
description: Используется в set_expression параметра функции SETATREF, чтобы указать, что set_expression должны быть оценены перед назначением эталонного параметра в SETATREF.
ms.openlocfilehash: a11a7485e04d4deb31e9497476bb198d675bc68f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432984"
---
# <a name="setatrefeval-function"></a><span data-ttu-id="4bc10-103">Функция SETATREFEVAL</span><span class="sxs-lookup"><span data-stu-id="4bc10-103">SETATREFEVAL Function</span></span>

<span data-ttu-id="4bc10-104">Используется в _set_expression_ параметра функции SETATREF,  чтобы указать, что set_expression должны быть  оценены перед назначением эталонного параметра в SETATREF.</span><span class="sxs-lookup"><span data-stu-id="4bc10-104">Used in the  _set_expression_ parameter of the SETATREF function to indicate that  _set_expression_ should be evaluated before assigning to the  _reference_ parameter in SETATREF.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4bc10-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4bc10-105">Syntax</span></span>

<span data-ttu-id="4bc10-106">SETATREFEVAL(\*\* *expr* \*\* )</span><span class="sxs-lookup"><span data-stu-id="4bc10-106">SETATREFEVAL(\*\* *expr* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4bc10-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4bc10-107">Parameters</span></span>

|<span data-ttu-id="4bc10-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="4bc10-108">**Name**</span></span>|<span data-ttu-id="4bc10-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="4bc10-109">**Required/Optional**</span></span>|<span data-ttu-id="4bc10-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="4bc10-110">**Data Type**</span></span>|<span data-ttu-id="4bc10-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4bc10-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4bc10-112">_expr_</span><span class="sxs-lookup"><span data-stu-id="4bc10-112">_expr_</span></span> <br/> |<span data-ttu-id="4bc10-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4bc10-113">Required</span></span>  <br/> |<span data-ttu-id="4bc10-114">**Разные**</span><span class="sxs-lookup"><span data-stu-id="4bc10-114">**Varies**</span></span> <br/> | <span data-ttu-id="4bc10-115">Выражение, которое оценивается при перенаправлении функции SETATREF  _set_expression_ другую ячейку.</span><span class="sxs-lookup"><span data-stu-id="4bc10-115">An expression that is evaluated when the SETATREF function redirects  _set_expression_ to another cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4bc10-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="4bc10-116">Remarks</span></span>

<span data-ttu-id="4bc10-117">При назначении *set_expression* функции SETATREF в ссылаемую ячейку Microsoft Visio записывает *set_expression* ячейку в качестве выражения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4bc10-117">When assigning the  *set_expression*  parameter of the SETATREF function to a referenced cell, Microsoft Visio writes  *set_expression*  to the cell as an expression by default.</span></span> <span data-ttu-id="4bc10-118">Однако если часть параметра *set_expression* завернута функцией SETATREFEVAL, Visio оценивает выражение и заменяет функцию SETATREFEVAL ее результатом до разрешения выражения SETATREF.</span><span class="sxs-lookup"><span data-stu-id="4bc10-118">However, if any portion of the  *set_expression*  parameter is wrapped by the SETATREFEVAL function, Visio evaluates the expression and replaces the SETATREFEVAL function with its result prior to resolving the SETATREF expression.</span></span> 
  
## <a name="example"></a><span data-ttu-id="4bc10-119">Пример</span><span class="sxs-lookup"><span data-stu-id="4bc10-119">Example</span></span>

<span data-ttu-id="4bc10-120">Например, см. [функцию SETATREF.](setatref-function.md)</span><span class="sxs-lookup"><span data-stu-id="4bc10-120">For an example, see the [SETATREF](setatref-function.md) function.</span></span> 
  

