---
title: Функция FONT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Возвращает целое значение уникального идентификатора шрифта, указанного по имени.
ms.openlocfilehash: 7ae6fe6dc8bb9c718a358d11d4a6a0227eaf18df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346139"
---
# <a name="font-function"></a><span data-ttu-id="d99e9-103">Функция FONT</span><span class="sxs-lookup"><span data-stu-id="d99e9-103">FONT Function</span></span>

<span data-ttu-id="d99e9-104">Возвращает целое значение уникального идентификатора шрифта, указанного по имени.</span><span class="sxs-lookup"><span data-stu-id="d99e9-104">Returns the integer value of the unique identifier for a font, specified by name.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d99e9-105">В большинстве случаев идентификатор шрифта относится к системе.</span><span class="sxs-lookup"><span data-stu-id="d99e9-105">In most cases, the font identifier is system-specific.</span></span> <span data-ttu-id="d99e9-106">Несмотря на то, что шрифт остается установленным при использовании в файле, функция **Font** обеспечивает единообразный доступ к определенному шрифту в системах и версиях Visio.</span><span class="sxs-lookup"><span data-stu-id="d99e9-106">Although the font remains established once used in a file, the **FONT** function provides consistent access to a particular font across systems and versions of Visio.</span></span> <span data-ttu-id="d99e9-107">Рекомендуется использовать функцию **Font** , чтобы назначать шрифты, а не ссылаться на идентификаторы шрифтов напрямую.</span><span class="sxs-lookup"><span data-stu-id="d99e9-107">It is recommended that you use the **FONT** function to assign fonts instead of referring to font identifiers directly.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="d99e9-108">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="d99e9-108">Version Information</span></span>

<span data-ttu-id="d99e9-109">Добавлена версия: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="d99e9-109">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d99e9-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d99e9-110">Syntax</span></span>

 <span data-ttu-id="d99e9-111">**Font (шрифт** ) ( _"фонт_наме_стринг"_)</span><span class="sxs-lookup"><span data-stu-id="d99e9-111">**FONT**( _"font_name_string"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="d99e9-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="d99e9-112">Parameters</span></span>

|<span data-ttu-id="d99e9-113">**Имя**</span><span class="sxs-lookup"><span data-stu-id="d99e9-113">**Name**</span></span>|<span data-ttu-id="d99e9-114">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="d99e9-114">**Required/Optional**</span></span>|<span data-ttu-id="d99e9-115">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="d99e9-115">**Data Type**</span></span>|<span data-ttu-id="d99e9-116">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d99e9-116">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d99e9-117">_фонт_наме_стринг_</span><span class="sxs-lookup"><span data-stu-id="d99e9-117">_font_name_string_</span></span> <br/> |<span data-ttu-id="d99e9-118">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d99e9-118">Required</span></span>  <br/> |<span data-ttu-id="d99e9-119">**строка**</span><span class="sxs-lookup"><span data-stu-id="d99e9-119">**string**</span></span> <br/> |<span data-ttu-id="d99e9-120">Имя шрифта.</span><span class="sxs-lookup"><span data-stu-id="d99e9-120">The name of the font.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="d99e9-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d99e9-121">Return value</span></span>

<span data-ttu-id="d99e9-122">Целое число</span><span class="sxs-lookup"><span data-stu-id="d99e9-122">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d99e9-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="d99e9-123">Remarks</span></span>

<span data-ttu-id="d99e9-124">Если строка, указанная для *фонт_наме_стринг* , не отвечает известному шрифту, эта функция возвращает объект #VALUE!</span><span class="sxs-lookup"><span data-stu-id="d99e9-124">If the string provided for  *font_name_string*  does not match a known font, this function returns a #VALUE!</span></span> <span data-ttu-id="d99e9-125">ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d99e9-125">error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d99e9-126">Пример</span><span class="sxs-lookup"><span data-stu-id="d99e9-126">Example</span></span>

 `FONT("Calibri")`
  
<span data-ttu-id="d99e9-127">Возвращает целое значение (4), представляющее уникальный идентификатор шрифта "Calibri".</span><span class="sxs-lookup"><span data-stu-id="d99e9-127">Returns the integer value (4) representing the unique ID for the "Calibri" font.</span></span>
  

