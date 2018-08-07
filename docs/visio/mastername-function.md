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
description: Возвращает имя образца листа в виде строки или строка «не образец» Если листа отсутствует главный.
ms.openlocfilehash: c1d5891fba0f967cde4a4e9ca58d07f87239f0b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814210"
---
# <a name="mastername-function"></a><span data-ttu-id="dc7a5-103">Функция MASTERNAME</span><span class="sxs-lookup"><span data-stu-id="dc7a5-103">MASTERNAME Function</span></span>

<span data-ttu-id="dc7a5-104">Возвращает имя образца листа в виде строки или строка "\<не образец\>" Если листа отсутствует главный.</span><span class="sxs-lookup"><span data-stu-id="dc7a5-104">Returns a sheet's master name as a string, or returns the string "\<no master\>" if the sheet doesn't have a master.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="dc7a5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc7a5-105">Syntax</span></span>

<span data-ttu-id="dc7a5-106">ИМЯОБРАЗЦА ([** *langID_opt* **])</span><span class="sxs-lookup"><span data-stu-id="dc7a5-106">MASTERNAME ([ ** *langID_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dc7a5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc7a5-107">Parameters</span></span>

|<span data-ttu-id="dc7a5-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="dc7a5-108">**Name**</span></span>|<span data-ttu-id="dc7a5-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="dc7a5-109">**Required/Optional**</span></span>|<span data-ttu-id="dc7a5-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="dc7a5-110">**Data Type**</span></span>|<span data-ttu-id="dc7a5-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dc7a5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dc7a5-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="dc7a5-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="dc7a5-113">Optional</span><span class="sxs-lookup"><span data-stu-id="dc7a5-113">Optional</span></span>  <br/> |<span data-ttu-id="dc7a5-114">**Число**</span><span class="sxs-lookup"><span data-stu-id="dc7a5-114">**Number**</span></span> <br/> |<span data-ttu-id="dc7a5-115">Используется для указания языка, функция возвращает строки.</span><span class="sxs-lookup"><span data-stu-id="dc7a5-115">Use to specify a language for the string the function returns.</span></span> <span data-ttu-id="dc7a5-116">Используйте 0 (значение по умолчанию), чтобы указать на локальном языке.</span><span class="sxs-lookup"><span data-stu-id="dc7a5-116">Use 0 (default value) to specify the local language.</span></span> <span data-ttu-id="dc7a5-117">Используйте 750, чтобы указать универсального языка.</span><span class="sxs-lookup"><span data-stu-id="dc7a5-117">Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="dc7a5-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8">Return value</span></span>

<span data-ttu-id="dc7a5-119">Строка</span><span class="sxs-lookup"><span data-stu-id="dc7a5-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dc7a5-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="dc7a5-120">Remarks</span></span>

<span data-ttu-id="dc7a5-121">Если передать код незаконную языка, используется локальный язык.</span><span class="sxs-lookup"><span data-stu-id="dc7a5-121">If you pass an illegal language code, the local language is used.</span></span> 
  

