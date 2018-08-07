---
title: Ячейка LockDelete (раздел "Защита")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251219
localization_priority: Normal
ms.assetid: 596c62b7-8d42-1854-d709-592db09a6a84
description: Блокирует фигуру таким образом, чтобы он не может быть удален.
ms.openlocfilehash: 00229dcabf45d2a3435039ffe05fd7eb4de75808
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814128"
---
# <a name="lockdelete-cell-protection-section"></a><span data-ttu-id="de705-103">Ячейка LockDelete (раздел "Защита")</span><span class="sxs-lookup"><span data-stu-id="de705-103">LockDelete Cell (Protection Section)</span></span>

<span data-ttu-id="de705-104">Блокирует фигуру таким образом, чтобы он не может быть удален.</span><span class="sxs-lookup"><span data-stu-id="de705-104">Locks the shape so that it cannot be deleted.</span></span>
  
|<span data-ttu-id="de705-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="de705-105">**Value**</span></span>|<span data-ttu-id="de705-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="de705-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="de705-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="de705-107">TRUE</span></span>  <br/> | <span data-ttu-id="de705-108">Фигура не может быть удалена</span><span class="sxs-lookup"><span data-stu-id="de705-108">Shape cannot be deleted</span></span>  <br/> |
| <span data-ttu-id="de705-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="de705-109">FALSE</span></span>  <br/> | <span data-ttu-id="de705-110">Фигура может быть удалена.</span><span class="sxs-lookup"><span data-stu-id="de705-110">Shape can be deleted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de705-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="de705-111">Remarks</span></span>

<span data-ttu-id="de705-112">Чтобы получить ссылку на ячейку LockDelete по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="de705-112">To get a reference to the LockDelete cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="de705-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="de705-113">Cell name:</span></span>  <br/> | <span data-ttu-id="de705-114">LockDelete</span><span class="sxs-lookup"><span data-stu-id="de705-114">LockDelete</span></span>  <br/> |
   
<span data-ttu-id="de705-115">Для получения ссылки на ячейки LockDelete по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="de705-115">To get a reference to the LockDelete cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="de705-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="de705-116">Section index:</span></span>  <br/> |<span data-ttu-id="de705-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="de705-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="de705-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="de705-118">Row index:</span></span>  <br/> |<span data-ttu-id="de705-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="de705-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="de705-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="de705-120">Cell index:</span></span>  <br/> |<span data-ttu-id="de705-121">**visLockDelete**</span><span class="sxs-lookup"><span data-stu-id="de705-121">**visLockDelete**</span></span> <br/> |
   

