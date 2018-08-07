---
title: Функция FONT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Возвращает целое значение уникальный идентификатор для шрифта, указанный в параметре name.
ms.openlocfilehash: 4afd2aa05f2103675bf0df8db5cc7ea21f45fe71
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813804"
---
# <a name="font-function"></a><span data-ttu-id="0bc71-103">Функция FONT</span><span class="sxs-lookup"><span data-stu-id="0bc71-103">FONT Function</span></span>

<span data-ttu-id="0bc71-104">Возвращает целое значение уникальный идентификатор для шрифта, указанный в параметре name.</span><span class="sxs-lookup"><span data-stu-id="0bc71-104">Returns the integer value of the unique identifier for a font, specified by name.</span></span>
  
> [!NOTE]
> <span data-ttu-id="0bc71-105">В большинстве случаев идентификатор шрифта относящиеся к системе.</span><span class="sxs-lookup"><span data-stu-id="0bc71-105">In most cases, the font identifier is system-specific.</span></span> <span data-ttu-id="0bc71-106">Хотя шрифта остается установленным один раз используется в файле, функция **ШРИФТА** предоставляет согласованный доступ для определенного шрифта в системах и версий Visio.</span><span class="sxs-lookup"><span data-stu-id="0bc71-106">Although the font remains established once used in a file, the **FONT** function provides consistent access to a particular font across systems and versions of Visio.</span></span> <span data-ttu-id="0bc71-107">Рекомендуется использовать функцию **ШРИФТА** для назначения шрифты вместо непосредственно идентификаторы шрифта.</span><span class="sxs-lookup"><span data-stu-id="0bc71-107">It is recommended that you use the **FONT** function to assign fonts instead of referring to font identifiers directly.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="0bc71-108">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="0bc71-108">Version Information</span></span>

<span data-ttu-id="0bc71-109">Добавлена версия: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="0bc71-109">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0bc71-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0bc71-110">Syntax</span></span>

 <span data-ttu-id="0bc71-111">**ШРИФТ** ( _«font_name_string»_)</span><span class="sxs-lookup"><span data-stu-id="0bc71-111">**FONT**( _"font_name_string"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="0bc71-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bc71-112">Parameters</span></span>

|<span data-ttu-id="0bc71-113">**Имя**</span><span class="sxs-lookup"><span data-stu-id="0bc71-113">**Name**</span></span>|<span data-ttu-id="0bc71-114">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="0bc71-114">**Required/Optional**</span></span>|<span data-ttu-id="0bc71-115">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="0bc71-115">**Data Type**</span></span>|<span data-ttu-id="0bc71-116">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0bc71-116">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0bc71-117">_font_name_string_</span><span class="sxs-lookup"><span data-stu-id="0bc71-117">_font_name_string_</span></span> <br/> |<span data-ttu-id="0bc71-118">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0bc71-118">Required</span></span>  <br/> |<span data-ttu-id="0bc71-119">**string**</span><span class="sxs-lookup"><span data-stu-id="0bc71-119">**string**</span></span> <br/> |<span data-ttu-id="0bc71-120">Имя шрифта.</span><span class="sxs-lookup"><span data-stu-id="0bc71-120">The name of the font.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="0bc71-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1">Return value</span></span>

<span data-ttu-id="0bc71-122">Целое число</span><span class="sxs-lookup"><span data-stu-id="0bc71-122">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0bc71-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="0bc71-123">Remarks</span></span>

<span data-ttu-id="0bc71-124">Если строка для *font_name_string* не соответствует известной шрифта, эта функция возвращает #VALUE!</span><span class="sxs-lookup"><span data-stu-id="0bc71-124">If the string provided for  *font_name_string*  does not match a known font, this function returns a #VALUE!</span></span> <span data-ttu-id="0bc71-125">Ошибка.</span><span class="sxs-lookup"><span data-stu-id="0bc71-125">error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="0bc71-126">Пример</span><span class="sxs-lookup"><span data-stu-id="0bc71-126">Example</span></span>

 `FONT("Calibri")`
  
<span data-ttu-id="0bc71-127">Возвращает целое значение, представляющее уникальный идентификатор для шрифта «Calibri» (4).</span><span class="sxs-lookup"><span data-stu-id="0bc71-127">Returns the integer value (4) representing the unique ID for the "Calibri" font.</span></span>
  

