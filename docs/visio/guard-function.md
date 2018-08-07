---
title: Функция GUARD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251435
localization_priority: Normal
ms.assetid: 6c85414c-9fb6-cdc5-f5b6-8eb13c9608af
description: Защищает выражение от удаления или изменения от действий, выполняемых в окне документа, например, для перемещения, изменения размера, Группировка и разгруппировка фигур.
ms.openlocfilehash: fd5fcfbe11eb054dfa625834640c0280cae96c3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813870"
---
# <a name="guard-function"></a><span data-ttu-id="b9cca-103">Функция GUARD</span><span class="sxs-lookup"><span data-stu-id="b9cca-103">GUARD Function</span></span>

<span data-ttu-id="b9cca-104">Защищает *выражение* от удаления или изменения от действий, выполняемых в окне документа, например, для перемещения, изменения размера, Группировка и разгруппировка фигур.</span><span class="sxs-lookup"><span data-stu-id="b9cca-104">Protects  *expression*  from deletion and change by actions performed in the drawing window, for example, moving, sizing, grouping, or ungrouping shapes.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b9cca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9cca-105">Syntax</span></span>

<span data-ttu-id="b9cca-106">Защита (** *выражение* **)</span><span class="sxs-lookup"><span data-stu-id="b9cca-106">GUARD(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b9cca-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9cca-107">Parameters</span></span>

|<span data-ttu-id="b9cca-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="b9cca-108">**Name**</span></span>|<span data-ttu-id="b9cca-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="b9cca-109">**Required/Optional**</span></span>|<span data-ttu-id="b9cca-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="b9cca-110">**Data Type**</span></span>|<span data-ttu-id="b9cca-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b9cca-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b9cca-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="b9cca-112">_expression_</span></span> <br/> |<span data-ttu-id="b9cca-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b9cca-113">Required</span></span>  <br/> |<span data-ttu-id="b9cca-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="b9cca-114">**String**</span></span> <br/> |<span data-ttu-id="b9cca-115">Комбинация константы, операторы, функции и ссылки на ячейки таблицы свойств фигуры, которая приводит к значение.</span><span class="sxs-lookup"><span data-stu-id="b9cca-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9cca-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="b9cca-116">Remarks</span></span>

<span data-ttu-id="b9cca-117">Ячейки, чаще всего влияет на функции защиты, Width, Height, PinX и PinY.</span><span class="sxs-lookup"><span data-stu-id="b9cca-117">The cells most often affected by the GUARD function are Width, Height, PinX, and PinY.</span></span> 
  
<span data-ttu-id="b9cca-118">Защита формулы в любой ячейке запрещает эту ячейку значение изменений, вносимых действий в окне документа.</span><span class="sxs-lookup"><span data-stu-id="b9cca-118">Guarding a formula in any cell prevents that cell's value from being changed by actions in the drawing window.</span></span> <span data-ttu-id="b9cca-119">Тем не менее одно действие в окне документа может повлиять на несколько ячеек, и каждый из этих ячеек необходимо принимать меры, если вы хотите запретить непредвиденные изменения внешнего вида фигуры.</span><span class="sxs-lookup"><span data-stu-id="b9cca-119">However, one action in the drawing window can affect several cells, and each of these cells must be guarded if you want to prevent unexpected changes to the shape's appearance.</span></span> 
  
## <a name="example"></a><span data-ttu-id="b9cca-120">Пример</span><span class="sxs-lookup"><span data-stu-id="b9cca-120">Example</span></span>

<span data-ttu-id="b9cca-121">GUARD(TEXTWIDTH(TheText) + 0,5 in)</span><span class="sxs-lookup"><span data-stu-id="b9cca-121">GUARD(TEXTWIDTH(TheText) + 0.5 in)</span></span> 
  
<span data-ttu-id="b9cca-122">Это выражение в ячейке ширину раздела преобразования фигуры фигуры предотвращает выражения (TEXTWIDTH(TheText) + 0,5 in) замене другим значением при изменении ширины фигуры в окне документа.</span><span class="sxs-lookup"><span data-stu-id="b9cca-122">This expression in the Width cell of a shape's Shape Transform section prevents the expression (TEXTWIDTH(TheText) + 0.5 in) from being replaced with another value when the shape's width is changed in the drawing window.</span></span> <span data-ttu-id="b9cca-123">TheText — это ячейка, которая получает запускается при изменении связанных с фигурой текстовой композиции.</span><span class="sxs-lookup"><span data-stu-id="b9cca-123">TheText is a cell that gets triggered when the associated shape's text composition changes.</span></span> 
  

