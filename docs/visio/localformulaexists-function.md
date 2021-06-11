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
description: Указывает, содержит ли эталонная ячейка локализованную формулу.
ms.openlocfilehash: bd0a5dafecf1bd8dca1567392d880ecaaa3e0374
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433292"
---
# <a name="localformulaexists-function"></a><span data-ttu-id="37299-103">Функция LOCALFORMULAEXISTS</span><span class="sxs-lookup"><span data-stu-id="37299-103">LOCALFORMULAEXISTS Function</span></span>

<span data-ttu-id="37299-104">Указывает, содержит ли эталонная ячейка локализованную формулу.</span><span class="sxs-lookup"><span data-stu-id="37299-104">Indicates whether the referenced cell contains a local formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="37299-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37299-105">Syntax</span></span>

<span data-ttu-id="37299-106">LOCALFORMULAEXISTS (\*\* *cellref* \*\* )</span><span class="sxs-lookup"><span data-stu-id="37299-106">LOCALFORMULAEXISTS (\*\* *cellref* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="37299-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="37299-107">Parameters</span></span>

|<span data-ttu-id="37299-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="37299-108">**Name**</span></span>|<span data-ttu-id="37299-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="37299-109">**Required/Optional**</span></span>|<span data-ttu-id="37299-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="37299-110">**Data Type**</span></span>|<span data-ttu-id="37299-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="37299-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="37299-112">_cellref_</span><span class="sxs-lookup"><span data-stu-id="37299-112">_cellref_</span></span> <br/> |<span data-ttu-id="37299-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="37299-113">Required</span></span>  <br/> |<span data-ttu-id="37299-114">**String**</span><span class="sxs-lookup"><span data-stu-id="37299-114">**String**</span></span> <br/> | <span data-ttu-id="37299-115">Ячейка, которую необходимо проверить на наличие формулы.</span><span class="sxs-lookup"><span data-stu-id="37299-115">The cell that you want to check for the presence of a formula.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="37299-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="37299-116">Return value</span></span>

<span data-ttu-id="37299-117">Boolean</span><span class="sxs-lookup"><span data-stu-id="37299-117">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="37299-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="37299-118">Remarks</span></span>

<span data-ttu-id="37299-119">Функция LOCALFORMULAEXISTS возвращает 1, если ячейка содержит локализованную формулу; если нет формулы или если формула наследуется, она возвращает 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="37299-119">The LOCALFORMULAEXISTS function returns 1 if the cell contains a local formula; if there is no formula, or if the formula is inherited, it returns 0 (zero).</span></span> 
  

