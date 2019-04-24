---
title: Функция REWIDEN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033808
localization_priority: Normal
ms.assetid: c20842cd-86b1-83fa-49ba-118936013b6f
description: Преобразует формулу, которая создает 16 – битовые коды символов, которые являются расширенными кодами символов с одним или более многобайтовым кодом, в строку 16 – разрядных символов Юникода с использованием указанных наборов символов.
ms.openlocfilehash: c885487f91e541027b7ba09812e7321a9deb00ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326770"
---
# <a name="rewiden-function"></a><span data-ttu-id="7bebd-103">Функция REWIDEN</span><span class="sxs-lookup"><span data-stu-id="7bebd-103">REWIDEN Function</span></span>

<span data-ttu-id="7bebd-104">Преобразует формулу, которая создает 16 – битовые коды символов, которые являются расширенными кодами символов с одним или более многобайтовым кодом, в строку 16 – разрядных символов Юникода с использованием указанных наборов символов.</span><span class="sxs-lookup"><span data-stu-id="7bebd-104">Converts a formula that produces 16-bit character codes that are widened single-byte or multibyte character-set codes into a string of 16-bit Unicode character codes, using the specified character sets.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7bebd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7bebd-105">Syntax</span></span>

<span data-ttu-id="7bebd-106">ReWIDEN (\* \* *сркчарсет* \* \*, \* \* *дстчарсет* \* \*, \* \* *Text* \* \*)</span><span class="sxs-lookup"><span data-stu-id="7bebd-106">REWIDEN(\*\* *srcCharSet* \*\*, \*\* *dstCharSet* \*\*, \*\* *text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7bebd-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7bebd-107">Parameters</span></span>

|<span data-ttu-id="7bebd-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="7bebd-108">**Name**</span></span>|<span data-ttu-id="7bebd-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="7bebd-109">**Required/Optional**</span></span>|<span data-ttu-id="7bebd-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="7bebd-110">**Data Type**</span></span>|<span data-ttu-id="7bebd-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7bebd-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7bebd-112">_Сркчарсет_</span><span class="sxs-lookup"><span data-stu-id="7bebd-112">_srcCharSet_</span></span> <br/> |<span data-ttu-id="7bebd-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7bebd-113">Required</span></span>  <br/> |<span data-ttu-id="7bebd-114">**String**</span><span class="sxs-lookup"><span data-stu-id="7bebd-114">**String**</span></span> <br/> |<span data-ttu-id="7bebd-115">Набор символов в исходном документе.</span><span class="sxs-lookup"><span data-stu-id="7bebd-115">The character set in the source document.</span></span>  <br/> |
| <span data-ttu-id="7bebd-116">_Дстчарсет_</span><span class="sxs-lookup"><span data-stu-id="7bebd-116">_dstCharSet_</span></span> <br/> |<span data-ttu-id="7bebd-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7bebd-117">Required</span></span>  <br/> |<span data-ttu-id="7bebd-118">**String**</span><span class="sxs-lookup"><span data-stu-id="7bebd-118">**String**</span></span> <br/> | <span data-ttu-id="7bebd-119">Набор символов в целевом документе.</span><span class="sxs-lookup"><span data-stu-id="7bebd-119">The character set in the destination document.</span></span>  <br/> |
| <span data-ttu-id="7bebd-120">_text_</span><span class="sxs-lookup"><span data-stu-id="7bebd-120">_text_</span></span> <br/> |<span data-ttu-id="7bebd-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7bebd-121">Required</span></span>  <br/> |<span data-ttu-id="7bebd-122">**String**</span><span class="sxs-lookup"><span data-stu-id="7bebd-122">**String**</span></span> <br/> |<span data-ttu-id="7bebd-123">Преобразуемый текст.</span><span class="sxs-lookup"><span data-stu-id="7bebd-123">The text to convert.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7bebd-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="7bebd-124">Remarks</span></span>

<span data-ttu-id="7bebd-125">Функция reWIDEN используется для автоматического преобразования документов Visio 2002 в документы Visio 2003.</span><span class="sxs-lookup"><span data-stu-id="7bebd-125">The REWIDEN function is used in automatic conversion of Visio 2002 documents to Visio 2003 documents.</span></span> <span data-ttu-id="7bebd-126">Использовать другие рекомендации не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="7bebd-126">Other use is not recommended.</span></span>
  

