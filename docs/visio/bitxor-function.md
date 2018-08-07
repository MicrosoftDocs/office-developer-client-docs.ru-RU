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
description: Возвращает 16-разрядный двоичное число, в котором каждый бит задано значение 1, если соответствующий бит в либо, но не оба двоичные Число1 и число2 двоичные 1. В противном случае бит равен 0.
ms.openlocfilehash: a0e03258bcfe694dc3bec5469095eff90fb94f1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813261"
---
# <a name="bitxor-function"></a><span data-ttu-id="f1c95-104">Функция BITXOR</span><span class="sxs-lookup"><span data-stu-id="f1c95-104">BITXOR Function</span></span>

<span data-ttu-id="f1c95-105">Возвращает 16-разрядный двоичное число, в котором каждый бит задано значение 1, если соответствующий бит в либо, но не оба двоичные Число1 и число2 двоичные 1.</span><span class="sxs-lookup"><span data-stu-id="f1c95-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either but not both binary number1 and binary number2 is 1.</span></span> <span data-ttu-id="f1c95-106">В противном случае бит равен 0.</span><span class="sxs-lookup"><span data-stu-id="f1c95-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f1c95-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1c95-107">Syntax</span></span>

<span data-ttu-id="f1c95-108">BITXOR (** *двоичные Число1* **, ** *двоичные число2* **)</span><span class="sxs-lookup"><span data-stu-id="f1c95-108">BITXOR(** *binary number1* **, ** *binary number2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f1c95-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1c95-109">Parameters</span></span>

|<span data-ttu-id="f1c95-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="f1c95-110">**Name**</span></span>|<span data-ttu-id="f1c95-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="f1c95-111">**Required/Optional**</span></span>|<span data-ttu-id="f1c95-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="f1c95-112">**Data Type**</span></span>|<span data-ttu-id="f1c95-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f1c95-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f1c95-114">_двоичные Число1_</span><span class="sxs-lookup"><span data-stu-id="f1c95-114">_binary number1_</span></span> <br/> |<span data-ttu-id="f1c95-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f1c95-115">Required</span></span>  <br/> |<span data-ttu-id="f1c95-116">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="f1c95-116">**Numeric**</span></span> <br/> |<span data-ttu-id="f1c95-117">Первый номер двоичные 16-разрядной.</span><span class="sxs-lookup"><span data-stu-id="f1c95-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="f1c95-118">_двоичные число2_</span><span class="sxs-lookup"><span data-stu-id="f1c95-118">_binary number2_</span></span> <br/> |<span data-ttu-id="f1c95-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f1c95-119">Required</span></span>  <br/> |<span data-ttu-id="f1c95-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="f1c95-120">**Numeric**</span></span> <br/> |<span data-ttu-id="f1c95-121">Второй 16-разрядное число двоичные.</span><span class="sxs-lookup"><span data-stu-id="f1c95-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f1c95-122">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="f1c95-122">Return value</span></span>

<span data-ttu-id="f1c95-123">16-разрядный двоичный</span><span class="sxs-lookup"><span data-stu-id="f1c95-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="f1c95-124">Пример</span><span class="sxs-lookup"><span data-stu-id="f1c95-124">Example</span></span>

<span data-ttu-id="f1c95-125">BITXOR(12,6)</span><span class="sxs-lookup"><span data-stu-id="f1c95-125">BITXOR(12,6)</span></span>
  
<span data-ttu-id="f1c95-126">Возвращает значение 10.</span><span class="sxs-lookup"><span data-stu-id="f1c95-126">Returns 10.</span></span> <span data-ttu-id="f1c95-127">12 = 0... 01100.</span><span class="sxs-lookup"><span data-stu-id="f1c95-127">The 12 = 0...01100.</span></span> <span data-ttu-id="f1c95-128">6 = 0... 00110.</span><span class="sxs-lookup"><span data-stu-id="f1c95-128">The 6 = 0...00110.</span></span> <span data-ttu-id="f1c95-129">Таким образом, BITXOR(12,6) = 0... 01010.</span><span class="sxs-lookup"><span data-stu-id="f1c95-129">Therefore, BITXOR(12,6) = 0...01010.</span></span>
  

