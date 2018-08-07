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
description: Возвращает точки, представленной координаты x и y как одно значение.
ms.openlocfilehash: be00f7d5ae55f70407e35eca43881a6d3f70ec13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814442"
---
# <a name="pnt-function"></a><span data-ttu-id="8caef-103">Функция PNT</span><span class="sxs-lookup"><span data-stu-id="8caef-103">PNT Function</span></span>

<span data-ttu-id="8caef-104">Возвращает точки, представленной координаты _x_ и _y_ как одно значение.</span><span class="sxs-lookup"><span data-stu-id="8caef-104">Returns the point represented by the coordinates  _x_ and  _y_ as a single value.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8caef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8caef-105">Syntax</span></span>

<span data-ttu-id="8caef-106">Раздела PNT (** *x, y* **)</span><span class="sxs-lookup"><span data-stu-id="8caef-106">PNT(** *x,y* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8caef-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8caef-107">Parameters</span></span>

|<span data-ttu-id="8caef-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="8caef-108">**Name**</span></span>|<span data-ttu-id="8caef-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="8caef-109">**Required/Optional**</span></span>|<span data-ttu-id="8caef-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="8caef-110">**Data Type**</span></span>|<span data-ttu-id="8caef-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8caef-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8caef-112">_x, y_</span><span class="sxs-lookup"><span data-stu-id="8caef-112">_x,y_</span></span> <br/> |<span data-ttu-id="8caef-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8caef-113">Required</span></span>  <br/> |<span data-ttu-id="8caef-114">**Номер, номер**</span><span class="sxs-lookup"><span data-stu-id="8caef-114">**Number, Number**</span></span> <br/> |<span data-ttu-id="8caef-115">Координаты точки в системе координат текущей фигуры.</span><span class="sxs-lookup"><span data-stu-id="8caef-115">The coordinates of the point in the coordinate system of the current shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8caef-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6">Return value</span></span>

<span data-ttu-id="8caef-117">Точка</span><span class="sxs-lookup"><span data-stu-id="8caef-117">Point</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8caef-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="8caef-118">Remarks</span></span>

<span data-ttu-id="8caef-119">Преобразование координат в пунктах позволяет изменить Геометрия фигуры без необходимости для работы с *x* - и *y* -координаты отдельно.</span><span class="sxs-lookup"><span data-stu-id="8caef-119">Converting coordinates to points allows you to change a shape's geometry without having to manipulate  *x*  - and  *y*  -coordinates separately.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8caef-120">Пример</span><span class="sxs-lookup"><span data-stu-id="8caef-120">Example</span></span>

<span data-ttu-id="8caef-121">PNT(PinX,PinY)</span><span class="sxs-lookup"><span data-stu-id="8caef-121">PNT(PinX,PinY)</span></span> 
  
<span data-ttu-id="8caef-122">Возвращает точки, представленной PinX и PinY.</span><span class="sxs-lookup"><span data-stu-id="8caef-122">Returns the point represented by PinX and PinY.</span></span> 
  

