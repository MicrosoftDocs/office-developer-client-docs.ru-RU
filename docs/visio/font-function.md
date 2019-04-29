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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422175"
---
# <a name="font-function"></a><span data-ttu-id="750cf-103">Функция FONT</span><span class="sxs-lookup"><span data-stu-id="750cf-103">FONT Function</span></span>

<span data-ttu-id="750cf-104">Возвращает целое значение уникального идентификатора шрифта, указанного по имени.</span><span class="sxs-lookup"><span data-stu-id="750cf-104">Returns the integer value of the unique identifier for a font, specified by name.</span></span>
  
> [!NOTE]
> <span data-ttu-id="750cf-105">В большинстве случаев идентификатор шрифта относится к системе.</span><span class="sxs-lookup"><span data-stu-id="750cf-105">In most cases, the font identifier is system-specific.</span></span> <span data-ttu-id="750cf-106">Несмотря на то, что шрифт остается установленным при использовании в файле, функция **Font** обеспечивает единообразный доступ к определенному шрифту в системах и версиях Visio.</span><span class="sxs-lookup"><span data-stu-id="750cf-106">Although the font remains established once used in a file, the **FONT** function provides consistent access to a particular font across systems and versions of Visio.</span></span> <span data-ttu-id="750cf-107">Рекомендуется использовать функцию **Font** , чтобы назначать шрифты, а не ссылаться на идентификаторы шрифтов напрямую.</span><span class="sxs-lookup"><span data-stu-id="750cf-107">It is recommended that you use the **FONT** function to assign fonts instead of referring to font identifiers directly.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="750cf-108">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="750cf-108">Version Information</span></span>

<span data-ttu-id="750cf-109">Добавлена версия: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="750cf-109">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="750cf-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="750cf-110">Syntax</span></span>

 <span data-ttu-id="750cf-111">**Font (шрифт** ) ( _"фонт_наме_стринг"_)</span><span class="sxs-lookup"><span data-stu-id="750cf-111">**FONT**( _"font_name_string"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="750cf-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="750cf-112">Parameters</span></span>

|<span data-ttu-id="750cf-113">**Имя**</span><span class="sxs-lookup"><span data-stu-id="750cf-113">**Name**</span></span>|<span data-ttu-id="750cf-114">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="750cf-114">**Required/Optional**</span></span>|<span data-ttu-id="750cf-115">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="750cf-115">**Data Type**</span></span>|<span data-ttu-id="750cf-116">**Описание**</span><span class="sxs-lookup"><span data-stu-id="750cf-116">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="750cf-117">_фонт_наме_стринг_</span><span class="sxs-lookup"><span data-stu-id="750cf-117">_font_name_string_</span></span> <br/> |<span data-ttu-id="750cf-118">Обязательный</span><span class="sxs-lookup"><span data-stu-id="750cf-118">Required</span></span>  <br/> |<span data-ttu-id="750cf-119">**строка**</span><span class="sxs-lookup"><span data-stu-id="750cf-119">**string**</span></span> <br/> |<span data-ttu-id="750cf-120">Имя шрифта.</span><span class="sxs-lookup"><span data-stu-id="750cf-120">The name of the font.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="750cf-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="750cf-121">Return value</span></span>

<span data-ttu-id="750cf-122">Целое число</span><span class="sxs-lookup"><span data-stu-id="750cf-122">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="750cf-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="750cf-123">Remarks</span></span>

<span data-ttu-id="750cf-124">Если строка, указанная для *фонт_наме_стринг* , не отвечает известному шрифту, эта функция возвращает объект #VALUE!</span><span class="sxs-lookup"><span data-stu-id="750cf-124">If the string provided for  *font_name_string*  does not match a known font, this function returns a #VALUE!</span></span> <span data-ttu-id="750cf-125">ошибкой.</span><span class="sxs-lookup"><span data-stu-id="750cf-125">error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="750cf-126">Пример</span><span class="sxs-lookup"><span data-stu-id="750cf-126">Example</span></span>

 `FONT("Calibri")`
  
<span data-ttu-id="750cf-127">Возвращает целое значение (4), представляющее уникальный идентификатор шрифта "Calibri".</span><span class="sxs-lookup"><span data-stu-id="750cf-127">Returns the integer value (4) representing the unique ID for the "Calibri" font.</span></span>
  

