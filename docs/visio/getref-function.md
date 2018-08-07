---
title: Функция GETREF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251884
localization_priority: Normal
ms.assetid: 25c9f817-d22b-28c9-1339-dc9f27d0dd41
description: Ссылается на ячейку и не производит повторное вычисление формулы при изменении связанной ячейки.
ms.openlocfilehash: 454314b1f156f560c237f22a45492978ca3c31ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813847"
---
# <a name="getref-function"></a><span data-ttu-id="bc98d-103">Функция GETREF</span><span class="sxs-lookup"><span data-stu-id="bc98d-103">GETREF Function</span></span>

<span data-ttu-id="bc98d-104">Ссылается на ячейку и не производит повторное вычисление формулы при изменении связанной ячейки.</span><span class="sxs-lookup"><span data-stu-id="bc98d-104">References a cell and doesn't recalculate the formula when the referenced cell changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="bc98d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc98d-105">Syntax</span></span>

<span data-ttu-id="bc98d-106">GETREF (** *cellname* **)</span><span class="sxs-lookup"><span data-stu-id="bc98d-106">GETREF(** *cellname* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bc98d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc98d-107">Parameters</span></span>

|<span data-ttu-id="bc98d-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="bc98d-108">**Name**</span></span>|<span data-ttu-id="bc98d-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="bc98d-109">**Required/Optional**</span></span>|<span data-ttu-id="bc98d-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="bc98d-110">**Data Type**</span></span>|<span data-ttu-id="bc98d-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bc98d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bc98d-112">_cellname_</span><span class="sxs-lookup"><span data-stu-id="bc98d-112">_cellname_</span></span> <br/> |<span data-ttu-id="bc98d-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bc98d-113">Required</span></span>  <br/> |<span data-ttu-id="bc98d-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="bc98d-114">**String**</span></span> <br/> |<span data-ttu-id="bc98d-115">Имя для получения ссылки на ячейки.</span><span class="sxs-lookup"><span data-stu-id="bc98d-115">The name of the cell to get a reference to.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="bc98d-116">Пример</span><span class="sxs-lookup"><span data-stu-id="bc98d-116">Example</span></span>

<span data-ttu-id="bc98d-117">SETF(GETREF(PinX),5.1)</span><span class="sxs-lookup"><span data-stu-id="bc98d-117">SETF(GETREF(PinX),5.1)</span></span> 
  
<span data-ttu-id="bc98d-118">Задает формулу в ячейку PinX 5.1.</span><span class="sxs-lookup"><span data-stu-id="bc98d-118">Sets the formula of the PinX cell to 5.1.</span></span> 
  

