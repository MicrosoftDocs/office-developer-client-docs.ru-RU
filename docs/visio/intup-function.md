---
title: Функция INTUP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251446
localization_priority: Normal
ms.assetid: ce193ce1-c7fd-6609-ad37-a3a28b30a1bd
description: Округлит число до следующей очереди.
ms.openlocfilehash: 405345ae1d22d599df85e2a640445c8c681ec2f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416141"
---
# <a name="intup-function"></a><span data-ttu-id="ad8d8-103">Функция INTUP</span><span class="sxs-lookup"><span data-stu-id="ad8d8-103">INTUP Function</span></span>

<span data-ttu-id="ad8d8-104">Округлит число до следующей очереди.</span><span class="sxs-lookup"><span data-stu-id="ad8d8-104">Rounds a number up to the next integer.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ad8d8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad8d8-105">Syntax</span></span>

<span data-ttu-id="ad8d8-106">INTUP(\*\* *number* \*\* )</span><span class="sxs-lookup"><span data-stu-id="ad8d8-106">INTUP(\*\* *number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ad8d8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad8d8-107">Parameters</span></span>

|<span data-ttu-id="ad8d8-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ad8d8-108">**Name**</span></span>|<span data-ttu-id="ad8d8-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="ad8d8-109">**Required/Optional**</span></span>|<span data-ttu-id="ad8d8-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="ad8d8-110">**Data Type**</span></span>|<span data-ttu-id="ad8d8-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ad8d8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ad8d8-112">_число_</span><span class="sxs-lookup"><span data-stu-id="ad8d8-112">_number_</span></span> <br/> |<span data-ttu-id="ad8d8-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ad8d8-113">Required</span></span>  <br/> |<span data-ttu-id="ad8d8-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="ad8d8-114">**Number**</span></span> <br/> |<span data-ttu-id="ad8d8-115">Номер, который нужно округить.</span><span class="sxs-lookup"><span data-stu-id="ad8d8-115">The number to round up.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="ad8d8-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ad8d8-116">Example 1</span></span>

<span data-ttu-id="ad8d8-117">INTUP (3.2)</span><span class="sxs-lookup"><span data-stu-id="ad8d8-117">INTUP(3.2)</span></span>
  
<span data-ttu-id="ad8d8-118">Возвращает 4.</span><span class="sxs-lookup"><span data-stu-id="ad8d8-118">Returns 4.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ad8d8-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ad8d8-119">Example 2</span></span>

<span data-ttu-id="ad8d8-120">INTUP(-3.2)</span><span class="sxs-lookup"><span data-stu-id="ad8d8-120">INTUP(-3.2)</span></span>
  
<span data-ttu-id="ad8d8-121">Возвращает -3.</span><span class="sxs-lookup"><span data-stu-id="ad8d8-121">Returns -3.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ad8d8-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ad8d8-122">Example 3</span></span>

<span data-ttu-id="ad8d8-123">INTUP(3)</span><span class="sxs-lookup"><span data-stu-id="ad8d8-123">INTUP(3)</span></span>
  
<span data-ttu-id="ad8d8-124">Возвращает 3.</span><span class="sxs-lookup"><span data-stu-id="ad8d8-124">Returns 3.</span></span>
  

