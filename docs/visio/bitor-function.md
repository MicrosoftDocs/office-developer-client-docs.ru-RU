---
title: Функция BITOR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251400
localization_priority: Normal
ms.assetid: 1d0954c5-b2cb-6c5d-62b3-a68011cf0c85
description: Возвращает 16-разрядный двоичное число, в котором каждый бит задано значение 1, если соответствующий бит в двоичные Число1 или двоичные число2 — 1. Только в том случае, если соответствующий бит равен 0 в двоичные Число1 и число2 двоичный бит имеет значение 0.
ms.openlocfilehash: db9808f16b32776149abbddf882310c02268cec3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813242"
---
# <a name="bitor-function"></a><span data-ttu-id="745fc-104">Функция BITOR</span><span class="sxs-lookup"><span data-stu-id="745fc-104">BITOR Function</span></span>

<span data-ttu-id="745fc-105">Возвращает 16-разрядный двоичное число, в котором каждый бит задано значение 1, если соответствующий бит в *двоичные Число1* или *двоичные число2* — 1.</span><span class="sxs-lookup"><span data-stu-id="745fc-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either  *binary number1*  or  *binary number2*  is 1.</span></span> <span data-ttu-id="745fc-106">Только в том случае, если соответствующий бит равен 0 в *двоичные Число1* и *число2 двоичный* бит имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="745fc-106">The bit is set to 0 only if the corresponding bit is 0 in both  *binary number1*  and  *binary number2*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="745fc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="745fc-107">Syntax</span></span>

<span data-ttu-id="745fc-108">BITOR (** *двоичные Число1* **, ** *двоичные число2* **)</span><span class="sxs-lookup"><span data-stu-id="745fc-108">BITOR(** *binary number1* **, ** *binary number2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="745fc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="745fc-109">Parameters</span></span>

|<span data-ttu-id="745fc-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="745fc-110">**Name**</span></span>|<span data-ttu-id="745fc-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="745fc-111">**Required/Optional**</span></span>|<span data-ttu-id="745fc-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="745fc-112">**Data Type**</span></span>|<span data-ttu-id="745fc-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="745fc-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="745fc-114">_двоичные Число1_</span><span class="sxs-lookup"><span data-stu-id="745fc-114">_binary number1_</span></span> <br/> |<span data-ttu-id="745fc-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="745fc-115">Required</span></span>  <br/> |<span data-ttu-id="745fc-116">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="745fc-116">**Numeric**</span></span> <br/> |<span data-ttu-id="745fc-117">Первый номер двоичные 16-разрядной.</span><span class="sxs-lookup"><span data-stu-id="745fc-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="745fc-118">_двоичные число2_</span><span class="sxs-lookup"><span data-stu-id="745fc-118">_binary number2_</span></span> <br/> |<span data-ttu-id="745fc-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="745fc-119">Required</span></span>  <br/> |<span data-ttu-id="745fc-120">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="745fc-120">**Numeric**</span></span> <br/> |<span data-ttu-id="745fc-121">Второй 16-разрядное число двоичные.</span><span class="sxs-lookup"><span data-stu-id="745fc-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="745fc-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2">Return value</span></span>

<span data-ttu-id="745fc-123">16-разрядный двоичный</span><span class="sxs-lookup"><span data-stu-id="745fc-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="745fc-124">Пример</span><span class="sxs-lookup"><span data-stu-id="745fc-124">Example</span></span>

<span data-ttu-id="745fc-125">BITOR(12,6)</span><span class="sxs-lookup"><span data-stu-id="745fc-125">BITOR(12,6)</span></span>
  
<span data-ttu-id="745fc-126">Возвращает 14.</span><span class="sxs-lookup"><span data-stu-id="745fc-126">Returns 14.</span></span> <span data-ttu-id="745fc-127">12 = 0... 01100.</span><span class="sxs-lookup"><span data-stu-id="745fc-127">The 12 = 0...01100.</span></span> <span data-ttu-id="745fc-128">6 = 0... 00110.</span><span class="sxs-lookup"><span data-stu-id="745fc-128">The 6 = 0...00110.</span></span> <span data-ttu-id="745fc-129">Таким образом, BITOR(12,6) = 0... 01110.</span><span class="sxs-lookup"><span data-stu-id="745fc-129">Therefore, BITOR(12,6) = 0...01110.</span></span>
  

