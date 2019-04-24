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
description: Защищает выражение от удаления и изменения по действиям, выполняемым в окне документа, например при перемещении, изменении размера, группировании или разгруппировании фигур.
ms.openlocfilehash: 0bdfa023d53e739a970cab65b1dbd67bc1a44461
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360195"
---
# <a name="guard-function"></a><span data-ttu-id="5ab03-103">Функция GUARD</span><span class="sxs-lookup"><span data-stu-id="5ab03-103">GUARD Function</span></span>

<span data-ttu-id="5ab03-104">Защищает *выражение* от удаления и изменения по действиям, выполняемым в окне документа, например при перемещении, изменении размера, группировании или разгруппировании фигур.</span><span class="sxs-lookup"><span data-stu-id="5ab03-104">Protects  *expression*  from deletion and change by actions performed in the drawing window, for example, moving, sizing, grouping, or ungrouping shapes.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5ab03-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ab03-105">Syntax</span></span>

<span data-ttu-id="5ab03-106">GUARD (\* \* *Expression* \* \*)</span><span class="sxs-lookup"><span data-stu-id="5ab03-106">GUARD(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5ab03-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ab03-107">Parameters</span></span>

|<span data-ttu-id="5ab03-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="5ab03-108">**Name**</span></span>|<span data-ttu-id="5ab03-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="5ab03-109">**Required/Optional**</span></span>|<span data-ttu-id="5ab03-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="5ab03-110">**Data Type**</span></span>|<span data-ttu-id="5ab03-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5ab03-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5ab03-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="5ab03-112">_expression_</span></span> <br/> |<span data-ttu-id="5ab03-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5ab03-113">Required</span></span>  <br/> |<span data-ttu-id="5ab03-114">**String**</span><span class="sxs-lookup"><span data-stu-id="5ab03-114">**String**</span></span> <br/> |<span data-ttu-id="5ab03-115">Сочетание констант, операторов, функций и ссылок на ячейки таблицы свойств фигуры, в результате чего получается значение.</span><span class="sxs-lookup"><span data-stu-id="5ab03-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ab03-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="5ab03-116">Remarks</span></span>

<span data-ttu-id="5ab03-117">К ячейкам, которые чаще всего влияют функцией GUARD, относятся ширина, высота, PinX и PinY.</span><span class="sxs-lookup"><span data-stu-id="5ab03-117">The cells most often affected by the GUARD function are Width, Height, PinX, and PinY.</span></span> 
  
<span data-ttu-id="5ab03-118">Защита формулы в ячейках в любой ячейке не позволяет изменить значение этой ячейки с помощью действий в окне документа.</span><span class="sxs-lookup"><span data-stu-id="5ab03-118">Guarding a formula in any cell prevents that cell's value from being changed by actions in the drawing window.</span></span> <span data-ttu-id="5ab03-119">Однако одно действие в окне документа может повлиять на несколько ячеек, и каждая из этих ячеек должна быть защищена, если необходимо предотвратить непредвиденные изменения внешнего вида фигуры.</span><span class="sxs-lookup"><span data-stu-id="5ab03-119">However, one action in the drawing window can affect several cells, and each of these cells must be guarded if you want to prevent unexpected changes to the shape's appearance.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5ab03-120">Пример</span><span class="sxs-lookup"><span data-stu-id="5ab03-120">Example</span></span>

<span data-ttu-id="5ab03-121">GUARD (TEXTWIDTH (TheText) + 0,5 in)</span><span class="sxs-lookup"><span data-stu-id="5ab03-121">GUARD(TEXTWIDTH(TheText) + 0.5 in)</span></span> 
  
<span data-ttu-id="5ab03-122">Это выражение в ячейке "ширина" в разделе "Преобразование фигуры фигуры" запрещает замену выражения (TEXTWIDTH (TheText) + 0,5 in) на другое значение при изменении ширины фигуры в окне документа.</span><span class="sxs-lookup"><span data-stu-id="5ab03-122">This expression in the Width cell of a shape's Shape Transform section prevents the expression (TEXTWIDTH(TheText) + 0.5 in) from being replaced with another value when the shape's width is changed in the drawing window.</span></span> <span data-ttu-id="5ab03-123">TheText — ячейка, которая вызывается при изменении композиции текста связанной фигуры.</span><span class="sxs-lookup"><span data-stu-id="5ab03-123">TheText is a cell that gets triggered when the associated shape's text composition changes.</span></span> 
  

