---
title: О функциях
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251825
localization_priority: Normal
ms.assetid: 871b8601-8117-bc51-17b9-6002234b4bfb
description: 'Функция выполняет одно четко определенное задание. Большинство функций принимает ряд аргументов в качестве ввода. Хотя тип и количество аргументов зависят от функции, все функции имеют один и тот же общий синтаксис:'
ms.openlocfilehash: 14995b0f7e3c1cc8346d47965038902b8ca4e8bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415980"
---
# <a name="about-functions"></a><span data-ttu-id="a02ff-105">О функциях</span><span class="sxs-lookup"><span data-stu-id="a02ff-105">About Functions</span></span>

<span data-ttu-id="a02ff-106">Функция выполняет одно четко определенное задание.</span><span class="sxs-lookup"><span data-stu-id="a02ff-106">A function performs a single well-defined task.</span></span> <span data-ttu-id="a02ff-107">Большинство функций принимает ряд аргументов в качестве ввода.</span><span class="sxs-lookup"><span data-stu-id="a02ff-107">Most functions take a number of arguments as input.</span></span> <span data-ttu-id="a02ff-108">Хотя тип и количество аргументов зависят от функции, все функции имеют один и тот же общий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="a02ff-108">Although the type and number of arguments depend on the function, all functions have the same general syntax:</span></span>
  
 <span data-ttu-id="a02ff-109">**FUNCTION** _(argument1_,  _argument2_, ...</span><span class="sxs-lookup"><span data-stu-id="a02ff-109">**FUNCTION(** _argument1_,  _argument2_, …</span></span>  <span data-ttu-id="a02ff-110">_argumentN_ [, _argumentA_  |   _argument_ **])**</span><span class="sxs-lookup"><span data-stu-id="a02ff-110">_argumentN_ [,  _argumentA_ |  _argument_ **])**</span></span>
  
|<span data-ttu-id="a02ff-111">**Элемент Синтаксиса**</span><span class="sxs-lookup"><span data-stu-id="a02ff-111">**Syntax element**</span></span>|<span data-ttu-id="a02ff-112">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a02ff-112">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a02ff-113">( )</span><span class="sxs-lookup"><span data-stu-id="a02ff-113">( )</span></span>  <br/> | <span data-ttu-id="a02ff-114">Если функция не принимает аргументов, за ней следует пустой набор скобок ( ).</span><span class="sxs-lookup"><span data-stu-id="a02ff-114">If a function takes no arguments, it must be followed by an empty set of parentheses ( ).</span></span>  <br/> |
| <span data-ttu-id="a02ff-115">,</span><span class="sxs-lookup"><span data-stu-id="a02ff-115">,</span></span>  <br/> | <span data-ttu-id="a02ff-116">Аргументы разделены запятой.</span><span class="sxs-lookup"><span data-stu-id="a02ff-116">Arguments are separated by a comma.</span></span>  <br/> |
| <span data-ttu-id="a02ff-117">...</span><span class="sxs-lookup"><span data-stu-id="a02ff-117">...</span></span>  <br/> | <span data-ttu-id="a02ff-118">Используется только для нотации; не включаются в функцию.</span><span class="sxs-lookup"><span data-stu-id="a02ff-118">Used for notation only; do not include in a function.</span></span>  <br/> |
| <span data-ttu-id="a02ff-119">[ ]</span><span class="sxs-lookup"><span data-stu-id="a02ff-119">[ ]</span></span>  <br/> | <span data-ttu-id="a02ff-120">Необязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="a02ff-120">Optional argument.</span></span> <span data-ttu-id="a02ff-121">Используется только для нотации; не включаются в функцию.</span><span class="sxs-lookup"><span data-stu-id="a02ff-121">Used for notation only; do not include in a function.</span></span>  <br/> |
| |  <br/> | <span data-ttu-id="a02ff-122">Выбор; вы можете включить  _argumentA или_  _аргумент_.</span><span class="sxs-lookup"><span data-stu-id="a02ff-122">A choice; you can include  _argumentA_ or  _argument_.</span></span> <span data-ttu-id="a02ff-123">Используется только для нотации; не включаются в функцию.</span><span class="sxs-lookup"><span data-stu-id="a02ff-123">Used for notation only; do not include in a function.</span></span>  <br/> |
   
<span data-ttu-id="a02ff-124">Многие функции, которые можно использовать в формулах, похожи на те, которые вы видели в программах электронных таблиц: математические, такие как SUM или SQRT; тригонометрический, например SIN или COS; или логически, например IF или NOT.</span><span class="sxs-lookup"><span data-stu-id="a02ff-124">Many functions that you can use in formulas resemble those you have seen in spreadsheet programs: mathematical, such as SUM or SQRT; trigonometric, such as SIN or COS; or logical, such as IF or NOT.</span></span> <span data-ttu-id="a02ff-125">Многие другие функции уникальны для Microsoft Office Visio, например GUARD, GRAVITY и RUNADDON.</span><span class="sxs-lookup"><span data-stu-id="a02ff-125">Many other functions are unique to Microsoft Office Visio, such as GUARD, GRAVITY, and RUNADDON.</span></span>
  
<span data-ttu-id="a02ff-126">Дополнительные сведения о конкретных функциях см. в этой ссылке На таблицу ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="a02ff-126">For more information on specific functions, see this ShapeSheet Reference.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="a02ff-127">Некоторые функции отображаются в формулах, созданных Visio, но не отображаются в диалоговом окне **Edit Formula** или описаны в этой ссылке, поскольку они зарезервированы для внутреннего использования и не должны использоваться в других формулах.</span><span class="sxs-lookup"><span data-stu-id="a02ff-127">Certain functions appear in formulas generated by Visio, but are not shown in the **Edit Formula** dialog box or described in this reference because they are reserved for internal use and should not be used in other formulas.</span></span> <span data-ttu-id="a02ff-128">Ниже приводится пример: ELLIPSE_THETA, _ELLIPSE_ECC, _UCON_C1 и _SHAPEMIN.</span><span class="sxs-lookup"><span data-stu-id="a02ff-128">Following are examples: ELLIPSE_THETA, _ELLIPSE_ECC, _UCON_C1, and _SHAPEMIN.</span></span> 
  

