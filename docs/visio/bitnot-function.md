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
description: Возвращает 16-разрядное двоичное число, для каждого бита которого задано значение 1, только если соответствующий бит в двоичном числе равен 0. В противном случае для бита задается значение 0.
ms.openlocfilehash: 34ea6fd614feae8e3c8e97e34b7ff6c531f4c123
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330011"
---
# <a name="bitnot-function"></a><span data-ttu-id="fd5cc-104">Функция BITNOT</span><span class="sxs-lookup"><span data-stu-id="fd5cc-104">BITNOT Function</span></span>

<span data-ttu-id="fd5cc-105">Возвращает 16-разрядное двоичное число, для каждого бита которого задано значение 1, только если соответствующий бит в двоичном числе равен 0.</span><span class="sxs-lookup"><span data-stu-id="fd5cc-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in binary number is 0.</span></span> <span data-ttu-id="fd5cc-106">В противном случае для бита задается значение 0.</span><span class="sxs-lookup"><span data-stu-id="fd5cc-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fd5cc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd5cc-107">Syntax</span></span>

<span data-ttu-id="fd5cc-108">BITNOT (\* \* *двоичное число* \* \*)</span><span class="sxs-lookup"><span data-stu-id="fd5cc-108">BITNOT(\*\* *binary number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fd5cc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd5cc-109">Parameters</span></span>

|<span data-ttu-id="fd5cc-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="fd5cc-110">**Name**</span></span>|<span data-ttu-id="fd5cc-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="fd5cc-111">**Required/Optional**</span></span>|<span data-ttu-id="fd5cc-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="fd5cc-112">**Data Type**</span></span>|<span data-ttu-id="fd5cc-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fd5cc-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fd5cc-114">_двоичное число_</span><span class="sxs-lookup"><span data-stu-id="fd5cc-114">_binary number_</span></span> <br/> |<span data-ttu-id="fd5cc-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fd5cc-115">Required</span></span>  <br/> |<span data-ttu-id="fd5cc-116">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="fd5cc-116">**Numeric**</span></span> <br/> |<span data-ttu-id="fd5cc-117">16 – разрядное двоичное число.</span><span class="sxs-lookup"><span data-stu-id="fd5cc-117">A 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fd5cc-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd5cc-118">Return value</span></span>

<span data-ttu-id="fd5cc-119">16 – разрядный двоичный</span><span class="sxs-lookup"><span data-stu-id="fd5cc-119">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="fd5cc-120">Пример</span><span class="sxs-lookup"><span data-stu-id="fd5cc-120">Example</span></span>

<span data-ttu-id="fd5cc-121">BITNOT (6)</span><span class="sxs-lookup"><span data-stu-id="fd5cc-121">BITNOT(6)</span></span>
  
<span data-ttu-id="fd5cc-122">Возвращает 65529.</span><span class="sxs-lookup"><span data-stu-id="fd5cc-122">Returns 65529.</span></span> <span data-ttu-id="fd5cc-123">6 = 0... 00110.</span><span class="sxs-lookup"><span data-stu-id="fd5cc-123">The 6 = 0...00110.</span></span> <span data-ttu-id="fd5cc-124">Таким образом, BITNOT (6) = 1... 11001.</span><span class="sxs-lookup"><span data-stu-id="fd5cc-124">Therefore, BITNOT(6) = 1...11001.</span></span>
  

