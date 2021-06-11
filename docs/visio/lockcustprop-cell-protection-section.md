---
title: LockCustProp Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60055
localization_priority: Normal
ms.assetid: d1c23f1d-485d-a897-594d-15d6e8d0fb3c
description: Определяет, может ли пользователь добавлять, удалять или изменять данные фигуры в пользовательском интерфейсе (пользовательском интерфейсе) с помощью диалогового окна Define Shape Data или меню ярлыка для окна Данных формы.
ms.openlocfilehash: 001123f3bd08d35f6f8e4874e20f2ee073835494
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422525"
---
# <a name="lockcustprop-cell-protection-section"></a><span data-ttu-id="10601-103">LockCustProp Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="10601-103">LockCustProp Cell (Protection Section)</span></span>

<span data-ttu-id="10601-104">Определяет, может ли пользователь добавлять, удалять или изменять данные фигуры в пользовательском интерфейсе (пользовательском интерфейсе) с помощью диалогового окна **Define Shape Data** или меню ярлыка для окна Данных **формы.**</span><span class="sxs-lookup"><span data-stu-id="10601-104">Determines whether the user can add, delete, or modify shape data in the user interface (UI) by using the **Define Shape Data** dialog box or the shortcut menu for the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="10601-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="10601-105">**Value**</span></span>|<span data-ttu-id="10601-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="10601-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="10601-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="10601-107">TRUE</span></span>  <br/> |<span data-ttu-id="10601-108">Отключена команда **Define Shape Data** в меню ярлыков в окне Shape **Data.**</span><span class="sxs-lookup"><span data-stu-id="10601-108">The **Define Shape Data** command on the shortcut menu in the **Shape Data** window is disabled.</span></span>  <br/> |
|<span data-ttu-id="10601-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="10601-109">FALSE</span></span>  <br/> |<span data-ttu-id="10601-110">Включена **команда Define Shape Data** в меню ярлыка в окне Shape **Data** (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="10601-110">The **Define Shape Data** command on the shortcut menu in the **Shape Data** window is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10601-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="10601-111">Remarks</span></span>

<span data-ttu-id="10601-112">Значение TRUE не мешает пользователю изменять значение элемента данных фигуры или изменять раздел Shape Data в окне ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="10601-112">A value of TRUE does not prevent a user from changing the value of a shape data item or changing the Shape Data section in the ShapeSheet window.</span></span> 
  
<span data-ttu-id="10601-113">Чтобы получить ссылку на ячейку LockCustProp по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="10601-113">To get a reference to the LockCustProp cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="10601-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="10601-114">Cell name:</span></span>  <br/> |<span data-ttu-id="10601-115">LockCustProp</span><span class="sxs-lookup"><span data-stu-id="10601-115">LockCustProp</span></span>  <br/> |
   
<span data-ttu-id="10601-116">Чтобы получить ссылку на ячейку LockCustProp по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="10601-116">To get a reference to the LockCustProp cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="10601-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="10601-117">Section index:</span></span>  <br/> |<span data-ttu-id="10601-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="10601-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="10601-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="10601-119">Row index:</span></span>  <br/> |<span data-ttu-id="10601-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="10601-120">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="10601-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="10601-121">Cell index:</span></span>  <br/> |<span data-ttu-id="10601-122">**visLockCustProp**</span><span class="sxs-lookup"><span data-stu-id="10601-122">**visLockCustProp**</span></span> <br/> |
   

