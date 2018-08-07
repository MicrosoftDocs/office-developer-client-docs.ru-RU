---
title: Функция BITNOT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251399
localization_priority: Normal
ms.assetid: 7b6486bb-3618-3747-4b00-93bd55767c1c
description: Возвращает 16-разрядный двоичное число, в котором каждый бит равен 1 только в том случае, если соответствующий бит в двоичное число равняется 0. В противном случае бит равен 0.
ms.openlocfilehash: 0806e7c52cab659a09d27a60efb9c09aa436fb92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813225"
---
# <a name="bitnot-function"></a><span data-ttu-id="4aa6a-104">Функция BITNOT</span><span class="sxs-lookup"><span data-stu-id="4aa6a-104">BITNOT Function</span></span>

<span data-ttu-id="4aa6a-105">Возвращает 16-разрядный двоичное число, в котором каждый бит равен 1 только в том случае, если соответствующий бит в двоичное число равняется 0.</span><span class="sxs-lookup"><span data-stu-id="4aa6a-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in binary number is 0.</span></span> <span data-ttu-id="4aa6a-106">В противном случае бит равен 0.</span><span class="sxs-lookup"><span data-stu-id="4aa6a-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="4aa6a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4aa6a-107">Syntax</span></span>

<span data-ttu-id="4aa6a-108">BITNOT (** *двоичное число* **)</span><span class="sxs-lookup"><span data-stu-id="4aa6a-108">BITNOT(** *binary number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4aa6a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4aa6a-109">Parameters</span></span>

|<span data-ttu-id="4aa6a-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="4aa6a-110">**Name**</span></span>|<span data-ttu-id="4aa6a-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="4aa6a-111">**Required/Optional**</span></span>|<span data-ttu-id="4aa6a-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="4aa6a-112">**Data Type**</span></span>|<span data-ttu-id="4aa6a-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4aa6a-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4aa6a-114">_двоичное число_</span><span class="sxs-lookup"><span data-stu-id="4aa6a-114">_binary number_</span></span> <br/> |<span data-ttu-id="4aa6a-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4aa6a-115">Required</span></span>  <br/> |<span data-ttu-id="4aa6a-116">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="4aa6a-116">**Numeric**</span></span> <br/> |<span data-ttu-id="4aa6a-117">16-разрядное двоичное число.</span><span class="sxs-lookup"><span data-stu-id="4aa6a-117">A 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4aa6a-118">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="4aa6a-118">Return value</span></span>

<span data-ttu-id="4aa6a-119">16-разрядный двоичный</span><span class="sxs-lookup"><span data-stu-id="4aa6a-119">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="4aa6a-120">Пример</span><span class="sxs-lookup"><span data-stu-id="4aa6a-120">Example</span></span>

<span data-ttu-id="4aa6a-121">BITNOT(6)</span><span class="sxs-lookup"><span data-stu-id="4aa6a-121">BITNOT(6)</span></span>
  
<span data-ttu-id="4aa6a-122">Возвращает 65529.</span><span class="sxs-lookup"><span data-stu-id="4aa6a-122">Returns 65529.</span></span> <span data-ttu-id="4aa6a-123">6 = 0... 00110.</span><span class="sxs-lookup"><span data-stu-id="4aa6a-123">The 6 = 0...00110.</span></span> <span data-ttu-id="4aa6a-124">Таким образом, BITNOT(6) = 1... 11001.</span><span class="sxs-lookup"><span data-stu-id="4aa6a-124">Therefore, BITNOT(6) = 1...11001.</span></span>
  

