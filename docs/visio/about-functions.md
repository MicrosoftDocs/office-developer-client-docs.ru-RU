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
description: 'Функция выполняет одну четко определяемую задачу. Большинство функций принимают в качестве входных данных несколько аргументов. Хотя тип и число аргументов зависят от функции, все функции имеют одинаковый общий синтаксис:'
ms.openlocfilehash: 14995b0f7e3c1cc8346d47965038902b8ca4e8bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415980"
---
# <a name="about-functions"></a><span data-ttu-id="2a1d2-105">О функциях</span><span class="sxs-lookup"><span data-stu-id="2a1d2-105">About Functions</span></span>

<span data-ttu-id="2a1d2-106">Функция выполняет одну четко определяемую задачу.</span><span class="sxs-lookup"><span data-stu-id="2a1d2-106">A function performs a single well-defined task.</span></span> <span data-ttu-id="2a1d2-107">Большинство функций принимают в качестве входных данных несколько аргументов.</span><span class="sxs-lookup"><span data-stu-id="2a1d2-107">Most functions take a number of arguments as input.</span></span> <span data-ttu-id="2a1d2-108">Хотя тип и число аргументов зависят от функции, все функции имеют одинаковый общий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="2a1d2-108">Although the type and number of arguments depend on the function, all functions have the same general syntax:</span></span>
  
 <span data-ttu-id="2a1d2-109">**FUNCTION(** _argument1_,  _argument2_, ...</span><span class="sxs-lookup"><span data-stu-id="2a1d2-109">**FUNCTION(** _argument1_,  _argument2_, …</span></span>  <span data-ttu-id="2a1d2-110">_argumentN_ [, _argumentA_  |   _argument_ **])**</span><span class="sxs-lookup"><span data-stu-id="2a1d2-110">_argumentN_ [,  _argumentA_ |  _argument_ **])**</span></span>
  
|<span data-ttu-id="2a1d2-111">**Элемент Syntax**</span><span class="sxs-lookup"><span data-stu-id="2a1d2-111">**Syntax element**</span></span>|<span data-ttu-id="2a1d2-112">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2a1d2-112">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2a1d2-113">( )</span><span class="sxs-lookup"><span data-stu-id="2a1d2-113">( )</span></span>  <br/> | <span data-ttu-id="2a1d2-114">Если функция не принимает аргументы, за ней должен следовать пустой набор скобок ( ).</span><span class="sxs-lookup"><span data-stu-id="2a1d2-114">If a function takes no arguments, it must be followed by an empty set of parentheses ( ).</span></span>  <br/> |
| <span data-ttu-id="2a1d2-115">,</span><span class="sxs-lookup"><span data-stu-id="2a1d2-115">,</span></span>  <br/> | <span data-ttu-id="2a1d2-116">Аргументы разделяются запятой.</span><span class="sxs-lookup"><span data-stu-id="2a1d2-116">Arguments are separated by a comma.</span></span>  <br/> |
| <span data-ttu-id="2a1d2-117">...</span><span class="sxs-lookup"><span data-stu-id="2a1d2-117">...</span></span>  <br/> | <span data-ttu-id="2a1d2-118">Используется только для нотации; не включаем в функцию.</span><span class="sxs-lookup"><span data-stu-id="2a1d2-118">Used for notation only; do not include in a function.</span></span>  <br/> |
| <span data-ttu-id="2a1d2-119">[ ]</span><span class="sxs-lookup"><span data-stu-id="2a1d2-119">[ ]</span></span>  <br/> | <span data-ttu-id="2a1d2-120">Необязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="2a1d2-120">Optional argument.</span></span> <span data-ttu-id="2a1d2-121">Используется только для нотации; не включаем в функцию.</span><span class="sxs-lookup"><span data-stu-id="2a1d2-121">Used for notation only; do not include in a function.</span></span>  <br/> |
| |  <br/> | <span data-ttu-id="2a1d2-122">Выбор; можно включить  _аргументA или_  _аргумент_.</span><span class="sxs-lookup"><span data-stu-id="2a1d2-122">A choice; you can include  _argumentA_ or  _argument_.</span></span> <span data-ttu-id="2a1d2-123">Используется только для нотации; не включаем в функцию.</span><span class="sxs-lookup"><span data-stu-id="2a1d2-123">Used for notation only; do not include in a function.</span></span>  <br/> |
   
<span data-ttu-id="2a1d2-124">Многие функции, которые можно использовать в формулах, похожи на функции, которые вы видели в программах для работы с электронными таблицами: математические, такие как СУММ или SQRT; тригонометрия, например SIN или COS; или логический, например IF или NOT.</span><span class="sxs-lookup"><span data-stu-id="2a1d2-124">Many functions that you can use in formulas resemble those you have seen in spreadsheet programs: mathematical, such as SUM or SQRT; trigonometric, such as SIN or COS; or logical, such as IF or NOT.</span></span> <span data-ttu-id="2a1d2-125">Многие другие функции уникальны для Microsoft Office Visio, например GUARD, GRAVITY и RUNADDON.</span><span class="sxs-lookup"><span data-stu-id="2a1d2-125">Many other functions are unique to Microsoft Office Visio, such as GUARD, GRAVITY, and RUNADDON.</span></span>
  
<span data-ttu-id="2a1d2-126">Дополнительные сведения о конкретных функциях см. в этом справочнике по таблицам фигур.</span><span class="sxs-lookup"><span data-stu-id="2a1d2-126">For more information on specific functions, see this ShapeSheet Reference.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="2a1d2-127">Некоторые функции отображаются в формулах, созданных Visio, но не отображаются в диалоговом окне "Изменить формулу" или описаны в этой ссылке, так как они зарезервированы для внутреннего использования и не должны использоваться в других формулах. </span><span class="sxs-lookup"><span data-stu-id="2a1d2-127">Certain functions appear in formulas generated by Visio, but are not shown in the **Edit Formula** dialog box or described in this reference because they are reserved for internal use and should not be used in other formulas.</span></span> <span data-ttu-id="2a1d2-128">Ниже примеры: ELLIPSE_THETA, _ELLIPSE_ECC, _UCON_C1 и _SHAPEMIN.</span><span class="sxs-lookup"><span data-stu-id="2a1d2-128">Following are examples: ELLIPSE_THETA, _ELLIPSE_ECC, _UCON_C1, and _SHAPEMIN.</span></span> 
  

