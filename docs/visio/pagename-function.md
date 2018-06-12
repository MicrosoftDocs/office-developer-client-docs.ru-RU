---
title: Функция ИМЯ_СТРАНИЦЫ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251577
localization_priority: Normal
ms.assetid: 12e45f46-e773-9445-4c7f-c726ab648671
description: Возвращает имя страницы в виде строки.
ms.openlocfilehash: 530707530d60955f460d6a747024b98ebdd5ab62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814344"
---
# <a name="pagename-function"></a><span data-ttu-id="f49b2-103">Функция ИМЯ_СТРАНИЦЫ</span><span class="sxs-lookup"><span data-stu-id="f49b2-103">PAGENAME Function</span></span>

<span data-ttu-id="f49b2-104">Возвращает имя страницы в виде строки.</span><span class="sxs-lookup"><span data-stu-id="f49b2-104">Returns the page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f49b2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f49b2-105">Syntax</span></span>

<span data-ttu-id="f49b2-106">ИМЯ_СТРАНИЦЫ (** *langID_opt* **)</span><span class="sxs-lookup"><span data-stu-id="f49b2-106">PAGENAME (** *langID_opt* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f49b2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f49b2-107">Parameters</span></span>

|<span data-ttu-id="f49b2-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="f49b2-108">**Name**</span></span>|<span data-ttu-id="f49b2-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="f49b2-109">**Required/Optional**</span></span>|<span data-ttu-id="f49b2-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="f49b2-110">**Data Type**</span></span>|<span data-ttu-id="f49b2-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f49b2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f49b2-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="f49b2-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="f49b2-113">Optional</span><span class="sxs-lookup"><span data-stu-id="f49b2-113">Optional</span></span>  <br/> |<span data-ttu-id="f49b2-114">**Число**</span><span class="sxs-lookup"><span data-stu-id="f49b2-114">**Number**</span></span> <br/> |<span data-ttu-id="f49b2-115">Используется для указания языка, функция возвращает строки.</span><span class="sxs-lookup"><span data-stu-id="f49b2-115">Use to specify a language for the string the function returns.</span></span> <span data-ttu-id="f49b2-116">Используйте 0 (значение по умолчанию), чтобы указать на локальном языке.</span><span class="sxs-lookup"><span data-stu-id="f49b2-116">Use 0 (default value) to specify the local language.</span></span> <span data-ttu-id="f49b2-117">Используйте 750, чтобы указать универсального языка.</span><span class="sxs-lookup"><span data-stu-id="f49b2-117">Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f49b2-118">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="f49b2-118">Return value</span></span>

<span data-ttu-id="f49b2-119">Строка</span><span class="sxs-lookup"><span data-stu-id="f49b2-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f49b2-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="f49b2-120">Remarks</span></span>

<span data-ttu-id="f49b2-121">Если передать код незаконную языка, используется локальный язык.</span><span class="sxs-lookup"><span data-stu-id="f49b2-121">If you pass an illegal language code, the local language is used.</span></span>
  

