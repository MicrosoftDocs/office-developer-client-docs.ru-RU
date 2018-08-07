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
description: Преобразует формулу, которая создала коды 16-разрядный символов, которые являются расширенными однобайтовые или многобайтовые кодов набор символов в строку коды знаков Юникод 16-разрядный, с помощью указанных наборов символов.
ms.openlocfilehash: 66dc3e801585077a9521cd93f8ae78c47f8a746b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814616"
---
# <a name="rewiden-function"></a><span data-ttu-id="853d6-103">Функция REWIDEN</span><span class="sxs-lookup"><span data-stu-id="853d6-103">REWIDEN Function</span></span>

<span data-ttu-id="853d6-104">Преобразует формулу, которая создала коды 16-разрядный символов, которые являются расширенными однобайтовые или многобайтовые кодов набор символов в строку коды знаков Юникод 16-разрядный, с помощью указанных наборов символов.</span><span class="sxs-lookup"><span data-stu-id="853d6-104">Converts a formula that produces 16-bit character codes that are widened single-byte or multibyte character-set codes into a string of 16-bit Unicode character codes, using the specified character sets.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="853d6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="853d6-105">Syntax</span></span>

<span data-ttu-id="853d6-106">REWIDEN (** *srcCharSet* **, ** *dstCharSet* **, ** *текст* **)</span><span class="sxs-lookup"><span data-stu-id="853d6-106">REWIDEN(** *srcCharSet* **, ** *dstCharSet* **, ** *text* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="853d6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="853d6-107">Parameters</span></span>

|<span data-ttu-id="853d6-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="853d6-108">**Name**</span></span>|<span data-ttu-id="853d6-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="853d6-109">**Required/Optional**</span></span>|<span data-ttu-id="853d6-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="853d6-110">**Data Type**</span></span>|<span data-ttu-id="853d6-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="853d6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="853d6-112">_srcCharSet_</span><span class="sxs-lookup"><span data-stu-id="853d6-112">_srcCharSet_</span></span> <br/> |<span data-ttu-id="853d6-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="853d6-113">Required</span></span>  <br/> |<span data-ttu-id="853d6-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="853d6-114">**String**</span></span> <br/> |<span data-ttu-id="853d6-115">Набор символов в исходном документе.</span><span class="sxs-lookup"><span data-stu-id="853d6-115">The character set in the source document.</span></span>  <br/> |
| <span data-ttu-id="853d6-116">_dstCharSet_</span><span class="sxs-lookup"><span data-stu-id="853d6-116">_dstCharSet_</span></span> <br/> |<span data-ttu-id="853d6-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="853d6-117">Required</span></span>  <br/> |<span data-ttu-id="853d6-118">**Строка**</span><span class="sxs-lookup"><span data-stu-id="853d6-118">**String**</span></span> <br/> | <span data-ttu-id="853d6-119">Набор символов в целевой документ.</span><span class="sxs-lookup"><span data-stu-id="853d6-119">The character set in the destination document.</span></span>  <br/> |
| <span data-ttu-id="853d6-120">_text_</span><span class="sxs-lookup"><span data-stu-id="853d6-120">_text_</span></span> <br/> |<span data-ttu-id="853d6-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="853d6-121">Required</span></span>  <br/> |<span data-ttu-id="853d6-122">**Строка**</span><span class="sxs-lookup"><span data-stu-id="853d6-122">**String**</span></span> <br/> |<span data-ttu-id="853d6-123">Текст для преобразования.</span><span class="sxs-lookup"><span data-stu-id="853d6-123">The text to convert.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="853d6-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="853d6-124">Remarks</span></span>

<span data-ttu-id="853d6-125">Функция REWIDEN используется в автоматическое преобразование документов Visio 2002 в документы Visio 2003.</span><span class="sxs-lookup"><span data-stu-id="853d6-125">The REWIDEN function is used in automatic conversion of Visio 2002 documents to Visio 2003 documents.</span></span> <span data-ttu-id="853d6-126">Не рекомендуется использовать другие.</span><span class="sxs-lookup"><span data-stu-id="853d6-126">Other use is not recommended.</span></span>
  

