---
title: Функция PAGENAME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251577
localization_priority: Normal
ms.assetid: 12e45f46-e773-9445-4c7f-c726ab648671
description: Возвращает имя страницы в качестве строки.
ms.openlocfilehash: d5527bde58a68c96bd75773f3a0a8c30f64fa20d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438654"
---
# <a name="pagename-function"></a><span data-ttu-id="a062b-103">Функция PAGENAME</span><span class="sxs-lookup"><span data-stu-id="a062b-103">PAGENAME Function</span></span>

<span data-ttu-id="a062b-104">Возвращает имя страницы в качестве строки.</span><span class="sxs-lookup"><span data-stu-id="a062b-104">Returns the page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a062b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a062b-105">Syntax</span></span>

<span data-ttu-id="a062b-106">PAGENAME (\*\* *langID_opt* \*\* )</span><span class="sxs-lookup"><span data-stu-id="a062b-106">PAGENAME (\*\* *langID_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a062b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a062b-107">Parameters</span></span>

|<span data-ttu-id="a062b-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="a062b-108">**Name**</span></span>|<span data-ttu-id="a062b-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="a062b-109">**Required/Optional**</span></span>|<span data-ttu-id="a062b-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="a062b-110">**Data Type**</span></span>|<span data-ttu-id="a062b-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a062b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a062b-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="a062b-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="a062b-113">Необязательна</span><span class="sxs-lookup"><span data-stu-id="a062b-113">Optional</span></span>  <br/> |<span data-ttu-id="a062b-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="a062b-114">**Number**</span></span> <br/> |<span data-ttu-id="a062b-115">Используется для указания языка для строки, возвращаемой функцией.</span><span class="sxs-lookup"><span data-stu-id="a062b-115">Use to specify a language for the string the function returns.</span></span> <span data-ttu-id="a062b-116">Используйте 0 (значение по умолчанию) для указания локального языка.</span><span class="sxs-lookup"><span data-stu-id="a062b-116">Use 0 (default value) to specify the local language.</span></span> <span data-ttu-id="a062b-117">Используйте 750 для указания универсального языка.</span><span class="sxs-lookup"><span data-stu-id="a062b-117">Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a062b-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a062b-118">Return value</span></span>

<span data-ttu-id="a062b-119">String</span><span class="sxs-lookup"><span data-stu-id="a062b-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a062b-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="a062b-120">Remarks</span></span>

<span data-ttu-id="a062b-121">Если вы передаете запрещенный код языка, используется локальный язык.</span><span class="sxs-lookup"><span data-stu-id="a062b-121">If you pass an illegal language code, the local language is used.</span></span>
  

