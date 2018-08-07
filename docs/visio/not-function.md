---
title: Функция NOT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251469
localization_priority: Normal
ms.assetid: 65873b32-2406-7c33-8e68-802461f467b2
description: Возвращает значение TRUE (1), если logicalexpression имеет значение FALSE. В противном случае возвращается значение FALSE (0).
ms.openlocfilehash: e2359aaab18469cd4f272f71aca8d899a12b2120
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814304"
---
# <a name="not-function"></a><span data-ttu-id="c0499-104">Функция NOT</span><span class="sxs-lookup"><span data-stu-id="c0499-104">NOT Function</span></span>

<span data-ttu-id="c0499-105">Возвращает значение TRUE (1), если _logicalexpression_ имеет значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="c0499-105">Returns TRUE (1) if  _logicalexpression_ is FALSE.</span></span> <span data-ttu-id="c0499-106">В противном случае возвращается значение FALSE (0).</span><span class="sxs-lookup"><span data-stu-id="c0499-106">Otherwise, it returns FALSE (0).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c0499-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0499-107">Syntax</span></span>

<span data-ttu-id="c0499-108">НЕ (** *logicalexpression* **)</span><span class="sxs-lookup"><span data-stu-id="c0499-108">NOT(** *logicalexpression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c0499-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0499-109">Parameters</span></span>

|<span data-ttu-id="c0499-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="c0499-110">**Name**</span></span>|<span data-ttu-id="c0499-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="c0499-111">**Required/Optional**</span></span>|<span data-ttu-id="c0499-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="c0499-112">**Data Type**</span></span>|<span data-ttu-id="c0499-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c0499-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c0499-114">_logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="c0499-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="c0499-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c0499-115">Required</span></span>  <br/> |<span data-ttu-id="c0499-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="c0499-116">**String**</span></span> <br/> |<span data-ttu-id="c0499-117">Логическое выражение для оценки.</span><span class="sxs-lookup"><span data-stu-id="c0499-117">The logical expression to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c0499-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8">Return value</span></span>

<span data-ttu-id="c0499-119">Логический</span><span class="sxs-lookup"><span data-stu-id="c0499-119">Boolean</span></span>
  
## <a name="example"></a><span data-ttu-id="c0499-120">Пример</span><span class="sxs-lookup"><span data-stu-id="c0499-120">Example</span></span>

<span data-ttu-id="c0499-121">НЕ (высота \> 0,75 in)</span><span class="sxs-lookup"><span data-stu-id="c0499-121">NOT(Height \> 0.75 in)</span></span> 
  
<span data-ttu-id="c0499-122">Возвращает значение 1, если высота — меньше или равно 0,75 дюйма.</span><span class="sxs-lookup"><span data-stu-id="c0499-122">Returns 1 if Height is less than or equal to 0.75 inches.</span></span> <span data-ttu-id="c0499-123">Возвращает 0, если высота больше, чем 0,75 дюйма.</span><span class="sxs-lookup"><span data-stu-id="c0499-123">Returns 0 if Height is greater than 0.75 inches.</span></span> 
  

