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
description: Защищает выражение от удаления и изменения действиями, выполняемыми в окне рисования, например, перемещением, размером, группировкой или разгруппировка фигур.
ms.openlocfilehash: 0bdfa023d53e739a970cab65b1dbd67bc1a44461
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408154"
---
# <a name="guard-function"></a><span data-ttu-id="cdaa8-103">Функция GUARD</span><span class="sxs-lookup"><span data-stu-id="cdaa8-103">GUARD Function</span></span>

<span data-ttu-id="cdaa8-104">Защищает  *выражение*  от удаления и изменения действиями, выполняемыми в окне рисования, например, перемещением, размером, группировкой или разгруппировка фигур.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-104">Protects  *expression*  from deletion and change by actions performed in the drawing window, for example, moving, sizing, grouping, or ungrouping shapes.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="cdaa8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cdaa8-105">Syntax</span></span>

<span data-ttu-id="cdaa8-106">GUARD(\*\* *выражение* \*\* )</span><span class="sxs-lookup"><span data-stu-id="cdaa8-106">GUARD(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="cdaa8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cdaa8-107">Parameters</span></span>

|<span data-ttu-id="cdaa8-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="cdaa8-108">**Name**</span></span>|<span data-ttu-id="cdaa8-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="cdaa8-109">**Required/Optional**</span></span>|<span data-ttu-id="cdaa8-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="cdaa8-110">**Data Type**</span></span>|<span data-ttu-id="cdaa8-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cdaa8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="cdaa8-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="cdaa8-112">_expression_</span></span> <br/> |<span data-ttu-id="cdaa8-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="cdaa8-113">Required</span></span>  <br/> |<span data-ttu-id="cdaa8-114">**String**</span><span class="sxs-lookup"><span data-stu-id="cdaa8-114">**String**</span></span> <br/> |<span data-ttu-id="cdaa8-115">Сочетание констант, операторов, функций и ссылок на ячейки ShapeSheet, что приводит к значению.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cdaa8-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="cdaa8-116">Remarks</span></span>

<span data-ttu-id="cdaa8-117">Чаще всего функцией GUARD страдают ячейки Ширина, Высота, PinX и PinY.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-117">The cells most often affected by the GUARD function are Width, Height, PinX, and PinY.</span></span> 
  
<span data-ttu-id="cdaa8-118">Охрана формулы в любой ячейке не позволяет изменить значение этой ячейки действиями в окне рисования.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-118">Guarding a formula in any cell prevents that cell's value from being changed by actions in the drawing window.</span></span> <span data-ttu-id="cdaa8-119">Однако одно действие в окне рисования может повлиять на несколько ячеек, и каждая из этих ячеек должна быть охраняема, если вы хотите предотвратить неожиданные изменения внешнего вида фигуры.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-119">However, one action in the drawing window can affect several cells, and each of these cells must be guarded if you want to prevent unexpected changes to the shape's appearance.</span></span> 
  
## <a name="example"></a><span data-ttu-id="cdaa8-120">Пример</span><span class="sxs-lookup"><span data-stu-id="cdaa8-120">Example</span></span>

<span data-ttu-id="cdaa8-121">GUARD (TEXTWIDTH(TheText) + 0.5 in)</span><span class="sxs-lookup"><span data-stu-id="cdaa8-121">GUARD(TEXTWIDTH(TheText) + 0.5 in)</span></span> 
  
<span data-ttu-id="cdaa8-122">Это выражение в ячейке Ширина раздела Преобразование формы формы предотвращает замену выражения (TEXTWIDTH (TheText) + 0.5 in на другое значение при смене ширины формы в окне рисования.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-122">This expression in the Width cell of a shape's Shape Transform section prevents the expression (TEXTWIDTH(TheText) + 0.5 in) from being replaced with another value when the shape's width is changed in the drawing window.</span></span> <span data-ttu-id="cdaa8-123">TheText — это ячейка, которая запускается при смене текстовой композиции связанной фигуры.</span><span class="sxs-lookup"><span data-stu-id="cdaa8-123">TheText is a cell that gets triggered when the associated shape's text composition changes.</span></span> 
  

