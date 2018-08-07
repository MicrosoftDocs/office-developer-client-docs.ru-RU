---
title: Функция FIELDPICTURE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251592
localization_priority: Normal
ms.assetid: df88c55f-c098-dd4c-bf53-c7d7b60cf719
description: Возвращает строку формата изображения, соответствующее поле формат Microsoft Visio внутренний текст кода.
ms.openlocfilehash: 1528cefd65ed0c7c1dde02fa390babf26442b4d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813728"
---
# <a name="fieldpicture-function"></a><span data-ttu-id="5775e-103">Функция FIELDPICTURE</span><span class="sxs-lookup"><span data-stu-id="5775e-103">FIELDPICTURE Function</span></span>

<span data-ttu-id="5775e-104">Возвращает строку формата изображения, соответствующее поле формат Microsoft Visio внутренний текст кода.</span><span class="sxs-lookup"><span data-stu-id="5775e-104">Returns a format-picture string that matches the Microsoft Visio internal text field format code.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5775e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5775e-105">Syntax</span></span>

<span data-ttu-id="5775e-106">FIELDPICTURE (** *кода* **)</span><span class="sxs-lookup"><span data-stu-id="5775e-106">FIELDPICTURE(** *code* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5775e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5775e-107">Parameters</span></span>

|<span data-ttu-id="5775e-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="5775e-108">**Name**</span></span>|<span data-ttu-id="5775e-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="5775e-109">**Required/Optional**</span></span>|<span data-ttu-id="5775e-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="5775e-110">**Data Type**</span></span>|<span data-ttu-id="5775e-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5775e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5775e-112">_code_</span><span class="sxs-lookup"><span data-stu-id="5775e-112">_code_</span></span> <br/> |<span data-ttu-id="5775e-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5775e-113">Required</span></span>  <br/> |<span data-ttu-id="5775e-114">**Число**</span><span class="sxs-lookup"><span data-stu-id="5775e-114">**Number**</span></span> <br/> | <span data-ttu-id="5775e-115">Код формата текстового поля.</span><span class="sxs-lookup"><span data-stu-id="5775e-115">A text field format code.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5775e-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6">Return value</span></span>

<span data-ttu-id="5775e-117">Строка</span><span class="sxs-lookup"><span data-stu-id="5775e-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5775e-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="5775e-118">Remarks</span></span>

<span data-ttu-id="5775e-119">В функции FORMAT для определения расширения значения даты, времени, чисел и заголовки устройства используются строки изображение формата.</span><span class="sxs-lookup"><span data-stu-id="5775e-119">Format picture strings are used in the FORMAT function to define the expansion of values to dates, times, numbers, and unit labels.</span></span>
  
## <a name="example"></a><span data-ttu-id="5775e-120">Пример</span><span class="sxs-lookup"><span data-stu-id="5775e-120">Example</span></span>

<span data-ttu-id="5775e-121">FIELDPICTURE(0)</span><span class="sxs-lookup"><span data-stu-id="5775e-121">FIELDPICTURE(0)</span></span> 
  
<span data-ttu-id="5775e-122">Возвращает строку формата рисунок «esc(0)», который указывает номер, который имеет один десятичный и описание строчная единицу при использовании функции FORMAT.</span><span class="sxs-lookup"><span data-stu-id="5775e-122">Returns the format picture string "esc(0)", which specifies a number that has one decimal place and a lowercase unit description when used in the FORMAT function.</span></span> 
  

