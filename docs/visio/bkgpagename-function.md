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
description: Возвращает имя фоновой страницы как строку.
ms.openlocfilehash: 290fa62242298b3c513bf2870df37204fab31bf3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813282"
---
# <a name="bkgpagename-function"></a><span data-ttu-id="113c5-103">Функция BKGPAGENAME</span><span class="sxs-lookup"><span data-stu-id="113c5-103">BKGPAGENAME Function</span></span>

<span data-ttu-id="113c5-104">Возвращает имя фоновой страницы как строку.</span><span class="sxs-lookup"><span data-stu-id="113c5-104">Returns a background page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="113c5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="113c5-105">Syntax</span></span>

<span data-ttu-id="113c5-106">BKGPAGENAME (** *langID_opt* **)</span><span class="sxs-lookup"><span data-stu-id="113c5-106">BKGPAGENAME (** *langID_opt* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="113c5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="113c5-107">Parameters</span></span>

|<span data-ttu-id="113c5-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="113c5-108">**Name**</span></span>|<span data-ttu-id="113c5-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="113c5-109">**Required/Optional**</span></span>|<span data-ttu-id="113c5-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="113c5-110">**Data Type**</span></span>|<span data-ttu-id="113c5-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="113c5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="113c5-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="113c5-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="113c5-113">Optional</span><span class="sxs-lookup"><span data-stu-id="113c5-113">Optional</span></span>  <br/> |<span data-ttu-id="113c5-114">**Числовой**</span><span class="sxs-lookup"><span data-stu-id="113c5-114">**Numeric**</span></span> <br/> |<span data-ttu-id="113c5-115">Используется для указания языка, функция возвращает строки.</span><span class="sxs-lookup"><span data-stu-id="113c5-115">Use to specify a language for the string the function returns.</span></span> <span data-ttu-id="113c5-116">Используйте 0 (значение по умолчанию), чтобы указать на локальном языке.</span><span class="sxs-lookup"><span data-stu-id="113c5-116">Use 0 (default value) to specify the local language.</span></span> <span data-ttu-id="113c5-117">Используйте 750, чтобы указать универсального языка.</span><span class="sxs-lookup"><span data-stu-id="113c5-117">Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="113c5-118">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="113c5-118">Return value</span></span>

<span data-ttu-id="113c5-119">Строка</span><span class="sxs-lookup"><span data-stu-id="113c5-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="113c5-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="113c5-120">Remarks</span></span>

<span data-ttu-id="113c5-121">Если страницы, для которого выполняется с помощью функции не фоновой страницы, строки "\<не фона\>" возвращаются.</span><span class="sxs-lookup"><span data-stu-id="113c5-121">If the page for which you are using the function doesn't have a background page, the string "\<no background\>" is returned.</span></span> 
  
<span data-ttu-id="113c5-122">Если передать код незаконную языка, используется локальный язык.</span><span class="sxs-lookup"><span data-stu-id="113c5-122">If you pass an illegal language code, the local language is used.</span></span> 
  

