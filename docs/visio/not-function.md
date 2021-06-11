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
description: Возвращает TRUE (1), если логическиеэкспрессии false. В противном случае возвращает FALSE (0).
ms.openlocfilehash: 3359e21654bcc318caf31405093f851eca064119
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413334"
---
# <a name="not-function"></a><span data-ttu-id="ed39c-104">Функция NOT</span><span class="sxs-lookup"><span data-stu-id="ed39c-104">NOT Function</span></span>

<span data-ttu-id="ed39c-105">Возвращает TRUE (1), если  _логическиеэкспрессии_ false.</span><span class="sxs-lookup"><span data-stu-id="ed39c-105">Returns TRUE (1) if  _logicalexpression_ is FALSE.</span></span> <span data-ttu-id="ed39c-106">В противном случае возвращает FALSE (0).</span><span class="sxs-lookup"><span data-stu-id="ed39c-106">Otherwise, it returns FALSE (0).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ed39c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed39c-107">Syntax</span></span>

<span data-ttu-id="ed39c-108">NOT(\*\* *logicalexpression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="ed39c-108">NOT(\*\* *logicalexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ed39c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed39c-109">Parameters</span></span>

|<span data-ttu-id="ed39c-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ed39c-110">**Name**</span></span>|<span data-ttu-id="ed39c-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="ed39c-111">**Required/Optional**</span></span>|<span data-ttu-id="ed39c-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="ed39c-112">**Data Type**</span></span>|<span data-ttu-id="ed39c-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ed39c-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ed39c-114">_logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="ed39c-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="ed39c-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ed39c-115">Required</span></span>  <br/> |<span data-ttu-id="ed39c-116">**String**</span><span class="sxs-lookup"><span data-stu-id="ed39c-116">**String**</span></span> <br/> |<span data-ttu-id="ed39c-117">Логическое выражение для оценки.</span><span class="sxs-lookup"><span data-stu-id="ed39c-117">The logical expression to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ed39c-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed39c-118">Return value</span></span>

<span data-ttu-id="ed39c-119">Boolean</span><span class="sxs-lookup"><span data-stu-id="ed39c-119">Boolean</span></span>
  
## <a name="example"></a><span data-ttu-id="ed39c-120">Пример</span><span class="sxs-lookup"><span data-stu-id="ed39c-120">Example</span></span>

<span data-ttu-id="ed39c-121">NOT (Высота \> 0,75 в)</span><span class="sxs-lookup"><span data-stu-id="ed39c-121">NOT(Height \> 0.75 in)</span></span> 
  
<span data-ttu-id="ed39c-122">Возвращает 1, если высота меньше или равна 0,75 дюйма.</span><span class="sxs-lookup"><span data-stu-id="ed39c-122">Returns 1 if Height is less than or equal to 0.75 inches.</span></span> <span data-ttu-id="ed39c-123">Возвращает 0, если высота больше 0,75 дюйма.</span><span class="sxs-lookup"><span data-stu-id="ed39c-123">Returns 0 if Height is greater than 0.75 inches.</span></span> 
  

