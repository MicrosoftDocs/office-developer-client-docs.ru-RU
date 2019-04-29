---
title: Функция MASTERNAME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251581
localization_priority: Normal
ms.assetid: 519d79d4-9178-2231-c26d-aa7f31a43412
description: Возвращает имя образца листа в виде строки или возвращает строку "No Master", если у листа нет образца.
ms.openlocfilehash: 7732cf9e8b23e2fd0fc2e3f2cc8d9ef4f39fd67f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414755"
---
# <a name="mastername-function"></a><span data-ttu-id="8f78d-103">Функция MASTERNAME</span><span class="sxs-lookup"><span data-stu-id="8f78d-103">MASTERNAME Function</span></span>

<span data-ttu-id="8f78d-104">Возвращает имя образца листа в виде строки или возвращает строку "\<без образца\>", если у листа нет образца.</span><span class="sxs-lookup"><span data-stu-id="8f78d-104">Returns a sheet's master name as a string, or returns the string "\<no master\>" if the sheet doesn't have a master.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8f78d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f78d-105">Syntax</span></span>

<span data-ttu-id="8f78d-106">MASTERNAME ([\* \* *лангид_опт* \* \*])</span><span class="sxs-lookup"><span data-stu-id="8f78d-106">MASTERNAME ([ \*\* *langID_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8f78d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f78d-107">Parameters</span></span>

|<span data-ttu-id="8f78d-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="8f78d-108">**Name**</span></span>|<span data-ttu-id="8f78d-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="8f78d-109">**Required/Optional**</span></span>|<span data-ttu-id="8f78d-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="8f78d-110">**Data Type**</span></span>|<span data-ttu-id="8f78d-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8f78d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8f78d-112">_Лангид_опт_</span><span class="sxs-lookup"><span data-stu-id="8f78d-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="8f78d-113">Необязательный</span><span class="sxs-lookup"><span data-stu-id="8f78d-113">Optional</span></span>  <br/> |<span data-ttu-id="8f78d-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="8f78d-114">**Number**</span></span> <br/> |<span data-ttu-id="8f78d-115">Используется для указания языка для строки, которую возвращает функция.</span><span class="sxs-lookup"><span data-stu-id="8f78d-115">Use to specify a language for the string the function returns.</span></span> <span data-ttu-id="8f78d-116">Используйте значение 0 (значение по умолчанию), чтобы указать локальный язык.</span><span class="sxs-lookup"><span data-stu-id="8f78d-116">Use 0 (default value) to specify the local language.</span></span> <span data-ttu-id="8f78d-117">Используйте 750, чтобы указать универсальный язык.</span><span class="sxs-lookup"><span data-stu-id="8f78d-117">Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8f78d-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8f78d-118">Return value</span></span>

<span data-ttu-id="8f78d-119">String</span><span class="sxs-lookup"><span data-stu-id="8f78d-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8f78d-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="8f78d-120">Remarks</span></span>

<span data-ttu-id="8f78d-121">Если вы передаете недопустимый код языка, используется локальный язык.</span><span class="sxs-lookup"><span data-stu-id="8f78d-121">If you pass an illegal language code, the local language is used.</span></span> 
  

