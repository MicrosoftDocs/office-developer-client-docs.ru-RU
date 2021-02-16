---
title: Функция BITXOR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251401
localization_priority: Normal
ms.assetid: 672eacaf-a374-c7e2-b39b-8d42d2371aee
description: Возвращает 16-битное двоичное число, в котором для каждого бита установлено 1, если соответствующий бит в двоичном номере 1 и двоичном номере 2 — 1. В противном случае для бита установлено 0.
ms.openlocfilehash: ab8ff46fe98512d963ef4ecd5c37127353827725
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439235"
---
# <a name="bitxor-function"></a><span data-ttu-id="559a4-104">Функция BITXOR</span><span class="sxs-lookup"><span data-stu-id="559a4-104">BITXOR Function</span></span>

<span data-ttu-id="559a4-105">Возвращает 16-битный двоичный номер, в котором для каждого бита установлено 1, если соответствующий бит в двоичном номере1 и двоичном номере 2 — 1.</span><span class="sxs-lookup"><span data-stu-id="559a4-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either but not both binary number1 and binary number2 is 1.</span></span> <span data-ttu-id="559a4-106">В противном случае для бита устанавливается 0.</span><span class="sxs-lookup"><span data-stu-id="559a4-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="559a4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="559a4-107">Syntax</span></span>

<span data-ttu-id="559a4-108">BITXOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span><span class="sxs-lookup"><span data-stu-id="559a4-108">BITXOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="559a4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="559a4-109">Parameters</span></span>

|<span data-ttu-id="559a4-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="559a4-110">**Name**</span></span>|<span data-ttu-id="559a4-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="559a4-111">**Required/Optional**</span></span>|<span data-ttu-id="559a4-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="559a4-112">**Data Type**</span></span>|<span data-ttu-id="559a4-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="559a4-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="559a4-114">_binary number1_</span><span class="sxs-lookup"><span data-stu-id="559a4-114">_binary number1_</span></span> <br/> |<span data-ttu-id="559a4-115">Обязательна</span><span class="sxs-lookup"><span data-stu-id="559a4-115">Required</span></span>  <br/> |<span data-ttu-id="559a4-116">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="559a4-116">**Numeric**</span></span> <br/> |<span data-ttu-id="559a4-117">Первый 16-битный двоичный номер.</span><span class="sxs-lookup"><span data-stu-id="559a4-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="559a4-118">_binary number2_</span><span class="sxs-lookup"><span data-stu-id="559a4-118">_binary number2_</span></span> <br/> |<span data-ttu-id="559a4-119">Обязательна</span><span class="sxs-lookup"><span data-stu-id="559a4-119">Required</span></span>  <br/> |<span data-ttu-id="559a4-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="559a4-120">**Numeric**</span></span> <br/> |<span data-ttu-id="559a4-121">Второй 16-битный двоичный номер.</span><span class="sxs-lookup"><span data-stu-id="559a4-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="559a4-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="559a4-122">Return value</span></span>

<span data-ttu-id="559a4-123">16-битный двоичный файл</span><span class="sxs-lookup"><span data-stu-id="559a4-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="559a4-124">Пример</span><span class="sxs-lookup"><span data-stu-id="559a4-124">Example</span></span>

<span data-ttu-id="559a4-125">BITXOR(12,6)</span><span class="sxs-lookup"><span data-stu-id="559a4-125">BITXOR(12,6)</span></span>
  
<span data-ttu-id="559a4-126">Возвращает 10.</span><span class="sxs-lookup"><span data-stu-id="559a4-126">Returns 10.</span></span> <span data-ttu-id="559a4-127">12 = 0...01100.</span><span class="sxs-lookup"><span data-stu-id="559a4-127">The 12 = 0...01100.</span></span> <span data-ttu-id="559a4-128">6 = 0...00110.</span><span class="sxs-lookup"><span data-stu-id="559a4-128">The 6 = 0...00110.</span></span> <span data-ttu-id="559a4-129">Таким образом, BITXOR(12,6) = 0...01010.</span><span class="sxs-lookup"><span data-stu-id="559a4-129">Therefore, BITXOR(12,6) = 0...01010.</span></span>
  

