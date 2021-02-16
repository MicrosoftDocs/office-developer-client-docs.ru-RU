---
title: Функция CALLOUTTARGETREF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67cfd32-5911-d8e9-dd51-fd4885dd2b0d
description: Возвращает ссылку на лист целевой фигуры фигуры вызовите.
ms.openlocfilehash: aeeb919fb2efc175d8e5ce23f464503c13331249
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423015"
---
# <a name="callouttargetref-function"></a><span data-ttu-id="6323c-103">Функция CALLOUTTARGETREF</span><span class="sxs-lookup"><span data-stu-id="6323c-103">CALLOUTTARGETREF Function</span></span>

<span data-ttu-id="6323c-104">Возвращает ссылку на лист целевой фигуры фигуры вызовите.</span><span class="sxs-lookup"><span data-stu-id="6323c-104">Returns a sheet reference to the target shape of the callout shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="6323c-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="6323c-105">Version Information</span></span>

<span data-ttu-id="6323c-106">Добавлена версия: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="6323c-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6323c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6323c-107">Syntax</span></span>

<span data-ttu-id="6323c-108">CALLOUTTARGETREF()!</span><span class="sxs-lookup"><span data-stu-id="6323c-108">CALLOUTTARGETREF()!</span></span>
  
### <a name="return-value"></a><span data-ttu-id="6323c-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6323c-109">Return value</span></span>

<span data-ttu-id="6323c-110">Справка по shapeSheet</span><span class="sxs-lookup"><span data-stu-id="6323c-110">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6323c-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="6323c-111">Remarks</span></span>

<span data-ttu-id="6323c-112">Если фигура не является фигурой вызовите или не связана с целевой фигурой, CALLOUTTARGETREF возвращает #REF.</span><span class="sxs-lookup"><span data-stu-id="6323c-112">If the shape is not a callout shape, or if it is not associated with a target shape, CALLOUTTARGETREF returns #REF.</span></span>
  
## <a name="example"></a><span data-ttu-id="6323c-113">Пример</span><span class="sxs-lookup"><span data-stu-id="6323c-113">Example</span></span>

<span data-ttu-id="6323c-114">CALLOUTTARGETREF()! Height</span><span class="sxs-lookup"><span data-stu-id="6323c-114">CALLOUTTARGETREF()!Height</span></span> 
  
<span data-ttu-id="6323c-115">Возвращает значение в ячейке Height фигуры, связанной с вызовом.</span><span class="sxs-lookup"><span data-stu-id="6323c-115">Returns the value in the Height cell of the shape that is associated with the callout.</span></span> 
  

