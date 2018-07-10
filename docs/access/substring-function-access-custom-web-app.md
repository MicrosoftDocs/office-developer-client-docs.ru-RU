---
title: Функция подстроки (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Возвращает выражение текста.
ms.openlocfilehash: 49d9afefe4b25d91738e518e0ddb2b902067c038
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807129"
---
# <a name="substring-function-access-custom-web-app"></a><span data-ttu-id="36b31-103">Функция подстроки (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="36b31-103">SubString Function (Access custom web app)</span></span>

<span data-ttu-id="36b31-104">Возвращает выражение текста.</span><span class="sxs-lookup"><span data-stu-id="36b31-104">Returns part of a text expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="36b31-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="36b31-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="36b31-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="36b31-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ru-ru/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="36b31-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36b31-107">Syntax</span></span>

 <span data-ttu-id="36b31-108">**Подстроки** (*TextExpression*, *запустите*, *Длина*)</span><span class="sxs-lookup"><span data-stu-id="36b31-108">**SubString** (*TextExpression*, *Start*, *Length*)</span></span> 
  
<span data-ttu-id="36b31-109">Функция **подстроки** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="36b31-109">The **SubString** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="36b31-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="36b31-110">**Argument name**</span></span>|<span data-ttu-id="36b31-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="36b31-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="36b31-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="36b31-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="36b31-113">Выражение текста.</span><span class="sxs-lookup"><span data-stu-id="36b31-113">A text expression.</span></span>  <br/> |
| <span data-ttu-id="36b31-114">*Start*</span><span class="sxs-lookup"><span data-stu-id="36b31-114">*Start*</span></span>  <br/> |<span data-ttu-id="36b31-115">Выражение целое число, указывающее, начинается возвращаемых символов.</span><span class="sxs-lookup"><span data-stu-id="36b31-115">An integer expression that specifies where the returned characters start.</span></span> <span data-ttu-id="36b31-116">Если запустить меньше 1, возвращаемое выражение начнется в первый символ, который указан в выражении.</span><span class="sxs-lookup"><span data-stu-id="36b31-116">If start is less than 1, the returned expression will begin at the first character that is specified in expression.</span></span> <span data-ttu-id="36b31-117">В этом случае число символов, возвращаемых — наибольшее значение суммы Пуск + длина-1 или 0.</span><span class="sxs-lookup"><span data-stu-id="36b31-117">In this case, the number of characters that are returned is the largest value of either the sum of start + length- 1 or 0.</span></span> <span data-ttu-id="36b31-118">Если start больше, чем количество символов в выражении значение, возвращается нулевой длины выражения.</span><span class="sxs-lookup"><span data-stu-id="36b31-118">If start is greater than the number of characters in the value expression, a zero-length expression is returned.</span></span>  <br/> |
| <span data-ttu-id="36b31-119">*Длина*</span><span class="sxs-lookup"><span data-stu-id="36b31-119">*Length*</span></span>  <br/> |<span data-ttu-id="36b31-120">Выражение положительное целое число, указывающее, сколько символов выражения будет возвращено.</span><span class="sxs-lookup"><span data-stu-id="36b31-120">A positive integer expression that specifies how many characters of the expression will be returned.</span></span> <span data-ttu-id="36b31-121">Если длина отрицательно, возникает ошибка, и оператор завершается.</span><span class="sxs-lookup"><span data-stu-id="36b31-121">If length is negative, an error is generated and the statement is terminated.</span></span> <span data-ttu-id="36b31-122">Если сумма start и длины больше, чем количество символов в выражении, возвращается всего значения выражения, начиная с начала.</span><span class="sxs-lookup"><span data-stu-id="36b31-122">If the sum of start and length is greater than the number of characters in expression, the whole value expression beginning at start is returned.</span></span>  <br/> |
   

