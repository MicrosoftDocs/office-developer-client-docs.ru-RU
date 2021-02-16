---
title: Функция CharIndex (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Выполняет поиск текстового выражения для другого текстового выражения и при его обнаружении возвращает его начальное положение.
ms.openlocfilehash: dc6906f70bc5bb17e12855d69946281909962988
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423134"
---
# <a name="charindex-function-access-custom-web-app"></a><span data-ttu-id="1f8b0-103">Функция CharIndex (пользовательское веб-приложение Access)</span><span class="sxs-lookup"><span data-stu-id="1f8b0-103">CharIndex function (Access custom web app)</span></span>

<span data-ttu-id="1f8b0-104">Выполняет поиск текстового выражения для другого текстового выражения и возвращает его начальное положение при обнаружении.</span><span class="sxs-lookup"><span data-stu-id="1f8b0-104">Searches a text expression for another text expression and returns its starting position if found.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="1f8b0-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="1f8b0-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="1f8b0-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="1f8b0-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1f8b0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f8b0-107">Syntax</span></span>

<span data-ttu-id="1f8b0-108">**CharIndex** (*TextExpression*, *WithinText*, [*Start*])</span><span class="sxs-lookup"><span data-stu-id="1f8b0-108">**CharIndex** (*TextExpression*, *WithinText*, [*Start*])</span></span> 
  
|<span data-ttu-id="1f8b0-109">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="1f8b0-109">**Argument Name**</span></span>|<span data-ttu-id="1f8b0-110">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="1f8b0-110">**Required**</span></span>|<span data-ttu-id="1f8b0-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1f8b0-111">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="1f8b0-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="1f8b0-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="1f8b0-113">Да</span><span class="sxs-lookup"><span data-stu-id="1f8b0-113">Yes</span></span>  <br/> |<span data-ttu-id="1f8b0-114">Текстовое выражение, содержаное текст, который необходимо найти.</span><span class="sxs-lookup"><span data-stu-id="1f8b0-114">A text expression that contains the text to be found.</span></span>  <br/> |
| <span data-ttu-id="1f8b0-115">*WithinText*</span><span class="sxs-lookup"><span data-stu-id="1f8b0-115">*WithinText*</span></span>  <br/> |<span data-ttu-id="1f8b0-116">Да</span><span class="sxs-lookup"><span data-stu-id="1f8b0-116">Yes</span></span>  <br/> |<span data-ttu-id="1f8b0-117">Текстовое выражение для поиска.</span><span class="sxs-lookup"><span data-stu-id="1f8b0-117">The text expression to be searched.</span></span>  <br/> |
| <span data-ttu-id="1f8b0-118">*Начало*</span><span class="sxs-lookup"><span data-stu-id="1f8b0-118">*Start*</span></span>  <br/> |<span data-ttu-id="1f8b0-119">Нет</span><span class="sxs-lookup"><span data-stu-id="1f8b0-119">No</span></span>  <br/> |<span data-ttu-id="1f8b0-120">Integer that specifies the location in  *WithinText*  to begin the search.</span><span class="sxs-lookup"><span data-stu-id="1f8b0-120">An integer that specifies the location in  *WithinText*  to begin the search.</span></span> <span data-ttu-id="1f8b0-121">Если *start* не указан, отрицательное число или 0, поиск начинается с начала *WithinText.*</span><span class="sxs-lookup"><span data-stu-id="1f8b0-121">If  *Start*  is not specified, is a negative number, or is 0, the search starts at the beginning of  *WithinText*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f8b0-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="1f8b0-122">Remarks</span></span>

<span data-ttu-id="1f8b0-123">Если  *textExpression или*  *WithinText*  имеет NULL,  *CharIndex*  возвращает NULL.</span><span class="sxs-lookup"><span data-stu-id="1f8b0-123">If either  *TextExpression*  or  *WithinText*  is NULL,  *CharIndex*  returns NULL.</span></span> 
  
<span data-ttu-id="1f8b0-124">Если  *textExpression*  не найден в  *WithinText,*  *CharIndex*  возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="1f8b0-124">If  *TextExpression*  is not found within  *WithinText*,  *CharIndex*  returns 0.</span></span> 
  
<span data-ttu-id="1f8b0-125">Возвращаемая начальная позиция основана на 1, а не на 0.</span><span class="sxs-lookup"><span data-stu-id="1f8b0-125">The starting position returned is 1-based, not 0-based.</span></span>
  

