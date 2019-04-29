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
description: Указывает, содержит ли указанная ячейка локальную формулу.
ms.openlocfilehash: bd0a5dafecf1bd8dca1567392d880ecaaa3e0374
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433292"
---
# <a name="localformulaexists-function"></a><span data-ttu-id="06382-103">Функция LOCALFORMULAEXISTS</span><span class="sxs-lookup"><span data-stu-id="06382-103">LOCALFORMULAEXISTS Function</span></span>

<span data-ttu-id="06382-104">Указывает, содержит ли указанная ячейка локальную формулу.</span><span class="sxs-lookup"><span data-stu-id="06382-104">Indicates whether the referenced cell contains a local formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="06382-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06382-105">Syntax</span></span>

<span data-ttu-id="06382-106">LOCALFORMULAEXISTS (\* \* *целлреф* \* \*)</span><span class="sxs-lookup"><span data-stu-id="06382-106">LOCALFORMULAEXISTS (\*\* *cellref* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="06382-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="06382-107">Parameters</span></span>

|<span data-ttu-id="06382-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="06382-108">**Name**</span></span>|<span data-ttu-id="06382-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="06382-109">**Required/Optional**</span></span>|<span data-ttu-id="06382-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="06382-110">**Data Type**</span></span>|<span data-ttu-id="06382-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="06382-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="06382-112">_целлреф_</span><span class="sxs-lookup"><span data-stu-id="06382-112">_cellref_</span></span> <br/> |<span data-ttu-id="06382-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="06382-113">Required</span></span>  <br/> |<span data-ttu-id="06382-114">**String**</span><span class="sxs-lookup"><span data-stu-id="06382-114">**String**</span></span> <br/> | <span data-ttu-id="06382-115">Ячейка, для которой необходимо проверить наличие формулы.</span><span class="sxs-lookup"><span data-stu-id="06382-115">The cell that you want to check for the presence of a formula.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="06382-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06382-116">Return value</span></span>

<span data-ttu-id="06382-117">Boolean</span><span class="sxs-lookup"><span data-stu-id="06382-117">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="06382-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="06382-118">Remarks</span></span>

<span data-ttu-id="06382-119">Функция LOCALFORMULAEXISTS возвращает 1, если ячейка содержит локальную формулу; Если формула отсутствует или формула унаследована, возвращается 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="06382-119">The LOCALFORMULAEXISTS function returns 1 if the cell contains a local formula; if there is no formula, or if the formula is inherited, it returns 0 (zero).</span></span> 
  

