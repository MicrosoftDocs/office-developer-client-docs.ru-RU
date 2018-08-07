---
title: Функция NAME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251580
localization_priority: Normal
ms.assetid: 1ca67a09-9df2-37f5-b269-e761d76bb011
description: Возвращает имя листа в виде строки.
ms.openlocfilehash: 0d3a70573177d8e16a16972d0a08245381b209dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814291"
---
# <a name="name-function"></a><span data-ttu-id="6f36b-103">Функция NAME</span><span class="sxs-lookup"><span data-stu-id="6f36b-103">NAME Function</span></span>

<span data-ttu-id="6f36b-104">Возвращает имя листа в виде строки.</span><span class="sxs-lookup"><span data-stu-id="6f36b-104">Returns a sheet's name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6f36b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f36b-105">Syntax</span></span>

<span data-ttu-id="6f36b-106">Имя (** *langID_opt* **)</span><span class="sxs-lookup"><span data-stu-id="6f36b-106">NAME (** *langID_opt* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6f36b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f36b-107">Parameters</span></span>

|<span data-ttu-id="6f36b-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="6f36b-108">**Name**</span></span>|<span data-ttu-id="6f36b-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="6f36b-109">**Required/Optional**</span></span>|<span data-ttu-id="6f36b-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="6f36b-110">**Data Type**</span></span>|<span data-ttu-id="6f36b-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6f36b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6f36b-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="6f36b-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="6f36b-113">Optional</span><span class="sxs-lookup"><span data-stu-id="6f36b-113">Optional</span></span>  <br/> |<span data-ttu-id="6f36b-114">**Число**</span><span class="sxs-lookup"><span data-stu-id="6f36b-114">**Number**</span></span> <br/> |<span data-ttu-id="6f36b-115">Используется для указания языка, функция возвращает строки.</span><span class="sxs-lookup"><span data-stu-id="6f36b-115">Use to specify a language for the string the function returns.</span></span> <span data-ttu-id="6f36b-116">Используйте 0 (значение по умолчанию), чтобы указать на локальном языке.</span><span class="sxs-lookup"><span data-stu-id="6f36b-116">Use 0 (default value) to specify the local language.</span></span> <span data-ttu-id="6f36b-117">Используйте 750, чтобы указать универсального языка.</span><span class="sxs-lookup"><span data-stu-id="6f36b-117">Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6f36b-118">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="6f36b-118">Return value</span></span>

<span data-ttu-id="6f36b-119">Строка</span><span class="sxs-lookup"><span data-stu-id="6f36b-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6f36b-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="6f36b-120">Remarks</span></span>

<span data-ttu-id="6f36b-121">Если передать код незаконную языка, используется локальный язык.</span><span class="sxs-lookup"><span data-stu-id="6f36b-121">If you pass an illegal language code, the local language is used.</span></span> 
  

