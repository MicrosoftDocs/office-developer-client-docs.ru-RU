---
title: НЕ [] значение NULL (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: Определяет, является ли указанный элемент expression равен NULL.
ms.openlocfilehash: fcbceb1e8edac65fe232ba9c2b12195b99db9545
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806960"
---
# <a name="is-not-null-access-custom-web-app"></a><span data-ttu-id="ae425-103">НЕ [] значение NULL (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="ae425-103">IS [NOT] NULL (Access custom web app)</span></span>

<span data-ttu-id="ae425-104">Определяет, является ли указанный элемент expression равен NULL.</span><span class="sxs-lookup"><span data-stu-id="ae425-104">Determines whether a specified expression is NULL.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ae425-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ae425-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="ae425-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="ae425-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ae425-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae425-107">Syntax</span></span>

 <span data-ttu-id="ae425-108">*выражение* **IS** [ *Не* ] **Значение NULL**</span><span class="sxs-lookup"><span data-stu-id="ae425-108">*expression* **IS** [  *NOT*  ] **NULL**</span></span>
  
<span data-ttu-id="ae425-109">**IS [NOT] NULL** предикат содержит следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="ae425-109">The **IS [NOT] NULL** predicate contains the following arguments.</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ae425-110">*expression*</span><span class="sxs-lookup"><span data-stu-id="ae425-110">*expression*</span></span>  <br/> |<span data-ttu-id="ae425-111">Любое допустимое выражение.</span><span class="sxs-lookup"><span data-stu-id="ae425-111">Any valid expression.</span></span>  <br/> |
| <span data-ttu-id="ae425-112">*NOT*</span><span class="sxs-lookup"><span data-stu-id="ae425-112">*NOT*</span></span>  <br/> |<span data-ttu-id="ae425-113">Указывает, должен быть инвертирован логическое значение.</span><span class="sxs-lookup"><span data-stu-id="ae425-113">Specifies that the Boolean result be negated.</span></span> <span data-ttu-id="ae425-114">Предикат отменяет его возвращаемых значений, возвращает значение TRUE, если значение не NULL и FALSE, если значение равно NULL.</span><span class="sxs-lookup"><span data-stu-id="ae425-114">The predicate reverses its return values, returning TRUE if the value is not NULL, and FALSE if the value is NULL.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae425-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="ae425-115">Remarks</span></span>

<span data-ttu-id="ae425-116">Если значение *выражения* имеет значение NULL, ИМЕЕТ значение NULL возвращает значение TRUE; в противном случае возвращает значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="ae425-116">If the value of  *expression*  is NULL, IS NULL returns TRUE; otherwise, it returns FALSE.</span></span> 
  
<span data-ttu-id="ae425-117">Если значение выражения имеет значение NULL, IS NOT NULL возвращает FALSE. в противном случае возвращается значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="ae425-117">If the value of expression is NULL, IS NOT NULL returns FALSE; otherwise, it returns TRUE.</span></span>
  

