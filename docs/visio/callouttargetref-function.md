---
title: Функция CALLOUTTARGETREF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67cfd32-5911-d8e9-dd51-fd4885dd2b0d
description: Возвращает ссылку на лист с конечной формой фигуры выноски.
ms.openlocfilehash: aeeb919fb2efc175d8e5ce23f464503c13331249
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337249"
---
# <a name="callouttargetref-function"></a><span data-ttu-id="a79c9-103">Функция CALLOUTTARGETREF</span><span class="sxs-lookup"><span data-stu-id="a79c9-103">CALLOUTTARGETREF Function</span></span>

<span data-ttu-id="a79c9-104">Возвращает ссылку на лист с конечной формой фигуры выноски.</span><span class="sxs-lookup"><span data-stu-id="a79c9-104">Returns a sheet reference to the target shape of the callout shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="a79c9-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="a79c9-105">Version Information</span></span>

<span data-ttu-id="a79c9-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="a79c9-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a79c9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a79c9-107">Syntax</span></span>

<span data-ttu-id="a79c9-108">CALLOUTTARGETREF ()!</span><span class="sxs-lookup"><span data-stu-id="a79c9-108">CALLOUTTARGETREF()!</span></span>
  
### <a name="return-value"></a><span data-ttu-id="a79c9-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a79c9-109">Return value</span></span>

<span data-ttu-id="a79c9-110">Ссылка на таблицу свойств фигуры</span><span class="sxs-lookup"><span data-stu-id="a79c9-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a79c9-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a79c9-111">Remarks</span></span>

<span data-ttu-id="a79c9-112">Если фигура не является фигурой выноски или не связана с целевой фигурой, CALLOUTTARGETREF возвращает #REF.</span><span class="sxs-lookup"><span data-stu-id="a79c9-112">If the shape is not a callout shape, or if it is not associated with a target shape, CALLOUTTARGETREF returns #REF.</span></span>
  
## <a name="example"></a><span data-ttu-id="a79c9-113">Пример</span><span class="sxs-lookup"><span data-stu-id="a79c9-113">Example</span></span>

<span data-ttu-id="a79c9-114">CALLOUTTARGETREF ()! Полноразмерные</span><span class="sxs-lookup"><span data-stu-id="a79c9-114">CALLOUTTARGETREF()!Height</span></span> 
  
<span data-ttu-id="a79c9-115">Возвращает значение в ячейке Height фигуры, связанной с вызываемым вызываемым вызываемым вызываемым выноски.</span><span class="sxs-lookup"><span data-stu-id="a79c9-115">Returns the value in the Height cell of the shape that is associated with the callout.</span></span> 
  

