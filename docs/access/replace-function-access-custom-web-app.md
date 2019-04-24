---
title: Функция rePlace (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 93c8fc1d-e70c-4726-af2f-c6501d82e49b
description: Заменяет все вхождения указанного строкового значения другим строковым значением.
ms.openlocfilehash: 678cf88fe66d65be454613ce2c615bb7cb8f66d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308003"
---
# <a name="replace-function-access-custom-web-app"></a><span data-ttu-id="2102a-103">Функция rePlace (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="2102a-103">Replace Function (Access custom web app)</span></span>

<span data-ttu-id="2102a-104">Заменяет все вхождения указанного строкового значения другим строковым значением.</span><span class="sxs-lookup"><span data-stu-id="2102a-104">Replaces all occurrences of a specified string value with another string value.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="2102a-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="2102a-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="2102a-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="2102a-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2102a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2102a-107">Syntax</span></span>

 <span data-ttu-id="2102a-108">**Замена** (*Текстекспрессион*, *шаблон*, *Замена*)</span><span class="sxs-lookup"><span data-stu-id="2102a-108">**Replace** (*TextExpression*, *Pattern*, *Replacement*)</span></span> 
  
<span data-ttu-id="2102a-109">Функция **Replace** содержит следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="2102a-109">The **Replace** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="2102a-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="2102a-110">**Argument name**</span></span>|<span data-ttu-id="2102a-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2102a-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2102a-112">*Текстекспрессион*</span><span class="sxs-lookup"><span data-stu-id="2102a-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="2102a-113">Строковое выражение, в котором выполняется поиск.</span><span class="sxs-lookup"><span data-stu-id="2102a-113">The string expression to be searched.</span></span>  <br/> |
| <span data-ttu-id="2102a-114">*Pattern*</span><span class="sxs-lookup"><span data-stu-id="2102a-114">*Pattern*</span></span>  <br/> |<span data-ttu-id="2102a-115">Подстрока, которую необходимо найти.</span><span class="sxs-lookup"><span data-stu-id="2102a-115">The substring to be found.</span></span>  <span data-ttu-id="2102a-116">*Шаблон* не может быть пустой строкой ("").</span><span class="sxs-lookup"><span data-stu-id="2102a-116">*Pattern*  cannot be an empty string ("").</span></span>  <br/> |
| <span data-ttu-id="2102a-117">*Replacement*</span><span class="sxs-lookup"><span data-stu-id="2102a-117">*Replacement*</span></span>  <br/> |<span data-ttu-id="2102a-118">Строка замены.</span><span class="sxs-lookup"><span data-stu-id="2102a-118">The replacement string.</span></span>  <br/> |
   

