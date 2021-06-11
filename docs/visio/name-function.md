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
description: Возвращает имя листа в качестве строки.
ms.openlocfilehash: 7d0a4e9f3c5f70be07e9cc5691f52afcbc7bea68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416799"
---
# <a name="name-function"></a><span data-ttu-id="b6b73-103">Функция NAME</span><span class="sxs-lookup"><span data-stu-id="b6b73-103">NAME Function</span></span>

<span data-ttu-id="b6b73-104">Возвращает имя листа в качестве строки.</span><span class="sxs-lookup"><span data-stu-id="b6b73-104">Returns a sheet's name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b6b73-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6b73-105">Syntax</span></span>

<span data-ttu-id="b6b73-106">NAME (\*\* *langID_opt* \*\* )</span><span class="sxs-lookup"><span data-stu-id="b6b73-106">NAME (\*\* *langID_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b6b73-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6b73-107">Parameters</span></span>

|<span data-ttu-id="b6b73-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="b6b73-108">**Name**</span></span>|<span data-ttu-id="b6b73-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="b6b73-109">**Required/Optional**</span></span>|<span data-ttu-id="b6b73-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="b6b73-110">**Data Type**</span></span>|<span data-ttu-id="b6b73-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b6b73-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b6b73-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="b6b73-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="b6b73-113">Необязательный</span><span class="sxs-lookup"><span data-stu-id="b6b73-113">Optional</span></span>  <br/> |<span data-ttu-id="b6b73-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="b6b73-114">**Number**</span></span> <br/> |<span data-ttu-id="b6b73-115">Используйте для указания языка для строки, возвращаемой функцией.</span><span class="sxs-lookup"><span data-stu-id="b6b73-115">Use to specify a language for the string the function returns.</span></span> <span data-ttu-id="b6b73-116">Для указания локального языка используйте значение 0 (значение по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="b6b73-116">Use 0 (default value) to specify the local language.</span></span> <span data-ttu-id="b6b73-117">Используйте 750 для указания универсального языка.</span><span class="sxs-lookup"><span data-stu-id="b6b73-117">Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b6b73-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6b73-118">Return value</span></span>

<span data-ttu-id="b6b73-119">String</span><span class="sxs-lookup"><span data-stu-id="b6b73-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b6b73-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="b6b73-120">Remarks</span></span>

<span data-ttu-id="b6b73-121">Если вы передаете нелегальный языковый код, используется местный язык.</span><span class="sxs-lookup"><span data-stu-id="b6b73-121">If you pass an illegal language code, the local language is used.</span></span> 
  

