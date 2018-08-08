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
description: 'Функция выполняет один четко определенной задачи. Большинство функций вступили число аргументов в качестве входных данных. Несмотря на то, что тип и количество аргументов зависят от функции, все функции имеют один и тот же общий синтаксис:'
ms.openlocfilehash: 21cf02d1bb3d6a33daa10ba62efc29c5b35a11cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813123"
---
# <a name="about-functions"></a><span data-ttu-id="f7707-105">Сведения о функциях</span><span class="sxs-lookup"><span data-stu-id="f7707-105">About Functions</span></span>

<span data-ttu-id="f7707-106">Функция выполняет один четко определенной задачи.</span><span class="sxs-lookup"><span data-stu-id="f7707-106">A function performs a single well-defined task.</span></span> <span data-ttu-id="f7707-107">Большинство функций вступили число аргументов в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="f7707-107">Most functions take a number of arguments as input.</span></span> <span data-ttu-id="f7707-108">Несмотря на то, что тип и количество аргументов зависят от функции, все функции имеют один и тот же общий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="f7707-108">Although the type and number of arguments depend on the function, all functions have the same general syntax:</span></span>
  
 <span data-ttu-id="f7707-109">**Функции (** _аргумент1_, _аргумент2_,...</span><span class="sxs-lookup"><span data-stu-id="f7707-109">**FUNCTION(** _argument1_,  _argument2_, …</span></span>  <span data-ttu-id="f7707-110">_argumentN_ [, _argumentA_ |  _аргумент_ **])**</span><span class="sxs-lookup"><span data-stu-id="f7707-110">_argumentN_ [,  _argumentA_ |  _argument_ **])**</span></span>
  
|<span data-ttu-id="f7707-111">**Синтаксис элемента**</span><span class="sxs-lookup"><span data-stu-id="f7707-111">**Syntax element**</span></span>|<span data-ttu-id="f7707-112">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f7707-112">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f7707-113">( )</span><span class="sxs-lookup"><span data-stu-id="f7707-113"></span></span>  <br/> | <span data-ttu-id="f7707-114">Если функция не принимает аргументы, он должен следовать пустой набор скобки ().</span><span class="sxs-lookup"><span data-stu-id="f7707-114">If a function takes no arguments, it must be followed by an empty set of parentheses ( ).</span></span>  <br/> |
| <span data-ttu-id="f7707-115">,</span><span class="sxs-lookup"><span data-stu-id="f7707-115"></span></span>  <br/> | <span data-ttu-id="f7707-116">Аргументы, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="f7707-116">Arguments are separated by a comma.</span></span>  <br/> |
| <span data-ttu-id="f7707-117">...</span><span class="sxs-lookup"><span data-stu-id="f7707-117"></span></span>  <br/> | <span data-ttu-id="f7707-118">Используется для нотацию только; не включайте в функции.</span><span class="sxs-lookup"><span data-stu-id="f7707-118">Used for notation only; do not include in a function.</span></span>  <br/> |
| <span data-ttu-id="f7707-119">[ ]</span><span class="sxs-lookup"><span data-stu-id="f7707-119"></span></span>  <br/> | <span data-ttu-id="f7707-120">Необязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="f7707-120">Optional argument.</span></span> <span data-ttu-id="f7707-121">Используется для нотацию только; не включайте в функции.</span><span class="sxs-lookup"><span data-stu-id="f7707-121">Used for notation only; do not include in a function.</span></span>  <br/> |
| |  <br/> | <span data-ttu-id="f7707-122">Выбор; может включать _argumentA_ или _аргумент_.</span><span class="sxs-lookup"><span data-stu-id="f7707-122">A choice; you can include  _argumentA_ or  _argument_.</span></span> <span data-ttu-id="f7707-123">Используется для нотацию только; не включайте в функции.</span><span class="sxs-lookup"><span data-stu-id="f7707-123">Used for notation only; do not include in a function.</span></span>  <br/> |
   
<span data-ttu-id="f7707-124">Многие функции, которые можно использовать в формулах, которые похожи видно в электронных таблицах: математических, такие как SUM или корень; тригонометрических, например SIN или COS; или логическим, например, если нет.</span><span class="sxs-lookup"><span data-stu-id="f7707-124">Many functions that you can use in formulas resemble those you have seen in spreadsheet programs: mathematical, such as SUM or SQRT; trigonometric, such as SIN or COS; or logical, such as IF or NOT.</span></span> <span data-ttu-id="f7707-125">Другие функции являются уникальными для Microsoft Office Visio, такие как защита, ВЕСА и RUNADDON.</span><span class="sxs-lookup"><span data-stu-id="f7707-125">Many other functions are unique to Microsoft Office Visio, such as GUARD, GRAVITY, and RUNADDON.</span></span>
  
<span data-ttu-id="f7707-126">Дополнительные сведения о конкретных функций видеть этот справочник по таблице свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="f7707-126">For more information on specific functions, see this ShapeSheet Reference.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="f7707-127">Определенные функции отображаются в формулах, созданных функцией Visio, но не отображаются в диалоговом окне **Изменить формулу** или описанные в этой справке, так как они зарезервированы для внутреннего использования и не должен использоваться в других формулах.</span><span class="sxs-lookup"><span data-stu-id="f7707-127">Certain functions appear in formulas generated by Visio, but are not shown in the **Edit Formula** dialog box or described in this reference because they are reserved for internal use and should not be used in other formulas.</span></span> <span data-ttu-id="f7707-128">Ниже приведены примеры: ELLIPSE_THETA, _ELLIPSE_ECC, _UCON_C1 и _SHAPEMIN.</span><span class="sxs-lookup"><span data-stu-id="f7707-128">Following are examples: ELLIPSE_THETA, _ELLIPSE_ECC, _UCON_C1, and _SHAPEMIN.</span></span> 
  

