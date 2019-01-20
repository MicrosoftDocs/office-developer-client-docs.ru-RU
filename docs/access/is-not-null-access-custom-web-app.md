---
title: IS [NOT] NULL (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: Определяет, имеет ли указанное выражение значение NULL.
localization_priority: Priority
ms.openlocfilehash: fe6a0fe4f182a1385304b783e7cfaaf515f732d4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699319"
---
# <a name="is-not-null-access-custom-web-app"></a><span data-ttu-id="a6448-103">IS [NOT] NULL (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="a6448-103">IS [NOT] NULL (Access 2013 custom web app)</span></span>

<span data-ttu-id="a6448-104">Определяет, имеет ли указанное выражение значение NULL.</span><span class="sxs-lookup"><span data-stu-id="a6448-104">Determines whether a specified expression is NULL.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a6448-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a6448-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="a6448-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/ru-RU/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="a6448-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ru-RU/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a6448-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6448-107">Syntax</span></span>

 <span data-ttu-id="a6448-108">*выражение* **IS** [  *NOT*  ] **NULL**</span><span class="sxs-lookup"><span data-stu-id="a6448-108">*expression* **IS** [  *NOT*  ] **NULL**</span></span>
  
<span data-ttu-id="a6448-109">Предикат **IS [NOT] NULL** содержит указанные ниже аргументы.</span><span class="sxs-lookup"><span data-stu-id="a6448-109">The **IS [NOT] NULL** predicate contains the following arguments.</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a6448-110">*выражение*</span><span class="sxs-lookup"><span data-stu-id="a6448-110">*expression*</span></span>  <br/> |<span data-ttu-id="a6448-111">Любое допустимое выражение.</span><span class="sxs-lookup"><span data-stu-id="a6448-111">Any valid expression.</span></span>  <br/> |
| <span data-ttu-id="a6448-112">*NOT*</span><span class="sxs-lookup"><span data-stu-id="a6448-112">*NOT*</span></span>  <br/> |<span data-ttu-id="a6448-113">Указывает, что логический результат отвергается.</span><span class="sxs-lookup"><span data-stu-id="a6448-113">Specifies that the Boolean result be negated.</span></span> <span data-ttu-id="a6448-114">Предикат меняет возвращенные значения на противоположные, возвращая TRUE, если значение отлично от NULL, и FALSE, если значением является NULL.</span><span class="sxs-lookup"><span data-stu-id="a6448-114">The predicate reverses its return values, returning TRUE if the value is not NULL, and FALSE if the value is NULL.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6448-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="a6448-115">Remarks</span></span>

<span data-ttu-id="a6448-116">Если *выражение* имеет значение NULL, предикат IS NULL возвращает значение TRUE; в ином случае возвращается значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="a6448-116">If the value of  *expression*  is NULL, IS NULL returns TRUE; otherwise, it returns FALSE.</span></span> 
  
<span data-ttu-id="a6448-117">Если выражение имеет значение NULL, предикат IS NOT NULL возвращает значение FALSE; в ином случае возвращается значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="a6448-117">If the value of expression is NULL, IS NOT NULL returns FALSE; otherwise, it returns TRUE.</span></span>
  

