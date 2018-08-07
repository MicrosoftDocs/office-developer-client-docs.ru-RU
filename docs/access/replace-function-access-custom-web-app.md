---
title: Замените функцию (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 93c8fc1d-e70c-4726-af2f-c6501d82e49b
description: Заменяет все вхождения указанного строкового значения другим строковое значение.
ms.openlocfilehash: 09ba1f68973e9fb4ec8d860197509ec664e86376
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807105"
---
# <a name="replace-function-access-custom-web-app"></a><span data-ttu-id="611b9-103">Замените функцию (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="611b9-103">Replace Function (Access custom web app)</span></span>

<span data-ttu-id="611b9-104">Заменяет все вхождения указанного строкового значения другим строковое значение.</span><span class="sxs-lookup"><span data-stu-id="611b9-104">Replaces all occurrences of a specified string value with another string value.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="611b9-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="611b9-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="611b9-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="611b9-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="611b9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="611b9-107">Syntax</span></span>

 <span data-ttu-id="611b9-108">**Замена** (*TextExpression*, *шаблон* *замены*)</span><span class="sxs-lookup"><span data-stu-id="611b9-108">**Replace** (*TextExpression*, *Pattern*, *Replacement*)</span></span> 
  
<span data-ttu-id="611b9-109">Функция **Replace** содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="611b9-109">The **Replace** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="611b9-110">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="611b9-110">**Argument name**</span></span>|<span data-ttu-id="611b9-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="611b9-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="611b9-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="611b9-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="611b9-113">Строковое выражение для поиска.</span><span class="sxs-lookup"><span data-stu-id="611b9-113">The string expression to be searched.</span></span>  <br/> |
| <span data-ttu-id="611b9-114">*Шаблон*</span><span class="sxs-lookup"><span data-stu-id="611b9-114">*Pattern*</span></span>  <br/> |<span data-ttu-id="611b9-115">Подстрока для поиска.</span><span class="sxs-lookup"><span data-stu-id="611b9-115">The substring to be found.</span></span>  <span data-ttu-id="611b9-116">*Шаблон* не может быть пустой строкой (»»).</span><span class="sxs-lookup"><span data-stu-id="611b9-116">*Pattern*  cannot be an empty string ("").</span></span>  <br/> |
| <span data-ttu-id="611b9-117">*Замена*</span><span class="sxs-lookup"><span data-stu-id="611b9-117">*Replacement*</span></span>  <br/> |<span data-ttu-id="611b9-118">Строка замены.</span><span class="sxs-lookup"><span data-stu-id="611b9-118">The replacement string.</span></span>  <br/> |
   

