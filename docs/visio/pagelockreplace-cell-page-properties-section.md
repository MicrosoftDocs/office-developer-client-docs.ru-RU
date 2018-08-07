---
title: Ячейка PageLockReplace (раздел "Свойства страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Указывает, будет ли кнопку Заменить фигуру запрещено на этой странице.
ms.openlocfilehash: b3956b3e2f2fcd5c4f82089e08a6e32200374778
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814341"
---
# <a name="pagelockreplace-cell-page-properties-section"></a><span data-ttu-id="9f029-103">Ячейка PageLockReplace (раздел "Свойства страницы")</span><span class="sxs-lookup"><span data-stu-id="9f029-103">PageLockReplace Cell (Page Properties Section)</span></span>

<span data-ttu-id="9f029-104">Указывает, будет ли кнопку **Заменить фигуру** запрещено на этой странице.</span><span class="sxs-lookup"><span data-stu-id="9f029-104">Indicates whether the **Replace Shape** button should be disabled for this page.</span></span> 
  
|<span data-ttu-id="9f029-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="9f029-105">**Value**</span></span>|<span data-ttu-id="9f029-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9f029-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9f029-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="9f029-107">TRUE</span></span>  <br/> |<span data-ttu-id="9f029-108">Кнопка **Изменить фигуру** недоступна при активной на этой странице.</span><span class="sxs-lookup"><span data-stu-id="9f029-108">The **Change Shape** button is grayed out when this page is active.</span></span>  <br/> |
|<span data-ttu-id="9f029-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9f029-109">FALSE</span></span>  <br/> |<span data-ttu-id="9f029-110">Кнопка **Изменить фигуру** по на этой странице не отключен.</span><span class="sxs-lookup"><span data-stu-id="9f029-110">The **Change Shape** button is not disabled by this page.</span></span> <span data-ttu-id="9f029-111">Кнопки по-прежнему могут быть недоступны if: **DocLockReplace** на **DocumentSheet** задано значение **TRUE**; Ячейка **LockReplace** для выбранной фигуры присвоено **значение TRUE**.</span><span class="sxs-lookup"><span data-stu-id="9f029-111">The button may still be grayed out if: the **DocLockReplace** on the **DocumentSheet** is set to **TRUE**; the **LockReplace** cell for the selected shape is set to **TRUE**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9f029-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="9f029-112">Remarks</span></span>

<span data-ttu-id="9f029-113">Для получения ссылки на ячейки **PageLockReplace** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="9f029-113">To get a reference to the **PageLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9f029-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="9f029-114">Cell name:</span></span>  <br/> | <span data-ttu-id="9f029-115">PageLockReplace</span><span class="sxs-lookup"><span data-stu-id="9f029-115">PageLockReplace</span></span>  <br/> |
   
<span data-ttu-id="9f029-116">Для получения ссылки на ячейки **PageLockReplace** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="9f029-116">To get a reference to the **PageLockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9f029-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="9f029-117">Section index:</span></span>  <br/> |<span data-ttu-id="9f029-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9f029-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9f029-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="9f029-119">Row index:</span></span>  <br/> |<span data-ttu-id="9f029-120">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="9f029-120">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="9f029-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="9f029-121">Cell index:</span></span>  <br/> |<span data-ttu-id="9f029-122">**visPageLockReplace**</span><span class="sxs-lookup"><span data-stu-id="9f029-122">**visPageLockReplace**</span></span> <br/> |
   

