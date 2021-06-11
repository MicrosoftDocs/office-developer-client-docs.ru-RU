---
title: Функция subString (Доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Возвращает часть текстового выражения.
ms.openlocfilehash: af93620905af366f41bcc50ab6102114acd3db9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433474"
---
# <a name="substring-function-access-custom-web-app"></a><span data-ttu-id="dc39e-103">Функция subString (Доступ к настраиваемой веб-приложению)</span><span class="sxs-lookup"><span data-stu-id="dc39e-103">SubString Function (Access custom web app)</span></span>

<span data-ttu-id="dc39e-104">Возвращает часть текстового выражения.</span><span class="sxs-lookup"><span data-stu-id="dc39e-104">Returns part of a text expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="dc39e-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="dc39e-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="dc39e-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="dc39e-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="dc39e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc39e-107">Syntax</span></span>

 <span data-ttu-id="dc39e-108">**SubString** *(TextExpression*, *Start*, *Length*)</span><span class="sxs-lookup"><span data-stu-id="dc39e-108">**SubString** (*TextExpression*, *Start*, *Length*)</span></span> 
  
<span data-ttu-id="dc39e-109">Функция **SubString** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="dc39e-109">The **SubString** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="dc39e-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="dc39e-110">**Argument name**</span></span>|<span data-ttu-id="dc39e-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dc39e-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="dc39e-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="dc39e-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="dc39e-113">Текстовое выражение.</span><span class="sxs-lookup"><span data-stu-id="dc39e-113">A text expression.</span></span>  <br/> |
| <span data-ttu-id="dc39e-114">*Start*</span><span class="sxs-lookup"><span data-stu-id="dc39e-114">*Start*</span></span>  <br/> |<span data-ttu-id="dc39e-115">Integer expression that specifies where the returned characters start.</span><span class="sxs-lookup"><span data-stu-id="dc39e-115">An integer expression that specifies where the returned characters start.</span></span> <span data-ttu-id="dc39e-116">Если начало меньше 1, возвращаемая экспрессия начнется с первого символа, указанного в выражении.</span><span class="sxs-lookup"><span data-stu-id="dc39e-116">If start is less than 1, the returned expression will begin at the first character that is specified in expression.</span></span> <span data-ttu-id="dc39e-117">В этом случае количество возвращаемого символа является самым большим значением суммы начала + длины — 1 или 0.</span><span class="sxs-lookup"><span data-stu-id="dc39e-117">In this case, the number of characters that are returned is the largest value of either the sum of start + length- 1 or 0.</span></span> <span data-ttu-id="dc39e-118">Если начало больше количества символов в выражении значения, возвращается выражение нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="dc39e-118">If start is greater than the number of characters in the value expression, a zero-length expression is returned.</span></span>  <br/> |
| <span data-ttu-id="dc39e-119">*Length*</span><span class="sxs-lookup"><span data-stu-id="dc39e-119">*Length*</span></span>  <br/> |<span data-ttu-id="dc39e-120">Положительное integer выражение, которое указывает, сколько символов выражения будет возвращено.</span><span class="sxs-lookup"><span data-stu-id="dc39e-120">A positive integer expression that specifies how many characters of the expression will be returned.</span></span> <span data-ttu-id="dc39e-121">Если длина является отрицательной, создается ошибка и завершается утверждение.</span><span class="sxs-lookup"><span data-stu-id="dc39e-121">If length is negative, an error is generated and the statement is terminated.</span></span> <span data-ttu-id="dc39e-122">Если сумма начала и длины больше, чем количество символов в выражении, возвращается все выражение значения, начиная с начала.</span><span class="sxs-lookup"><span data-stu-id="dc39e-122">If the sum of start and length is greater than the number of characters in expression, the whole value expression beginning at start is returned.</span></span>  <br/> |
   

