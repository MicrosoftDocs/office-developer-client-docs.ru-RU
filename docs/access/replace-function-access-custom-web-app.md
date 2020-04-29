---
title: Функция Replace (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 93c8fc1d-e70c-4726-af2f-c6501d82e49b
description: Заменяет все вхождения указанного строкового значения другим строковым значением.
ms.openlocfilehash: 678cf88fe66d65be454613ce2c615bb7cb8f66d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421034"
---
# <a name="replace-function-access-custom-web-app"></a><span data-ttu-id="d2249-103">Функция Replace (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="d2249-103">Replace Function (Access custom web app)</span></span>

<span data-ttu-id="d2249-104">Заменяет все вхождения указанного строкового значения другим строковым значением.</span><span class="sxs-lookup"><span data-stu-id="d2249-104">Replaces all occurrences of a specified string value with another string value.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d2249-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d2249-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="d2249-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="d2249-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d2249-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2249-107">Syntax</span></span>

 <span data-ttu-id="d2249-108">**Replace** (*текстекспрессион*, *pattern*, *replacement*)</span><span class="sxs-lookup"><span data-stu-id="d2249-108">**Replace** (*TextExpression*, *Pattern*, *Replacement*)</span></span> 
  
<span data-ttu-id="d2249-109">Функция **Replace** содержит следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="d2249-109">The **Replace** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="d2249-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="d2249-110">**Argument name**</span></span>|<span data-ttu-id="d2249-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d2249-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d2249-112">*текстекспрессион*</span><span class="sxs-lookup"><span data-stu-id="d2249-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="d2249-113">Строковое выражение, в котором выполняется поиск.</span><span class="sxs-lookup"><span data-stu-id="d2249-113">The string expression to be searched.</span></span>  <br/> |
| <span data-ttu-id="d2249-114">*Pattern*</span><span class="sxs-lookup"><span data-stu-id="d2249-114">*Pattern*</span></span>  <br/> |<span data-ttu-id="d2249-115">Подстрока, которую необходимо найти.</span><span class="sxs-lookup"><span data-stu-id="d2249-115">The substring to be found.</span></span>  <span data-ttu-id="d2249-116">*Шаблон* не может быть пустой строкой ("").</span><span class="sxs-lookup"><span data-stu-id="d2249-116">*Pattern*  cannot be an empty string ("").</span></span>  <br/> |
| <span data-ttu-id="d2249-117">*Replacement*</span><span class="sxs-lookup"><span data-stu-id="d2249-117">*Replacement*</span></span>  <br/> |<span data-ttu-id="d2249-118">Строка замены.</span><span class="sxs-lookup"><span data-stu-id="d2249-118">The replacement string.</span></span>  <br/> |
   

