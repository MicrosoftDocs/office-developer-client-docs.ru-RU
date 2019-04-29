---
title: Функция PNT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251480
localization_priority: Normal
ms.assetid: d14a735c-0278-922f-7823-79adf6cb1e64
description: Возвращает точку, представленную координатами x и y в виде одного значения.
ms.openlocfilehash: c0a12aa18f4c766ea1f5b0fa1d827804d766713c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435714"
---
# <a name="pnt-function"></a><span data-ttu-id="3c9bd-103">Функция PNT</span><span class="sxs-lookup"><span data-stu-id="3c9bd-103">PNT Function</span></span>

<span data-ttu-id="3c9bd-104">Возвращает точку, представленную координатами _x_ и _y_ в виде одного значения.</span><span class="sxs-lookup"><span data-stu-id="3c9bd-104">Returns the point represented by the coordinates  _x_ and  _y_ as a single value.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3c9bd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c9bd-105">Syntax</span></span>

<span data-ttu-id="3c9bd-106">PNT (\* \* *x, y* \* \*)</span><span class="sxs-lookup"><span data-stu-id="3c9bd-106">PNT(\*\* *x,y* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3c9bd-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c9bd-107">Parameters</span></span>

|<span data-ttu-id="3c9bd-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="3c9bd-108">**Name**</span></span>|<span data-ttu-id="3c9bd-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="3c9bd-109">**Required/Optional**</span></span>|<span data-ttu-id="3c9bd-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="3c9bd-110">**Data Type**</span></span>|<span data-ttu-id="3c9bd-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3c9bd-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3c9bd-112">_x, y_</span><span class="sxs-lookup"><span data-stu-id="3c9bd-112">_x,y_</span></span> <br/> |<span data-ttu-id="3c9bd-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3c9bd-113">Required</span></span>  <br/> |<span data-ttu-id="3c9bd-114">**Число, число**</span><span class="sxs-lookup"><span data-stu-id="3c9bd-114">**Number, Number**</span></span> <br/> |<span data-ttu-id="3c9bd-115">Координаты точки в системе координат текущей фигуры.</span><span class="sxs-lookup"><span data-stu-id="3c9bd-115">The coordinates of the point in the coordinate system of the current shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3c9bd-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c9bd-116">Return value</span></span>

<span data-ttu-id="3c9bd-117">Point</span><span class="sxs-lookup"><span data-stu-id="3c9bd-117">Point</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3c9bd-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="3c9bd-118">Remarks</span></span>

<span data-ttu-id="3c9bd-119">При преобразовании координат в точки можно изменить геометрию фигуры без необходимости управлять координатами *x* и *y* раздельно.</span><span class="sxs-lookup"><span data-stu-id="3c9bd-119">Converting coordinates to points allows you to change a shape's geometry without having to manipulate  *x*  - and  *y*  -coordinates separately.</span></span> 
  
## <a name="example"></a><span data-ttu-id="3c9bd-120">Пример</span><span class="sxs-lookup"><span data-stu-id="3c9bd-120">Example</span></span>

<span data-ttu-id="3c9bd-121">PNT (PinX, PinY)</span><span class="sxs-lookup"><span data-stu-id="3c9bd-121">PNT(PinX,PinY)</span></span> 
  
<span data-ttu-id="3c9bd-122">Возвращает точку, представленную PinX и PinY.</span><span class="sxs-lookup"><span data-stu-id="3c9bd-122">Returns the point represented by PinX and PinY.</span></span> 
  

