---
title: Ячейка PageLockDuplicate (раздел "Свойства страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Определяет, будет ли страница может быть реализовано, как логическое значение.
ms.openlocfilehash: 6cfe8f7a33942f51130ef103b8aba70a5c38b37d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814335"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a><span data-ttu-id="2d173-103">Ячейка PageLockDuplicate (раздел "Свойства страницы")</span><span class="sxs-lookup"><span data-stu-id="2d173-103">PageLockDuplicate Cell (Page Properties Section)</span></span>

<span data-ttu-id="2d173-104">Определяет, будет ли страница может быть реализовано, как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="2d173-104">Determines whether the page can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2d173-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="2d173-105">TRUE</span></span>  <br/> |<span data-ttu-id="2d173-106">**Дублируется** в контекстное меню страницы и метод автоматизации **Page.Duplicate** оба отключены для страницы.</span><span class="sxs-lookup"><span data-stu-id="2d173-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled for the page.</span></span>  <br/> |
|<span data-ttu-id="2d173-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="2d173-107">FALSE</span></span>  <br/> |<span data-ttu-id="2d173-108">Страница может быть реализовано.</span><span class="sxs-lookup"><span data-stu-id="2d173-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d173-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="2d173-109">Remarks</span></span>

<span data-ttu-id="2d173-110">Для получения ссылки на ячейки **PageLockDuplicate** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="2d173-110">To get a reference to the **PageLockDuplicate** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2d173-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="2d173-111">Cell name:</span></span>  <br/> | <span data-ttu-id="2d173-112">PageLockDuplicate</span><span class="sxs-lookup"><span data-stu-id="2d173-112">PageLockDuplicate</span></span>  <br/> |
   
<span data-ttu-id="2d173-113">Для получения ссылки на ячейки **PageLockDuplicate** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="2d173-113">To get a reference to the **PageLockDuplicate** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2d173-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="2d173-114">Section index:</span></span>  <br/> |<span data-ttu-id="2d173-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2d173-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2d173-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="2d173-116">Row index:</span></span>  <br/> |<span data-ttu-id="2d173-117">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="2d173-117">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="2d173-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="2d173-118">Cell index:</span></span>  <br/> |<span data-ttu-id="2d173-119">**visPageLockDuplicate**</span><span class="sxs-lookup"><span data-stu-id="2d173-119">**visPageLockDuplicate**</span></span> <br/> |
   

