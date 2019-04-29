---
title: Функция substring (пользовательское веб-приложение для Access)
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
# <a name="substring-function-access-custom-web-app"></a><span data-ttu-id="d3646-103">Функция substring (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="d3646-103">SubString Function (Access custom web app)</span></span>

<span data-ttu-id="d3646-104">Возвращает часть текстового выражения.</span><span class="sxs-lookup"><span data-stu-id="d3646-104">Returns part of a text expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d3646-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d3646-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="d3646-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="d3646-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d3646-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3646-107">Syntax</span></span>

 <span data-ttu-id="d3646-108">\*\*\*\* Подстрока (*Текстекспрессион*, *Начало*, *Длина*)</span><span class="sxs-lookup"><span data-stu-id="d3646-108">**SubString** (*TextExpression*, *Start*, *Length*)</span></span> 
  
<span data-ttu-id="d3646-109">Функция **substring** содержит следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="d3646-109">The **SubString** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="d3646-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="d3646-110">**Argument name**</span></span>|<span data-ttu-id="d3646-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d3646-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d3646-112">*Текстекспрессион*</span><span class="sxs-lookup"><span data-stu-id="d3646-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="d3646-113">Текстовое выражение.</span><span class="sxs-lookup"><span data-stu-id="d3646-113">A text expression.</span></span>  <br/> |
| <span data-ttu-id="d3646-114">*Start*</span><span class="sxs-lookup"><span data-stu-id="d3646-114">*Start*</span></span>  <br/> |<span data-ttu-id="d3646-115">Целочисленное выражение, задающее начало возвращаемых символов.</span><span class="sxs-lookup"><span data-stu-id="d3646-115">An integer expression that specifies where the returned characters start.</span></span> <span data-ttu-id="d3646-116">Если значение start меньше 1, возвращаемое выражение будет начинаться с первого символа, указанного в выражении.</span><span class="sxs-lookup"><span data-stu-id="d3646-116">If start is less than 1, the returned expression will begin at the first character that is specified in expression.</span></span> <span data-ttu-id="d3646-117">В этом случае число возвращаемых символов является наибольшим значением суммы start + length-1 или 0.</span><span class="sxs-lookup"><span data-stu-id="d3646-117">In this case, the number of characters that are returned is the largest value of either the sum of start + length- 1 or 0.</span></span> <span data-ttu-id="d3646-118">Если значение Start больше, чем число символов в выражении value, возвращается выражение нулевой длины.</span><span class="sxs-lookup"><span data-stu-id="d3646-118">If start is greater than the number of characters in the value expression, a zero-length expression is returned.</span></span>  <br/> |
| <span data-ttu-id="d3646-119">*Length*</span><span class="sxs-lookup"><span data-stu-id="d3646-119">*Length*</span></span>  <br/> |<span data-ttu-id="d3646-120">Положительное целое число, определяющее, сколько символов в выражении будет возвращено.</span><span class="sxs-lookup"><span data-stu-id="d3646-120">A positive integer expression that specifies how many characters of the expression will be returned.</span></span> <span data-ttu-id="d3646-121">Если длина имеет отрицательное значение, возникает ошибка и оператор завершается.</span><span class="sxs-lookup"><span data-stu-id="d3646-121">If length is negative, an error is generated and the statement is terminated.</span></span> <span data-ttu-id="d3646-122">Если сумма начала и длина больше, чем число символов в выражении, возвращается выражение целого значения, начинающееся с Start.</span><span class="sxs-lookup"><span data-stu-id="d3646-122">If the sum of start and length is greater than the number of characters in expression, the whole value expression beginning at start is returned.</span></span>  <br/> |
   

