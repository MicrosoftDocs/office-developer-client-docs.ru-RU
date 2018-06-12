---
title: Функция LOCALFORMULAEXISTS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60105
localization_priority: Normal
ms.assetid: 2b757c8d-7732-0f9b-c836-ef755dd1c673
description: Показывает, содержит ли указанная ячейка локальную формулу.
ms.openlocfilehash: 1b749011de8554cb5b777fe92b20a6bcdb2fcb19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814122"
---
# <a name="localformulaexists-function"></a><span data-ttu-id="f5579-103">Функция LOCALFORMULAEXISTS</span><span class="sxs-lookup"><span data-stu-id="f5579-103">LOCALFORMULAEXISTS Function</span></span>

<span data-ttu-id="f5579-104">Показывает, содержит ли указанная ячейка локальную формулу.</span><span class="sxs-lookup"><span data-stu-id="f5579-104">Indicates whether the referenced cell contains a local formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f5579-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5579-105">Syntax</span></span>

<span data-ttu-id="f5579-106">LOCALFORMULAEXISTS (** *cellref* **)</span><span class="sxs-lookup"><span data-stu-id="f5579-106">LOCALFORMULAEXISTS (** *cellref* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f5579-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5579-107">Parameters</span></span>

|<span data-ttu-id="f5579-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="f5579-108">**Name**</span></span>|<span data-ttu-id="f5579-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="f5579-109">**Required/Optional**</span></span>|<span data-ttu-id="f5579-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="f5579-110">**Data Type**</span></span>|<span data-ttu-id="f5579-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f5579-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f5579-112">_cellref_</span><span class="sxs-lookup"><span data-stu-id="f5579-112">_cellref_</span></span> <br/> |<span data-ttu-id="f5579-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f5579-113">Required</span></span>  <br/> |<span data-ttu-id="f5579-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="f5579-114">**String**</span></span> <br/> | <span data-ttu-id="f5579-115">Ячейка, необходимо проверить наличие формулы.</span><span class="sxs-lookup"><span data-stu-id="f5579-115">The cell that you want to check for the presence of a formula.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f5579-116">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="f5579-116">Return value</span></span>

<span data-ttu-id="f5579-117">Логический</span><span class="sxs-lookup"><span data-stu-id="f5579-117">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f5579-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="f5579-118">Remarks</span></span>

<span data-ttu-id="f5579-119">Функция LOCALFORMULAEXISTS возвращает 1, если ячейка с формулой локального; Если нет формулы не или наследуется формулу, возвращает нуль (0).</span><span class="sxs-lookup"><span data-stu-id="f5579-119">The LOCALFORMULAEXISTS function returns 1 if the cell contains a local formula; if there is no formula, or if the formula is inherited, it returns 0 (zero).</span></span> 
  

