---
title: Функция FONT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Возвращает значение integer уникального идентификатора для шрифта, указанного по имени.
ms.openlocfilehash: 7ae6fe6dc8bb9c718a358d11d4a6a0227eaf18df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422175"
---
# <a name="font-function"></a><span data-ttu-id="979e3-103">Функция FONT</span><span class="sxs-lookup"><span data-stu-id="979e3-103">FONT Function</span></span>

<span data-ttu-id="979e3-104">Возвращает значение integer уникального идентификатора для шрифта, указанного по имени.</span><span class="sxs-lookup"><span data-stu-id="979e3-104">Returns the integer value of the unique identifier for a font, specified by name.</span></span>
  
> [!NOTE]
> <span data-ttu-id="979e3-105">В большинстве случаев идентификатор шрифта является системным.</span><span class="sxs-lookup"><span data-stu-id="979e3-105">In most cases, the font identifier is system-specific.</span></span> <span data-ttu-id="979e3-106">Хотя шрифт остается установленным после использования в файле, функция **FONT** обеспечивает последовательный доступ к определенному шрифту в системах и версиях Visio.</span><span class="sxs-lookup"><span data-stu-id="979e3-106">Although the font remains established once used in a file, the **FONT** function provides consistent access to a particular font across systems and versions of Visio.</span></span> <span data-ttu-id="979e3-107">Рекомендуется использовать функцию **FONT** для назначения шрифтов, а не ссылаясь непосредственно на идентификаторы шрифтов.</span><span class="sxs-lookup"><span data-stu-id="979e3-107">It is recommended that you use the **FONT** function to assign fonts instead of referring to font identifiers directly.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="979e3-108">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="979e3-108">Version Information</span></span>

<span data-ttu-id="979e3-109">Добавлена версия: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="979e3-109">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="979e3-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="979e3-110">Syntax</span></span>

 <span data-ttu-id="979e3-111">**FONT** _(font_name_string)_</span><span class="sxs-lookup"><span data-stu-id="979e3-111">**FONT**( _"font_name_string"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="979e3-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="979e3-112">Parameters</span></span>

|<span data-ttu-id="979e3-113">**Имя**</span><span class="sxs-lookup"><span data-stu-id="979e3-113">**Name**</span></span>|<span data-ttu-id="979e3-114">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="979e3-114">**Required/Optional**</span></span>|<span data-ttu-id="979e3-115">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="979e3-115">**Data Type**</span></span>|<span data-ttu-id="979e3-116">**Описание**</span><span class="sxs-lookup"><span data-stu-id="979e3-116">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="979e3-117">_font_name_string_</span><span class="sxs-lookup"><span data-stu-id="979e3-117">_font_name_string_</span></span> <br/> |<span data-ttu-id="979e3-118">Обязательный</span><span class="sxs-lookup"><span data-stu-id="979e3-118">Required</span></span>  <br/> |<span data-ttu-id="979e3-119">**строка**</span><span class="sxs-lookup"><span data-stu-id="979e3-119">**string**</span></span> <br/> |<span data-ttu-id="979e3-120">Имя шрифта.</span><span class="sxs-lookup"><span data-stu-id="979e3-120">The name of the font.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="979e3-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="979e3-121">Return value</span></span>

<span data-ttu-id="979e3-122">Целое число</span><span class="sxs-lookup"><span data-stu-id="979e3-122">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="979e3-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="979e3-123">Remarks</span></span>

<span data-ttu-id="979e3-124">Если строка,  *предусмотренная для font_name_string,*  не соответствует известному шрифту, эта функция возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="979e3-124">If the string provided for  *font_name_string*  does not match a known font, this function returns a #VALUE!</span></span> <span data-ttu-id="979e3-125">ошибка.</span><span class="sxs-lookup"><span data-stu-id="979e3-125">error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="979e3-126">Пример</span><span class="sxs-lookup"><span data-stu-id="979e3-126">Example</span></span>

 `FONT("Calibri")`
  
<span data-ttu-id="979e3-127">Возвращает значение integer (4), представляющее уникальный ID для шрифта "Calibri".</span><span class="sxs-lookup"><span data-stu-id="979e3-127">Returns the integer value (4) representing the unique ID for the "Calibri" font.</span></span>
  

