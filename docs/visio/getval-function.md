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
description: Получает значение ячейки и не пересчитывает формулу при изменении значения ячейки.
ms.openlocfilehash: b4c8ea14b7184101a360c9f5ee4af03fd178aa6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813849"
---
# <a name="getval-function"></a><span data-ttu-id="ec781-103">Функция GETVAL</span><span class="sxs-lookup"><span data-stu-id="ec781-103">GETVAL Function</span></span>

<span data-ttu-id="ec781-104">Получает значение ячейки и не пересчитывает формулу при изменении значения ячейки.</span><span class="sxs-lookup"><span data-stu-id="ec781-104">Gets the value of a cell and doesn't recalculate the formula when the cell's value changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ec781-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec781-105">Syntax</span></span>

<span data-ttu-id="ec781-106">GETVAL (** *cellname* **)</span><span class="sxs-lookup"><span data-stu-id="ec781-106">GETVAL(** *cellname* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ec781-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec781-107">Parameters</span></span>

|<span data-ttu-id="ec781-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ec781-108">**Name**</span></span>|<span data-ttu-id="ec781-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="ec781-109">**Required/Optional**</span></span>|<span data-ttu-id="ec781-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="ec781-110">**Data Type**</span></span>|<span data-ttu-id="ec781-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ec781-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ec781-112">_cellname_</span><span class="sxs-lookup"><span data-stu-id="ec781-112">_cellname_</span></span> <br/> |<span data-ttu-id="ec781-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ec781-113">Required</span></span>  <br/> |<span data-ttu-id="ec781-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="ec781-114">**String**</span></span> <br/> |<span data-ttu-id="ec781-115">Имя ячейки, чтобы возвратить значение.</span><span class="sxs-lookup"><span data-stu-id="ec781-115">The name of the cell to get the value of.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="ec781-116">Пример</span><span class="sxs-lookup"><span data-stu-id="ec781-116">Example</span></span>

<span data-ttu-id="ec781-117">GETVAL(PinX) + GETVAL(PinY) + ширины</span><span class="sxs-lookup"><span data-stu-id="ec781-117">GETVAL(PinX) + GETVAL(PinY) + Width</span></span> 
  
<span data-ttu-id="ec781-118">Возвращает сумму значение PinX, PinY и ширина ячеек.</span><span class="sxs-lookup"><span data-stu-id="ec781-118">Returns the sum of the value of the PinX, PinY, and Width cells.</span></span> 
  

