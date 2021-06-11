---
title: Функция DEPENDSON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251420
localization_priority: Normal
ms.assetid: 8fcfcfdd-69e2-b061-fdb6-d29389d14403
description: Создает зависимость от ссылок на ячейки.
ms.openlocfilehash: 26e7f5fb0620a5f1812d878f02d5bedd43afe524
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423470"
---
# <a name="dependson-function"></a><span data-ttu-id="5d6ae-103">Функция DEPENDSON</span><span class="sxs-lookup"><span data-stu-id="5d6ae-103">DEPENDSON Function</span></span>

<span data-ttu-id="5d6ae-104">Создает зависимость от ссылок на ячейки.</span><span class="sxs-lookup"><span data-stu-id="5d6ae-104">Creates a cell reference dependency.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5d6ae-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d6ae-105">Syntax</span></span>

<span data-ttu-id="5d6ae-106">DEPENDSON(\*\* *cellref* \*\* [, \*\* *cellref2* \*\*,...])</span><span class="sxs-lookup"><span data-stu-id="5d6ae-106">DEPENDSON(\*\* *cellref* \*\* [, \*\* *cellref2* \*\*,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5d6ae-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d6ae-107">Parameters</span></span>

|<span data-ttu-id="5d6ae-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="5d6ae-108">**Name**</span></span>|<span data-ttu-id="5d6ae-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="5d6ae-109">**Required/Optional**</span></span>|<span data-ttu-id="5d6ae-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="5d6ae-110">**Data Type**</span></span>|<span data-ttu-id="5d6ae-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5d6ae-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5d6ae-112">_cellref_</span><span class="sxs-lookup"><span data-stu-id="5d6ae-112">_cellref_</span></span> <br/> |<span data-ttu-id="5d6ae-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5d6ae-113">Required</span></span>  <br/> |<span data-ttu-id="5d6ae-114">**String**</span><span class="sxs-lookup"><span data-stu-id="5d6ae-114">**String**</span></span> <br/> |<span data-ttu-id="5d6ae-115">Первая ссылка ячейки.</span><span class="sxs-lookup"><span data-stu-id="5d6ae-115">The first cell reference.</span></span>  <br/> |
| <span data-ttu-id="5d6ae-116">_cellref2_</span><span class="sxs-lookup"><span data-stu-id="5d6ae-116">_cellref2_</span></span> <br/> |<span data-ttu-id="5d6ae-117">Необязательный</span><span class="sxs-lookup"><span data-stu-id="5d6ae-117">Optional</span></span>  <br/> |<span data-ttu-id="5d6ae-118">**String**</span><span class="sxs-lookup"><span data-stu-id="5d6ae-118">**String**</span></span> <br/> |<span data-ttu-id="5d6ae-119">Вторая ссылка ячейки.</span><span class="sxs-lookup"><span data-stu-id="5d6ae-119">The second cell reference.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d6ae-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="5d6ae-120">Remarks</span></span>

<span data-ttu-id="5d6ae-121">Эта функция всегда возвращает FALSE.</span><span class="sxs-lookup"><span data-stu-id="5d6ae-121">This function always returns FALSE.</span></span> <span data-ttu-id="5d6ae-122">Это не влияет при его использования в строке Event или ячейке Action.</span><span class="sxs-lookup"><span data-stu-id="5d6ae-122">It has no effect when used in an Event row or an Action cell.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5d6ae-123">Пример</span><span class="sxs-lookup"><span data-stu-id="5d6ae-123">Example</span></span>

<span data-ttu-id="5d6ae-124">OPENTEXTWIN() + DEPENDSON (PinX,PinY)</span><span class="sxs-lookup"><span data-stu-id="5d6ae-124">OPENTEXTWIN() + DEPENDSON(PinX,PinY)</span></span> 
  
<span data-ttu-id="5d6ae-125">Открывает текстовый блок для фигуры всякий раз, когда меняются ячейки PinX или PinY формы.</span><span class="sxs-lookup"><span data-stu-id="5d6ae-125">Opens the text block for a shape whenever the shape's PinX or PinY cells change.</span></span> 
  

