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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413334"
---
# <a name="not-function"></a><span data-ttu-id="0deec-104">Функция NOT</span><span class="sxs-lookup"><span data-stu-id="0deec-104">NOT Function</span></span>

<span data-ttu-id="0deec-105">Возвращает значение истина (1), если _логикалекспрессион_ имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="0deec-105">Returns TRUE (1) if  _logicalexpression_ is FALSE.</span></span> <span data-ttu-id="0deec-106">В противном случае возвращается значение FALSE (0).</span><span class="sxs-lookup"><span data-stu-id="0deec-106">Otherwise, it returns FALSE (0).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0deec-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0deec-107">Syntax</span></span>

<span data-ttu-id="0deec-108">НЕТ (\* \* *логикалекспрессион* \* \*)</span><span class="sxs-lookup"><span data-stu-id="0deec-108">NOT(\*\* *logicalexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0deec-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0deec-109">Parameters</span></span>

|<span data-ttu-id="0deec-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="0deec-110">**Name**</span></span>|<span data-ttu-id="0deec-111">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="0deec-111">**Required/Optional**</span></span>|<span data-ttu-id="0deec-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="0deec-112">**Data Type**</span></span>|<span data-ttu-id="0deec-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0deec-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0deec-114">_логикалекспрессион_</span><span class="sxs-lookup"><span data-stu-id="0deec-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="0deec-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0deec-115">Required</span></span>  <br/> |<span data-ttu-id="0deec-116">**String**</span><span class="sxs-lookup"><span data-stu-id="0deec-116">**String**</span></span> <br/> |<span data-ttu-id="0deec-117">Логическое выражение для оценки.</span><span class="sxs-lookup"><span data-stu-id="0deec-117">The logical expression to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0deec-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0deec-118">Return value</span></span>

<span data-ttu-id="0deec-119">Boolean</span><span class="sxs-lookup"><span data-stu-id="0deec-119">Boolean</span></span>
  
## <a name="example"></a><span data-ttu-id="0deec-120">Пример</span><span class="sxs-lookup"><span data-stu-id="0deec-120">Example</span></span>

<span data-ttu-id="0deec-121">НЕТ (высота \> 0,75)</span><span class="sxs-lookup"><span data-stu-id="0deec-121">NOT(Height \> 0.75 in)</span></span> 
  
<span data-ttu-id="0deec-122">Возвращает 1, если высота меньше или равна 0,75 сантиметра.</span><span class="sxs-lookup"><span data-stu-id="0deec-122">Returns 1 if Height is less than or equal to 0.75 inches.</span></span> <span data-ttu-id="0deec-123">Возвращает значение 0, если высота превышает 0,75 дюймов.</span><span class="sxs-lookup"><span data-stu-id="0deec-123">Returns 0 if Height is greater than 0.75 inches.</span></span> 
  

