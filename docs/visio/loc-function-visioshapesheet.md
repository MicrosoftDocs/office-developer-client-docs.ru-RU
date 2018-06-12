---
title: Функция LOC (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251455
localization_priority: Normal
ms.assetid: 7db7a8ed-50a9-8495-b978-42a2fddb466a
description: Принимает точку, определенную в локальной системе координат одной фигуры и возвращает эквивалентную точку, выраженную в локальной системе координат фигуры, связанной с формулой.
ms.openlocfilehash: 196e2c92ea6ab410b6ecca9767b68605e4eb4d30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814115"
---
# <a name="loc-function-visioshapesheet"></a><span data-ttu-id="bbce7-103">Функция LOC (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="bbce7-103">LOC Function (VisioShapeSheet)</span></span>

<span data-ttu-id="bbce7-104">Принимает точку, определенную в локальной системе координат одной фигуры и возвращает эквивалентную точку, выраженную в локальной системе координат фигуры, связанной с формулой.</span><span class="sxs-lookup"><span data-stu-id="bbce7-104">Takes a point defined in one shape's local coordinates and returns the equivalent point expressed in the local coordinates of the shape associated with the formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bbce7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bbce7-105">Syntax</span></span>

<span data-ttu-id="bbce7-106">LOC (** *пункт* **)</span><span class="sxs-lookup"><span data-stu-id="bbce7-106">LOC(** *point* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bbce7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bbce7-107">Parameters</span></span>

|<span data-ttu-id="bbce7-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="bbce7-108">**Name**</span></span>|<span data-ttu-id="bbce7-109">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="bbce7-109">**Required/Optional**</span></span>|<span data-ttu-id="bbce7-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="bbce7-110">**Data Type**</span></span>|<span data-ttu-id="bbce7-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bbce7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bbce7-112">_точка_</span><span class="sxs-lookup"><span data-stu-id="bbce7-112">_point_</span></span> <br/> |<span data-ttu-id="bbce7-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bbce7-113">Required</span></span>  <br/> |<span data-ttu-id="bbce7-114">**Строка**</span><span class="sxs-lookup"><span data-stu-id="bbce7-114">**String**</span></span> <br/> | <span data-ttu-id="bbce7-115">Точка, определенные в локальной системе координат одной фигуры.</span><span class="sxs-lookup"><span data-stu-id="bbce7-115">A point defined in one shape's local coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="bbce7-116">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="bbce7-116">Return value</span></span>

<span data-ttu-id="bbce7-117">Строка</span><span class="sxs-lookup"><span data-stu-id="bbce7-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bbce7-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="bbce7-118">Remarks</span></span>

<span data-ttu-id="bbce7-119">Локальные координаты отсчитываются с левого нижнего угла прямоугольник выделения фигуры.</span><span class="sxs-lookup"><span data-stu-id="bbce7-119">Local coordinates are measured from the lower-left corner of the shape's selection rectangle.</span></span> <span data-ttu-id="bbce7-120">Обе фигуры должны располагаться на той же странице.</span><span class="sxs-lookup"><span data-stu-id="bbce7-120">Both shapes must be on the same page.</span></span>
  
## <a name="example"></a><span data-ttu-id="bbce7-121">Пример</span><span class="sxs-lookup"><span data-stu-id="bbce7-121">Example</span></span>

<span data-ttu-id="bbce7-122">LOC (раздела PNT (Sheet.5! LocPinX Sheet.5! LocPinY))</span><span class="sxs-lookup"><span data-stu-id="bbce7-122">LOC(PNT(Sheet.5!LocPinX, Sheet.5!LocPinY))</span></span> 
  
<span data-ttu-id="bbce7-123">В этом выражении раздела PNT преобразует набор локальных координат Sheet.5 точки.</span><span class="sxs-lookup"><span data-stu-id="bbce7-123">In this expression, PNT converts a set of local coordinates in Sheet.5 to a point.</span></span> <span data-ttu-id="bbce7-124">(Sheet.5 является другую фигуру на одной странице документа). Затем LOC преобразует текущего момента эквивалентный точки в текущей форме локальной системе координат, относящиеся к левом нижнем углу прямоугольник выделения текущей фигуры.</span><span class="sxs-lookup"><span data-stu-id="bbce7-124">(Sheet.5 is another shape on the same drawing page.) LOC then converts that point to an equivalent point in the current shape's local coordinate system, relative to the lower-left corner of the selection rectangle of the current shape.</span></span> 
  
<span data-ttu-id="bbce7-125">5 в Sheet.5 — это идентификатор для фигуры, которая отображается в диалоговом окне **Имени фигуры** (вкладки "**Разработчик** ").</span><span class="sxs-lookup"><span data-stu-id="bbce7-125">The 5 in Sheet.5 is the ID number for the shape, which is displayed in the **Shape Name** dialog box (**Developer** tab).</span></span> 
  

