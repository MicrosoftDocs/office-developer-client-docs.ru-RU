---
title: Ячейка DocLockDuplicatePage (раздел "Свойства документа")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Определяет ли страниц в документе может быть реализовано, типа Boolean.
ms.openlocfilehash: 97bca23a7dc9150f66eb0c87834fca72c215448b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813624"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a><span data-ttu-id="65973-103">Ячейка DocLockDuplicatePage (раздел "Свойства документа")</span><span class="sxs-lookup"><span data-stu-id="65973-103">DocLockDuplicatePage Cell (Document Properties Section)</span></span>

<span data-ttu-id="65973-104">Определяет ли страниц в документе может быть реализовано, типа Boolean.</span><span class="sxs-lookup"><span data-stu-id="65973-104">Determines whether pages in the document can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="65973-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="65973-105">TRUE</span></span>  <br/> |<span data-ttu-id="65973-106">**Дублируется** в контекстное меню страницы и метод автоматизации **Page.Duplicate** оба отключены.</span><span class="sxs-lookup"><span data-stu-id="65973-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled.</span></span>  <br/> |
|<span data-ttu-id="65973-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="65973-107">FALSE</span></span>  <br/> |<span data-ttu-id="65973-108">Страница может быть реализовано.</span><span class="sxs-lookup"><span data-stu-id="65973-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="65973-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="65973-109">Remarks</span></span>

<span data-ttu-id="65973-110">Для получения ссылки на ячейки **DocLockDuplicatePage** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="65973-110">To get a reference to the **DocLockDuplicatePage** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="65973-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="65973-111">Cell name:</span></span>  <br/> | <span data-ttu-id="65973-112">DocLockDuplicatePage</span><span class="sxs-lookup"><span data-stu-id="65973-112">DocLockDuplicatePage</span></span>  <br/> |
   
<span data-ttu-id="65973-113">Для получения ссылки на ячейки **DocLockDuplicatePage** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="65973-113">To get a reference to the **DocLockDuplicatePage** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="65973-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="65973-114">Section index:</span></span>  <br/> |<span data-ttu-id="65973-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="65973-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="65973-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="65973-116">Row index:</span></span>  <br/> |<span data-ttu-id="65973-117">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="65973-117">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="65973-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="65973-118">Cell index:</span></span>  <br/> |<span data-ttu-id="65973-119">**visDocLockDuplicatePage**</span><span class="sxs-lookup"><span data-stu-id="65973-119">**visDocLockDuplicatePage**</span></span> <br/> |
   

