---
title: Функция NEARESTPOINTONPATH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Возвращает процент расстояния по пути точки, который является ближайшим по указанным координатам как в диапазоне от 0 до 1.
ms.openlocfilehash: d9e9b890033526fec99f04cee30ae93578487652
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814289"
---
# <a name="nearestpointonpath-function"></a><span data-ttu-id="7a52a-103">Функция NEARESTPOINTONPATH</span><span class="sxs-lookup"><span data-stu-id="7a52a-103">NEARESTPOINTONPATH Function</span></span>

<span data-ttu-id="7a52a-104">Возвращает процент расстояния по пути точки, который является ближайшим по указанным координатам как в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="7a52a-104">Returns the percentage of the distance along the path of the point that is nearest to the specified coordinates, as a value between 0 and 1.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="7a52a-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="7a52a-105">Version Information</span></span>

<span data-ttu-id="7a52a-106">Добавлена версия: Visio 2010</span><span class="sxs-lookup"><span data-stu-id="7a52a-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7a52a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a52a-107">Syntax</span></span>

<span data-ttu-id="7a52a-108">NEARESTPOINTONPATH (** *раздел* **, ** *x* **, ** *y* **)</span><span class="sxs-lookup"><span data-stu-id="7a52a-108">NEARESTPOINTONPATH(** *section* **, ** *x* **, ** *y* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7a52a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a52a-109">Parameters</span></span>

|<span data-ttu-id="7a52a-110">**Имя**</span><span class="sxs-lookup"><span data-stu-id="7a52a-110">**Name**</span></span>|<span data-ttu-id="7a52a-111">**Обязательный или необязательный**</span><span class="sxs-lookup"><span data-stu-id="7a52a-111">**Required/Optional**</span></span>|<span data-ttu-id="7a52a-112">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="7a52a-112">**Data Type**</span></span>|<span data-ttu-id="7a52a-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7a52a-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7a52a-114">_section_</span><span class="sxs-lookup"><span data-stu-id="7a52a-114">_section_</span></span> <br/> |<span data-ttu-id="7a52a-115">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7a52a-115">Required</span></span>  <br/> |<span data-ttu-id="7a52a-116">**Строка**</span><span class="sxs-lookup"><span data-stu-id="7a52a-116">**String**</span></span> <br/> |<span data-ttu-id="7a52a-117">Раздел геометрии, представляющий путь, указанный с помощью ссылки на его ячейку Path (например, Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="7a52a-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="7a52a-118">_x_</span><span class="sxs-lookup"><span data-stu-id="7a52a-118">_x_</span></span> <br/> |<span data-ttu-id="7a52a-119">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7a52a-119">Required</span></span>  <br/> |<span data-ttu-id="7a52a-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="7a52a-120">**Double**</span></span> <br/> |<span data-ttu-id="7a52a-121">_X_-координата указанный момент.</span><span class="sxs-lookup"><span data-stu-id="7a52a-121">The  _x_-coordinate of the specified point.</span></span>  <br/> |
| <span data-ttu-id="7a52a-122">_y_</span><span class="sxs-lookup"><span data-stu-id="7a52a-122">_y_</span></span> <br/> |<span data-ttu-id="7a52a-123">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7a52a-123">Required</span></span>  <br/> |<span data-ttu-id="7a52a-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="7a52a-124">**Double**</span></span> <br/> |<span data-ttu-id="7a52a-125">_Y_-координата указанный момент.</span><span class="sxs-lookup"><span data-stu-id="7a52a-125">The  _y_-coordinate of the specified point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="7a52a-126">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="7a52a-126">Return value</span></span>

 <span data-ttu-id="7a52a-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="7a52a-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7a52a-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="7a52a-128">Remarks</span></span>

<span data-ttu-id="7a52a-129">Если _раздел_ не существует, Microsoft Visio возвращает #REF!.</span><span class="sxs-lookup"><span data-stu-id="7a52a-129">If  _section_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

