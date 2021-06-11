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
description: Преобразует формулу, которая создает 16-разрядные коды символов, которые расширяются однобайтными или многобайтными кодами символов, в строку из 16-разрядных кодов символов Юникод, используя указанные наборы символов.
ms.openlocfilehash: c885487f91e541027b7ba09812e7321a9deb00ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405214"
---
# <a name="rewiden-function"></a><span data-ttu-id="e9995-103">Функция REWIDEN</span><span class="sxs-lookup"><span data-stu-id="e9995-103">REWIDEN Function</span></span>

<span data-ttu-id="e9995-104">Преобразует формулу, которая создает 16-разрядные коды символов, которые расширяются однобайтными или многобайтными кодами символов, в строку из 16-разрядных кодов символов Юникод, используя указанные наборы символов.</span><span class="sxs-lookup"><span data-stu-id="e9995-104">Converts a formula that produces 16-bit character codes that are widened single-byte or multibyte character-set codes into a string of 16-bit Unicode character codes, using the specified character sets.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e9995-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9995-105">Syntax</span></span>

<span data-ttu-id="e9995-106">REWIDEN(\*\* *srcCharSet* \*\*, \*\* *dstCharSet* \*\*, \*\* *text* \*\* )</span><span class="sxs-lookup"><span data-stu-id="e9995-106">REWIDEN(\*\* *srcCharSet* \*\*, \*\* *dstCharSet* \*\*, \*\* *text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e9995-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9995-107">Parameters</span></span>

|<span data-ttu-id="e9995-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="e9995-108">**Name**</span></span>|<span data-ttu-id="e9995-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="e9995-109">**Required/Optional**</span></span>|<span data-ttu-id="e9995-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="e9995-110">**Data Type**</span></span>|<span data-ttu-id="e9995-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e9995-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e9995-112">_srcCharSet_</span><span class="sxs-lookup"><span data-stu-id="e9995-112">_srcCharSet_</span></span> <br/> |<span data-ttu-id="e9995-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e9995-113">Required</span></span>  <br/> |<span data-ttu-id="e9995-114">**String**</span><span class="sxs-lookup"><span data-stu-id="e9995-114">**String**</span></span> <br/> |<span data-ttu-id="e9995-115">Набор символов в исходных документах.</span><span class="sxs-lookup"><span data-stu-id="e9995-115">The character set in the source document.</span></span>  <br/> |
| <span data-ttu-id="e9995-116">_dstCharSet_</span><span class="sxs-lookup"><span data-stu-id="e9995-116">_dstCharSet_</span></span> <br/> |<span data-ttu-id="e9995-117">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e9995-117">Required</span></span>  <br/> |<span data-ttu-id="e9995-118">**String**</span><span class="sxs-lookup"><span data-stu-id="e9995-118">**String**</span></span> <br/> | <span data-ttu-id="e9995-119">Набор символов в документе назначения.</span><span class="sxs-lookup"><span data-stu-id="e9995-119">The character set in the destination document.</span></span>  <br/> |
| <span data-ttu-id="e9995-120">_text_</span><span class="sxs-lookup"><span data-stu-id="e9995-120">_text_</span></span> <br/> |<span data-ttu-id="e9995-121">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e9995-121">Required</span></span>  <br/> |<span data-ttu-id="e9995-122">**String**</span><span class="sxs-lookup"><span data-stu-id="e9995-122">**String**</span></span> <br/> |<span data-ttu-id="e9995-123">Текст преобразования.</span><span class="sxs-lookup"><span data-stu-id="e9995-123">The text to convert.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9995-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="e9995-124">Remarks</span></span>

<span data-ttu-id="e9995-125">Функция REWIDEN используется в автоматическом преобразовании документов 2002 Visio 2002 Visio документов 2003 года.</span><span class="sxs-lookup"><span data-stu-id="e9995-125">The REWIDEN function is used in automatic conversion of Visio 2002 documents to Visio 2003 documents.</span></span> <span data-ttu-id="e9995-126">Другое использование не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="e9995-126">Other use is not recommended.</span></span>
  

