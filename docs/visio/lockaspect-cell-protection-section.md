---
title: Ячейка LockAspect (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251218
localization_priority: Normal
ms.assetid: e9bfced5-af29-f86c-8604-44ec9a573229
description: Блокирует пропорции фигуры, форму можно изменять только пропорционально. не может иметь размер одного измерения.
ms.openlocfilehash: fb5736add65f548f06697077bc539ec7fac5feb2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814124"
---
# <a name="lockaspect-cell-protection-section"></a><span data-ttu-id="61115-103">Ячейка LockAspect (раздел "Защита")</span><span class="sxs-lookup"><span data-stu-id="61115-103">LockAspect Cell (Protection Section)</span></span>

<span data-ttu-id="61115-104">Блокирует пропорции фигуры, форму можно изменять только пропорционально. не может иметь размер одного измерения.</span><span class="sxs-lookup"><span data-stu-id="61115-104">Locks the aspect ratio of the shape so that the shape can only be sized proportionally; it cannot be sized in a single dimension.</span></span>
  
|<span data-ttu-id="61115-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="61115-105">**Value**</span></span>|<span data-ttu-id="61115-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="61115-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="61115-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="61115-107">TRUE</span></span>  <br/> | <span data-ttu-id="61115-108">Заблокированный пропорции.</span><span class="sxs-lookup"><span data-stu-id="61115-108">Aspect ratio is locked.</span></span>  <br/> |
| <span data-ttu-id="61115-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="61115-109">FALSE</span></span>  <br/> | <span data-ttu-id="61115-110">Отношение сторон не блокируется.</span><span class="sxs-lookup"><span data-stu-id="61115-110">Aspect ratio is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61115-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="61115-111">Remarks</span></span>

<span data-ttu-id="61115-112">Чтобы получить ссылку на ячейку LockAspect по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="61115-112">To get a reference to the LockAspect cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="61115-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="61115-113">Cell name:</span></span>  <br/> | <span data-ttu-id="61115-114">LockAspect</span><span class="sxs-lookup"><span data-stu-id="61115-114">LockAspect</span></span>  <br/> |
   
<span data-ttu-id="61115-115">Для получения ссылки на ячейки LockAspect по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="61115-115">To get a reference to the LockAspect cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="61115-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="61115-116">Section index:</span></span>  <br/> |<span data-ttu-id="61115-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="61115-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="61115-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="61115-118">Row index:</span></span>  <br/> |<span data-ttu-id="61115-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="61115-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="61115-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="61115-120">Cell index:</span></span>  <br/> |<span data-ttu-id="61115-121">**visLockAspect**</span><span class="sxs-lookup"><span data-stu-id="61115-121">**visLockAspect**</span></span> <br/> |
   

