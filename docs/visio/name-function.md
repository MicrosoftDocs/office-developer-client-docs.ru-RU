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
ms.openlocfilehash: 7d0a4e9f3c5f70be07e9cc5691f52afcbc7bea68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319427"
---
# <a name="name-function"></a><span data-ttu-id="a715f-103">Функция NAME</span><span class="sxs-lookup"><span data-stu-id="a715f-103">NAME Function</span></span>

<span data-ttu-id="a715f-104">Возвращает имя листа в виде строки.</span><span class="sxs-lookup"><span data-stu-id="a715f-104">Returns a sheet's name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a715f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a715f-105">Syntax</span></span>

<span data-ttu-id="a715f-106">ИМЯ (\* \* *лангид_опт* \* \*)</span><span class="sxs-lookup"><span data-stu-id="a715f-106">NAME (\*\* *langID_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a715f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a715f-107">Parameters</span></span>

|<span data-ttu-id="a715f-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="a715f-108">**Name**</span></span>|<span data-ttu-id="a715f-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="a715f-109">**Required/Optional**</span></span>|<span data-ttu-id="a715f-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="a715f-110">**Data Type**</span></span>|<span data-ttu-id="a715f-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a715f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a715f-112">_Лангид_опт_</span><span class="sxs-lookup"><span data-stu-id="a715f-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="a715f-113">Необязательный</span><span class="sxs-lookup"><span data-stu-id="a715f-113">Optional</span></span>  <br/> |<span data-ttu-id="a715f-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="a715f-114">**Number**</span></span> <br/> |<span data-ttu-id="a715f-115">Используется для указания языка для строки, которую возвращает функция.</span><span class="sxs-lookup"><span data-stu-id="a715f-115">Use to specify a language for the string the function returns.</span></span> <span data-ttu-id="a715f-116">Используйте значение 0 (значение по умолчанию), чтобы указать локальный язык.</span><span class="sxs-lookup"><span data-stu-id="a715f-116">Use 0 (default value) to specify the local language.</span></span> <span data-ttu-id="a715f-117">Используйте 750, чтобы указать универсальный язык.</span><span class="sxs-lookup"><span data-stu-id="a715f-117">Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a715f-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a715f-118">Return value</span></span>

<span data-ttu-id="a715f-119">Строка</span><span class="sxs-lookup"><span data-stu-id="a715f-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a715f-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="a715f-120">Remarks</span></span>

<span data-ttu-id="a715f-121">Если вы передаете недопустимый код языка, используется локальный язык.</span><span class="sxs-lookup"><span data-stu-id="a715f-121">If you pass an illegal language code, the local language is used.</span></span> 
  

