---
title: Функция CALLOUTTARGETREF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67cfd32-5911-d8e9-dd51-fd4885dd2b0d
description: Возвращает ссылку листа на конечную фигуру выноски фигуры.
ms.openlocfilehash: 1b0cb7c6737a810a0ade65f19afaff7bb4b9f616
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813304"
---
# <a name="callouttargetref-function"></a><span data-ttu-id="a967e-103">Функция CALLOUTTARGETREF</span><span class="sxs-lookup"><span data-stu-id="a967e-103">CALLOUTTARGETREF Function</span></span>

<span data-ttu-id="a967e-104">Возвращает ссылку листа на конечную фигуру выноски фигуры.</span><span class="sxs-lookup"><span data-stu-id="a967e-104">Returns a sheet reference to the target shape of the callout shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="a967e-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="a967e-105">Version Information</span></span>

<span data-ttu-id="a967e-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="a967e-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a967e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a967e-107">Syntax</span></span>

<span data-ttu-id="a967e-108">CALLOUTTARGETREF()!</span><span class="sxs-lookup"><span data-stu-id="a967e-108">CALLOUTTARGETREF()!</span></span>
  
### <a name="return-value"></a><span data-ttu-id="a967e-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9">Return value</span></span>

<span data-ttu-id="a967e-110">Справочник по таблице свойств фигуры</span><span class="sxs-lookup"><span data-stu-id="a967e-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a967e-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="a967e-111">Remarks</span></span>

<span data-ttu-id="a967e-112">Если фигура не является фигурой выноски или не связана с конечную фигуру, CALLOUTTARGETREF возвращает #REF.</span><span class="sxs-lookup"><span data-stu-id="a967e-112">If the shape is not a callout shape, or if it is not associated with a target shape, CALLOUTTARGETREF returns #REF.</span></span>
  
## <a name="example"></a><span data-ttu-id="a967e-113">Пример</span><span class="sxs-lookup"><span data-stu-id="a967e-113">Example</span></span>

<span data-ttu-id="a967e-114">CALLOUTTARGETREF()! Высота</span><span class="sxs-lookup"><span data-stu-id="a967e-114">CALLOUTTARGETREF()!Height</span></span> 
  
<span data-ttu-id="a967e-115">Возвращает значение в ячейке высоту фигуры, связанный с этим вызовом.</span><span class="sxs-lookup"><span data-stu-id="a967e-115">Returns the value in the Height cell of the shape that is associated with the callout.</span></span> 
  

