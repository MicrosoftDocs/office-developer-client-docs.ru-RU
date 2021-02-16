---
title: Функция GETVAL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251885
localization_priority: Normal
ms.assetid: 1da42991-5791-ebab-84cc-286cfe984a61
description: Получает значение ячейки и не пересчитывает формулу при смене значения ячейки.
ms.openlocfilehash: 9449ccd8f849b23faf08ee25826301a1b6efe6d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416890"
---
# <a name="getval-function"></a><span data-ttu-id="d301c-103">Функция GETVAL</span><span class="sxs-lookup"><span data-stu-id="d301c-103">GETVAL Function</span></span>

<span data-ttu-id="d301c-104">Получает значение ячейки и не пересчитывает формулу при смене значения ячейки.</span><span class="sxs-lookup"><span data-stu-id="d301c-104">Gets the value of a cell and doesn't recalculate the formula when the cell's value changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d301c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d301c-105">Syntax</span></span>

<span data-ttu-id="d301c-106">GETVAL(\*\* *cellname* \*\* )</span><span class="sxs-lookup"><span data-stu-id="d301c-106">GETVAL(\*\* *cellname* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d301c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d301c-107">Parameters</span></span>

|<span data-ttu-id="d301c-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="d301c-108">**Name**</span></span>|<span data-ttu-id="d301c-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="d301c-109">**Required/Optional**</span></span>|<span data-ttu-id="d301c-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="d301c-110">**Data Type**</span></span>|<span data-ttu-id="d301c-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d301c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d301c-112">_cellname_</span><span class="sxs-lookup"><span data-stu-id="d301c-112">_cellname_</span></span> <br/> |<span data-ttu-id="d301c-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="d301c-113">Required</span></span>  <br/> |<span data-ttu-id="d301c-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="d301c-114">**String**</span></span> <br/> |<span data-ttu-id="d301c-115">Имя ячейки, для которого необходимо получить значение.</span><span class="sxs-lookup"><span data-stu-id="d301c-115">The name of the cell to get the value of.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="d301c-116">Пример</span><span class="sxs-lookup"><span data-stu-id="d301c-116">Example</span></span>

<span data-ttu-id="d301c-117">GETVAL(PinX) + GETVAL(PinY) + Width</span><span class="sxs-lookup"><span data-stu-id="d301c-117">GETVAL(PinX) + GETVAL(PinY) + Width</span></span> 
  
<span data-ttu-id="d301c-118">Возвращает сумму значений ячеек PinX, PinY и Width.</span><span class="sxs-lookup"><span data-stu-id="d301c-118">Returns the sum of the value of the PinX, PinY, and Width cells.</span></span> 
  

