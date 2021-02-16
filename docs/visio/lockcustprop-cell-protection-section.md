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
description: Определяет, может ли пользователь добавлять, удалять или изменять данные фигур в пользовательском интерфейсе с помощью диалоговых окон "Определение данных фигуры" или ярлыка для окна "Данные фигуры".
ms.openlocfilehash: 001123f3bd08d35f6f8e4874e20f2ee073835494
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422525"
---
# <a name="lockcustprop-cell-protection-section"></a><span data-ttu-id="c0c44-103">LockCustProp Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="c0c44-103">LockCustProp Cell (Protection Section)</span></span>

<span data-ttu-id="c0c44-104">Определяет, может ли пользователь добавлять, удалять или изменять данные фигур в пользовательском  интерфейсе с помощью диалоговых окон "Определение данных фигуры" или ярлыка для окна **"Данные** фигуры".</span><span class="sxs-lookup"><span data-stu-id="c0c44-104">Determines whether the user can add, delete, or modify shape data in the user interface (UI) by using the **Define Shape Data** dialog box or the shortcut menu for the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="c0c44-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c0c44-105">**Value**</span></span>|<span data-ttu-id="c0c44-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c0c44-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c0c44-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c0c44-107">TRUE</span></span>  <br/> |<span data-ttu-id="c0c44-108">Команда **"Определение данных фигуры"** в ярлыковом меню в окне **"Данные** фигуры" отключена.</span><span class="sxs-lookup"><span data-stu-id="c0c44-108">The **Define Shape Data** command on the shortcut menu in the **Shape Data** window is disabled.</span></span>  <br/> |
|<span data-ttu-id="c0c44-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c0c44-109">FALSE</span></span>  <br/> |<span data-ttu-id="c0c44-110">Команда **"Определение данных фигуры"** в ярлыковом меню в окне **"Данные** фигуры" включена (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="c0c44-110">The **Define Shape Data** command on the shortcut menu in the **Shape Data** window is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0c44-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="c0c44-111">Remarks</span></span>

<span data-ttu-id="c0c44-112">Значение TRUE не мешает пользователю изменять значение элемента данных фигуры или раздел "Данные фигуры" в окне Таблицы фигур.</span><span class="sxs-lookup"><span data-stu-id="c0c44-112">A value of TRUE does not prevent a user from changing the value of a shape data item or changing the Shape Data section in the ShapeSheet window.</span></span> 
  
<span data-ttu-id="c0c44-113">Чтобы получить ссылку на ячейку LockCustProp по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="c0c44-113">To get a reference to the LockCustProp cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c0c44-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="c0c44-114">Cell name:</span></span>  <br/> |<span data-ttu-id="c0c44-115">LockCustProp</span><span class="sxs-lookup"><span data-stu-id="c0c44-115">LockCustProp</span></span>  <br/> |
   
<span data-ttu-id="c0c44-116">Чтобы получить ссылку на ячейку LockCustProp по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="c0c44-116">To get a reference to the LockCustProp cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c0c44-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c0c44-117">Section index:</span></span>  <br/> |<span data-ttu-id="c0c44-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c0c44-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c0c44-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c0c44-119">Row index:</span></span>  <br/> |<span data-ttu-id="c0c44-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="c0c44-120">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="c0c44-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c0c44-121">Cell index:</span></span>  <br/> |<span data-ttu-id="c0c44-122">**visLockCustProp**</span><span class="sxs-lookup"><span data-stu-id="c0c44-122">**visLockCustProp**</span></span> <br/> |
   

