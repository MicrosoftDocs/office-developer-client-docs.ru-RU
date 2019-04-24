---
title: Функция BKGPAGENAME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253219
localization_priority: Normal
ms.assetid: f6e410ef-54d5-9c08-926b-97a2a9786622
description: Возвращает имя фоновой страницы в виде строки.
ms.openlocfilehash: 3b628315052117fe853c8f9c0fc36572de25d871
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358543"
---
# <a name="bkgpagename-function"></a><span data-ttu-id="45786-103">Функция BKGPAGENAME</span><span class="sxs-lookup"><span data-stu-id="45786-103">BKGPAGENAME Function</span></span>

<span data-ttu-id="45786-104">Возвращает имя фоновой страницы в виде строки.</span><span class="sxs-lookup"><span data-stu-id="45786-104">Returns a background page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="45786-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45786-105">Syntax</span></span>

<span data-ttu-id="45786-106">BKGPAGENAME (\* \* *лангид_опт* \* \*)</span><span class="sxs-lookup"><span data-stu-id="45786-106">BKGPAGENAME (\*\* *langID_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="45786-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="45786-107">Parameters</span></span>

|<span data-ttu-id="45786-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="45786-108">**Name**</span></span>|<span data-ttu-id="45786-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="45786-109">**Required/Optional**</span></span>|<span data-ttu-id="45786-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="45786-110">**Data Type**</span></span>|<span data-ttu-id="45786-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="45786-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="45786-112">_Лангид_опт_</span><span class="sxs-lookup"><span data-stu-id="45786-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="45786-113">Необязательный</span><span class="sxs-lookup"><span data-stu-id="45786-113">Optional</span></span>  <br/> |<span data-ttu-id="45786-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="45786-114">**Numeric**</span></span> <br/> |<span data-ttu-id="45786-115">Используется для указания языка для строки, которую возвращает функция.</span><span class="sxs-lookup"><span data-stu-id="45786-115">Use to specify a language for the string the function returns.</span></span> <span data-ttu-id="45786-116">Используйте значение 0 (значение по умолчанию), чтобы указать локальный язык.</span><span class="sxs-lookup"><span data-stu-id="45786-116">Use 0 (default value) to specify the local language.</span></span> <span data-ttu-id="45786-117">Используйте 750, чтобы указать универсальный язык.</span><span class="sxs-lookup"><span data-stu-id="45786-117">Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="45786-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45786-118">Return value</span></span>

<span data-ttu-id="45786-119">Строка</span><span class="sxs-lookup"><span data-stu-id="45786-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="45786-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="45786-120">Remarks</span></span>

<span data-ttu-id="45786-121">Если страница, для которой используется функция, не имеет фоновой страницы, возвращается строка "\<без фона\>".</span><span class="sxs-lookup"><span data-stu-id="45786-121">If the page for which you are using the function doesn't have a background page, the string "\<no background\>" is returned.</span></span> 
  
<span data-ttu-id="45786-122">Если вы передаете недопустимый код языка, используется локальный язык.</span><span class="sxs-lookup"><span data-stu-id="45786-122">If you pass an illegal language code, the local language is used.</span></span> 
  

