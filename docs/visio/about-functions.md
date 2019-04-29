---
title: Сведения о функциях
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251825
localization_priority: Normal
ms.assetid: 871b8601-8117-bc51-17b9-6002234b4bfb
description: 'Функция выполняет одну строго определенную задачу. Большинство функций в качестве входных данных используют несколько аргументов. Несмотря на то, что тип и количество аргументов зависят от функции, все функции имеют одинаковый общий синтаксис:'
ms.openlocfilehash: 14995b0f7e3c1cc8346d47965038902b8ca4e8bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415980"
---
# <a name="about-functions"></a><span data-ttu-id="33f11-105">Сведения о функциях</span><span class="sxs-lookup"><span data-stu-id="33f11-105">About Functions</span></span>

<span data-ttu-id="33f11-106">Функция выполняет одну строго определенную задачу.</span><span class="sxs-lookup"><span data-stu-id="33f11-106">A function performs a single well-defined task.</span></span> <span data-ttu-id="33f11-107">Большинство функций в качестве входных данных используют несколько аргументов.</span><span class="sxs-lookup"><span data-stu-id="33f11-107">Most functions take a number of arguments as input.</span></span> <span data-ttu-id="33f11-108">Несмотря на то, что тип и количество аргументов зависят от функции, все функции имеют одинаковый общий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="33f11-108">Although the type and number of arguments depend on the function, all functions have the same general syntax:</span></span>
  
 <span data-ttu-id="33f11-109">**Функция (** _argument1_, _argument2_,...</span><span class="sxs-lookup"><span data-stu-id="33f11-109">**FUNCTION(** _argument1_,  _argument2_, …</span></span>  <span data-ttu-id="33f11-110">_аргументн_ [, _аргумент_ |  __ , аргумент **])**</span><span class="sxs-lookup"><span data-stu-id="33f11-110">_argumentN_ [,  _argumentA_ |  _argument_ **])**</span></span>
  
|<span data-ttu-id="33f11-111">**Элемент синтаксиса**</span><span class="sxs-lookup"><span data-stu-id="33f11-111">**Syntax element**</span></span>|<span data-ttu-id="33f11-112">**Описание**</span><span class="sxs-lookup"><span data-stu-id="33f11-112">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="33f11-113">( )</span><span class="sxs-lookup"><span data-stu-id="33f11-113"></span></span>  <br/> | <span data-ttu-id="33f11-114">Если функция не принимает аргументы, ей должен следовать пустой набор скобок ().</span><span class="sxs-lookup"><span data-stu-id="33f11-114">If a function takes no arguments, it must be followed by an empty set of parentheses ( ).</span></span>  <br/> |
| <span data-ttu-id="33f11-115">,</span><span class="sxs-lookup"><span data-stu-id="33f11-115"></span></span>  <br/> | <span data-ttu-id="33f11-116">Аргументы разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="33f11-116">Arguments are separated by a comma.</span></span>  <br/> |
| <span data-ttu-id="33f11-117">...</span><span class="sxs-lookup"><span data-stu-id="33f11-117"></span></span>  <br/> | <span data-ttu-id="33f11-118">Используется только для обозначения; не включайте в функцию.</span><span class="sxs-lookup"><span data-stu-id="33f11-118">Used for notation only; do not include in a function.</span></span>  <br/> |
| <span data-ttu-id="33f11-119">[ ]</span><span class="sxs-lookup"><span data-stu-id="33f11-119"></span></span>  <br/> | <span data-ttu-id="33f11-120">НеОбязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="33f11-120">Optional argument.</span></span> <span data-ttu-id="33f11-121">Используется только для обозначения; не включайте в функцию.</span><span class="sxs-lookup"><span data-stu-id="33f11-121">Used for notation only; do not include in a function.</span></span>  <br/> |
| |  <br/> | <span data-ttu-id="33f11-122">Выбор; Допускается включение _аргумента_ или аргумента. __</span><span class="sxs-lookup"><span data-stu-id="33f11-122">A choice; you can include  _argumentA_ or  _argument_.</span></span> <span data-ttu-id="33f11-123">Используется только для обозначения; не включайте в функцию.</span><span class="sxs-lookup"><span data-stu-id="33f11-123">Used for notation only; do not include in a function.</span></span>  <br/> |
   
<span data-ttu-id="33f11-124">Многие функции, которые можно использовать в формулах, похожи на те, что отображаются в программах для работы с электронными таблицами: математические, такие как SUM или SQRT; тригонометрия, например SIN или COS; или логическое, например IF.</span><span class="sxs-lookup"><span data-stu-id="33f11-124">Many functions that you can use in formulas resemble those you have seen in spreadsheet programs: mathematical, such as SUM or SQRT; trigonometric, such as SIN or COS; or logical, such as IF or NOT.</span></span> <span data-ttu-id="33f11-125">Многие другие функции уникальны для Microsoft Office Visio, например "GUARD", "сила ПРИТЯЖЕНИя" и "RUNADDON".</span><span class="sxs-lookup"><span data-stu-id="33f11-125">Many other functions are unique to Microsoft Office Visio, such as GUARD, GRAVITY, and RUNADDON.</span></span>
  
<span data-ttu-id="33f11-126">Для получения дополнительных сведений об определенных функциях, ознакомьтесь с этой ссылкой на таблицу свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="33f11-126">For more information on specific functions, see this ShapeSheet Reference.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="33f11-127">Некоторые функции отображаются в формулах, создаваемых Visio, но не отображаются в диалоговом окне **изменить формулу** или описаны в этой ссылке, так как они зарезервированы для внутреннего использования и не должны использоваться в других формулах.</span><span class="sxs-lookup"><span data-stu-id="33f11-127">Certain functions appear in formulas generated by Visio, but are not shown in the **Edit Formula** dialog box or described in this reference because they are reserved for internal use and should not be used in other formulas.</span></span> <span data-ttu-id="33f11-128">Ниже приведены примеры: ЕЛЛИПСЕ_СЕТА, _ЕЛЛИПСЕ_ЕКК, _UCON_C1 и _ШАПЕМИН.</span><span class="sxs-lookup"><span data-stu-id="33f11-128">Following are examples: ELLIPSE_THETA, _ELLIPSE_ECC, _UCON_C1, and _SHAPEMIN.</span></span> 
  

