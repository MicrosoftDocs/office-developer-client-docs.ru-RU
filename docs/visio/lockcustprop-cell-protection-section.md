---
title: Ячейка LockCustProp (раздел Защита)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60055
localization_priority: Normal
ms.assetid: d1c23f1d-485d-a897-594d-15d6e8d0fb3c
description: Определяет, является ли пользователь добавлять, удалять и изменения данных в пользовательского интерфейса (UI) с помощью диалогового окна Определение данных фигуры или контекстное меню для окна данных фигуры.
ms.openlocfilehash: a88da9e4973f819b398b5bdeda434ede14640797
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814129"
---
# <a name="lockcustprop-cell-protection-section"></a><span data-ttu-id="81d5c-103">Ячейка LockCustProp (раздел Защита)</span><span class="sxs-lookup"><span data-stu-id="81d5c-103">LockCustProp Cell (Protection Section)</span></span>

<span data-ttu-id="81d5c-104">Определяет, является ли пользователь добавлять, удалять и изменения данных в пользовательского интерфейса (UI) с помощью диалогового окна **Определение данных фигуры** или контекстное меню для окна **Данных фигуры** .</span><span class="sxs-lookup"><span data-stu-id="81d5c-104">Determines whether the user can add, delete, or modify shape data in the user interface (UI) by using the **Define Shape Data** dialog box or the shortcut menu for the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="81d5c-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="81d5c-105">**Value**</span></span>|<span data-ttu-id="81d5c-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="81d5c-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="81d5c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="81d5c-107">TRUE</span></span>  <br/> |<span data-ttu-id="81d5c-108">**Определение данных фигуры** команда контекстного меню в окне **Данных фигуры** отключена.</span><span class="sxs-lookup"><span data-stu-id="81d5c-108">The **Define Shape Data** command on the shortcut menu in the **Shape Data** window is disabled.</span></span>  <br/> |
|<span data-ttu-id="81d5c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="81d5c-109">FALSE</span></span>  <br/> |<span data-ttu-id="81d5c-110">**Определение данных фигуры** команда контекстного меню в окне **Данных фигуры** включена (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="81d5c-110">The **Define Shape Data** command on the shortcut menu in the **Shape Data** window is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81d5c-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="81d5c-111">Remarks</span></span>

<span data-ttu-id="81d5c-112">Значение TRUE не позволяют пользователю изменять значение элемента данных фигуры или изменение раздела данных фигуры в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="81d5c-112">A value of TRUE does not prevent a user from changing the value of a shape data item or changing the Shape Data section in the ShapeSheet window.</span></span> 
  
<span data-ttu-id="81d5c-113">Чтобы получить ссылку на ячейку LockCustProp по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="81d5c-113">To get a reference to the LockCustProp cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81d5c-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="81d5c-114">Cell name:</span></span>  <br/> |<span data-ttu-id="81d5c-115">LockCustProp</span><span class="sxs-lookup"><span data-stu-id="81d5c-115">LockCustProp</span></span>  <br/> |
   
<span data-ttu-id="81d5c-116">Для получения ссылки на ячейки LockCustProp по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="81d5c-116">To get a reference to the LockCustProp cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81d5c-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="81d5c-117">Section index:</span></span>  <br/> |<span data-ttu-id="81d5c-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="81d5c-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="81d5c-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="81d5c-119">Row index:</span></span>  <br/> |<span data-ttu-id="81d5c-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="81d5c-120">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="81d5c-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="81d5c-121">Cell index:</span></span>  <br/> |<span data-ttu-id="81d5c-122">**visLockCustProp**</span><span class="sxs-lookup"><span data-stu-id="81d5c-122">**visLockCustProp**</span></span> <br/> |
   

