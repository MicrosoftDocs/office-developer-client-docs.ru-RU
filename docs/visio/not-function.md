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
description: Возвращает значение истина (1), если логикалекспрессион имеет значение FALSE. В противном случае возвращается значение FALSE (0).
ms.openlocfilehash: 3359e21654bcc318caf31405093f851eca064119
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341141"
---
# <a name="not-function"></a><span data-ttu-id="eb18e-104">Функция NOT</span><span class="sxs-lookup"><span data-stu-id="eb18e-104">NOT Function</span></span>

<span data-ttu-id="eb18e-105">Возвращает значение истина (1), если _логикалекспрессион_ имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="eb18e-105">Returns TRUE (1) if  _logicalexpression_ is FALSE.</span></span> <span data-ttu-id="eb18e-106">В противном случае возвращается значение FALSE (0).</span><span class="sxs-lookup"><span data-stu-id="eb18e-106">Otherwise, it returns FALSE (0).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="eb18e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb18e-107">Syntax</span></span>

<span data-ttu-id="eb18e-108">НЕТ (\* \* *логикалекспрессион* \* \*)</span><span class="sxs-lookup"><span data-stu-id="eb18e-108">NOT(\*\* *logicalexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="eb18e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="eb18e-109">Parameters</span></span>

|<span data-ttu-id="eb18e-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="eb18e-110">**Name**</span></span>|<span data-ttu-id="eb18e-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="eb18e-111">**Required/Optional**</span></span>|<span data-ttu-id="eb18e-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="eb18e-112">**Data Type**</span></span>|<span data-ttu-id="eb18e-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="eb18e-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="eb18e-114">_логикалекспрессион_</span><span class="sxs-lookup"><span data-stu-id="eb18e-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="eb18e-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="eb18e-115">Required</span></span>  <br/> |<span data-ttu-id="eb18e-116">**String**</span><span class="sxs-lookup"><span data-stu-id="eb18e-116">**String**</span></span> <br/> |<span data-ttu-id="eb18e-117">Логическое выражение для оценки.</span><span class="sxs-lookup"><span data-stu-id="eb18e-117">The logical expression to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="eb18e-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eb18e-118">Return value</span></span>

<span data-ttu-id="eb18e-119">Boolean</span><span class="sxs-lookup"><span data-stu-id="eb18e-119">Boolean</span></span>
  
## <a name="example"></a><span data-ttu-id="eb18e-120">Пример</span><span class="sxs-lookup"><span data-stu-id="eb18e-120">Example</span></span>

<span data-ttu-id="eb18e-121">НЕТ (высота \> 0,75)</span><span class="sxs-lookup"><span data-stu-id="eb18e-121">NOT(Height \> 0.75 in)</span></span> 
  
<span data-ttu-id="eb18e-122">Возвращает 1, если высота меньше или равна 0,75 сантиметра.</span><span class="sxs-lookup"><span data-stu-id="eb18e-122">Returns 1 if Height is less than or equal to 0.75 inches.</span></span> <span data-ttu-id="eb18e-123">Возвращает значение 0, если высота превышает 0,75 дюймов.</span><span class="sxs-lookup"><span data-stu-id="eb18e-123">Returns 0 if Height is greater than 0.75 inches.</span></span> 
  

