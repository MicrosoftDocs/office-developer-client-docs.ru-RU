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
description: Возвращает имя хозяина листа в качестве строки или возвращает строку "no master", если на листе нет хозяина.
ms.openlocfilehash: 7732cf9e8b23e2fd0fc2e3f2cc8d9ef4f39fd67f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414755"
---
# <a name="mastername-function"></a><span data-ttu-id="26732-103">Функция MASTERNAME</span><span class="sxs-lookup"><span data-stu-id="26732-103">MASTERNAME Function</span></span>

<span data-ttu-id="26732-104">Возвращает имя хозяина листа в качестве строки или возвращает строку "no master", если на листе нет \< \> хозяина.</span><span class="sxs-lookup"><span data-stu-id="26732-104">Returns a sheet's master name as a string, or returns the string "\<no master\>" if the sheet doesn't have a master.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="26732-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26732-105">Syntax</span></span>

<span data-ttu-id="26732-106">MASTERNAME ([ \*\* *langID_opt* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="26732-106">MASTERNAME ([ \*\* *langID_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="26732-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="26732-107">Parameters</span></span>

|<span data-ttu-id="26732-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="26732-108">**Name**</span></span>|<span data-ttu-id="26732-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="26732-109">**Required/Optional**</span></span>|<span data-ttu-id="26732-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="26732-110">**Data Type**</span></span>|<span data-ttu-id="26732-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="26732-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="26732-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="26732-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="26732-113">Необязательна</span><span class="sxs-lookup"><span data-stu-id="26732-113">Optional</span></span>  <br/> |<span data-ttu-id="26732-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="26732-114">**Number**</span></span> <br/> |<span data-ttu-id="26732-115">Используется для указания языка для строки, возвращаемой функцией.</span><span class="sxs-lookup"><span data-stu-id="26732-115">Use to specify a language for the string the function returns.</span></span> <span data-ttu-id="26732-116">Используйте 0 (значение по умолчанию) для указания локального языка.</span><span class="sxs-lookup"><span data-stu-id="26732-116">Use 0 (default value) to specify the local language.</span></span> <span data-ttu-id="26732-117">Используйте 750 для указания универсального языка.</span><span class="sxs-lookup"><span data-stu-id="26732-117">Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="26732-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="26732-118">Return value</span></span>

<span data-ttu-id="26732-119">String</span><span class="sxs-lookup"><span data-stu-id="26732-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="26732-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="26732-120">Remarks</span></span>

<span data-ttu-id="26732-121">Если вы передаете запрещенный код языка, используется локальный язык.</span><span class="sxs-lookup"><span data-stu-id="26732-121">If you pass an illegal language code, the local language is used.</span></span> 
  

