---
title: Ячейка DocLockReplace (раздел "Свойства документа")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Определяет, отключены ли фигура заменить пользовательского интерфейса для данного документа.
ms.openlocfilehash: 41552ddad4e48680960c45869ded5cf4f80d760f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813648"
---
# <a name="doclockreplace-cell-document-properties-section"></a><span data-ttu-id="b2fee-103">Ячейка DocLockReplace (раздел "Свойства документа")</span><span class="sxs-lookup"><span data-stu-id="b2fee-103">DocLockReplace Cell (Document Properties Section)</span></span>

<span data-ttu-id="b2fee-104">Определяет, отключены ли фигура заменить пользовательского интерфейса для данного документа.</span><span class="sxs-lookup"><span data-stu-id="b2fee-104">Determines whether the replace shape UI should be disabled for this document.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2fee-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="b2fee-105">TRUE</span></span>  <br/> |<span data-ttu-id="b2fee-106">**Замена фигуры** кнопка недоступна в пользовательском Интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="b2fee-106">The **Replace Shape** button is grayed out in the UI.</span></span>  <br/> |
|<span data-ttu-id="b2fee-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="b2fee-107">FALSE</span></span>  <br/> |<span data-ttu-id="b2fee-108">**Замена фигуры** кнопка активна в пользовательском Интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="b2fee-108">The **Replace Shape** button is active in the UI.</span></span> <span data-ttu-id="b2fee-109">Пользователи могут использовать функцию замените фигуры в этом документе.</span><span class="sxs-lookup"><span data-stu-id="b2fee-109">Users can use the Replace Shape feature in this document.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2fee-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="b2fee-110">Remarks</span></span>

<span data-ttu-id="b2fee-111">Для получения ссылки на ячейки **DocLockReplace** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="b2fee-111">To get a reference to the **DocLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b2fee-112">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="b2fee-112">Cell name:</span></span>  <br/> | <span data-ttu-id="b2fee-113">DocLocReplace</span><span class="sxs-lookup"><span data-stu-id="b2fee-113">DocLocReplace</span></span>  <br/> |
   
<span data-ttu-id="b2fee-114">Для получения ссылки на ячейки **DocLocReplace** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="b2fee-114">To get a reference to the **DocLocReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b2fee-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b2fee-115">Section index:</span></span>  <br/> |<span data-ttu-id="b2fee-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b2fee-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b2fee-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b2fee-117">Row index:</span></span>  <br/> |<span data-ttu-id="b2fee-118">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="b2fee-118">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="b2fee-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b2fee-119">Cell index:</span></span>  <br/> |<span data-ttu-id="b2fee-120">** visDocLockReplace **</span><span class="sxs-lookup"><span data-stu-id="b2fee-120">**visDocLockReplace **</span></span> <br/> |
   

