---
title: Функция USERUI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251511
localization_priority: Normal
ms.assetid: c01dd938-677c-b2ba-8f56-4638e7e988fd
description: Применяет одну из двух выражений в зависимости от значения состояния.
ms.openlocfilehash: 2cfdf23986a06dcc109106bd50a1a38e5af91313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815123"
---
# <a name="userui-function"></a><span data-ttu-id="a7330-103">Функция USERUI</span><span class="sxs-lookup"><span data-stu-id="a7330-103">USERUI Function</span></span>

<span data-ttu-id="a7330-104">Применяет одну из двух выражений в зависимости от значения _состояния_.</span><span class="sxs-lookup"><span data-stu-id="a7330-104">Evaluates one of the two expressions depending on the value of  _state_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a7330-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7330-105">Syntax</span></span>

<span data-ttu-id="a7330-106">USERUI (** *состояние* **, ** *defaultexpression* **, ** *userexpression* **)</span><span class="sxs-lookup"><span data-stu-id="a7330-106">USERUI(** *state* **, ** *defaultexpression* **, ** *userexpression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a7330-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7330-107">Parameters</span></span>

|<span data-ttu-id="a7330-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="a7330-108">**Name**</span></span>|<span data-ttu-id="a7330-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="a7330-109">**Required/Optional**</span></span>|<span data-ttu-id="a7330-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="a7330-110">**Data Type**</span></span>|<span data-ttu-id="a7330-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a7330-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a7330-112">_state_</span><span class="sxs-lookup"><span data-stu-id="a7330-112">_state_</span></span> <br/> |<span data-ttu-id="a7330-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a7330-113">Required</span></span>  <br/> |<span data-ttu-id="a7330-114">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a7330-114">**Boolean**</span></span> <br/> |<span data-ttu-id="a7330-115">Определяет, какие выражение для вычисления.</span><span class="sxs-lookup"><span data-stu-id="a7330-115">Determines which expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="a7330-116">_defaultexpression_</span><span class="sxs-lookup"><span data-stu-id="a7330-116">_defaultexpression_</span></span> <br/> |<span data-ttu-id="a7330-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a7330-117">Required</span></span>  <br/> |<span data-ttu-id="a7330-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="a7330-118">**String**</span></span> <br/> |<span data-ttu-id="a7330-119">Выражение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a7330-119">The default expression.</span></span>  <br/> |
| <span data-ttu-id="a7330-120">_userexpression_</span><span class="sxs-lookup"><span data-stu-id="a7330-120">_userexpression_</span></span> <br/> |<span data-ttu-id="a7330-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a7330-121">Required</span></span>  <br/> |<span data-ttu-id="a7330-122">**Строка**</span><span class="sxs-lookup"><span data-stu-id="a7330-122">**String**</span></span> <br/> |<span data-ttu-id="a7330-123">Выражение, предоставленные пользователем.</span><span class="sxs-lookup"><span data-stu-id="a7330-123">An expression supplied by the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7330-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="a7330-124">Remarks</span></span>

<span data-ttu-id="a7330-125">Если _состояние_ имеет значение 0, функция USERUI вычисляет _defaultexpression_.</span><span class="sxs-lookup"><span data-stu-id="a7330-125">If  _state_ is 0, the USERUI function evaluates the  _defaultexpression_.</span></span> <span data-ttu-id="a7330-126">Если _задано значение 1,_ вычисляет _userexpression_.</span><span class="sxs-lookup"><span data-stu-id="a7330-126">If  _state_ is 1, it evaluates the  _userexpression_.</span></span>
  
## <a name="example"></a><span data-ttu-id="a7330-127">Пример</span><span class="sxs-lookup"><span data-stu-id="a7330-127">Example</span></span>

<span data-ttu-id="a7330-128">USERUI (1, если (ширина\>на 6, 6 in, ширина), ширина\*0,75)</span><span class="sxs-lookup"><span data-stu-id="a7330-128">USERUI(1, if(Width\>6in, 6in, Width), Width\*0.75)</span></span> 
  
<span data-ttu-id="a7330-129">Применяет выражение ширина\*.075 и возвращает результат.</span><span class="sxs-lookup"><span data-stu-id="a7330-129">Evaluates the expression Width\*.075 and returns the result.</span></span> 
  

