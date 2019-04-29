---
title: Checked Cell (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm155
localization_priority: Normal
ms.assetid: 50937e29-eaa1-0cd0-53cc-dc17e7793e55
description: Указывает, отмечен ли элемент в контекстном меню или меню тегов действий.
ms.openlocfilehash: 870823f28d802e7cafa81efbe5617f27b6714885
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438332"
---
# <a name="checked-cell-actions-section"></a><span data-ttu-id="f71e4-103">Checked Cell (Actions Section)</span><span class="sxs-lookup"><span data-stu-id="f71e4-103">Checked Cell (Actions Section)</span></span>

<span data-ttu-id="f71e4-104">Указывает, отмечен ли элемент в контекстном меню или меню тегов действий.</span><span class="sxs-lookup"><span data-stu-id="f71e4-104">Indicates whether an item is checked on the shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f71e4-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="f71e4-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="f71e4-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="f71e4-106">**Value**</span></span>|<span data-ttu-id="f71e4-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f71e4-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f71e4-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="f71e4-108">TRUE</span></span>  <br/> |<span data-ttu-id="f71e4-109">Отображается галочка.</span><span class="sxs-lookup"><span data-stu-id="f71e4-109">Check mark is displayed.</span></span>  <br/> |
|<span data-ttu-id="f71e4-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="f71e4-110">FALSE</span></span>  <br/> |<span data-ttu-id="f71e4-111">Галочка не отображается (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="f71e4-111">Check mark is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f71e4-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="f71e4-112">Remarks</span></span>

<span data-ttu-id="f71e4-113">Чтобы получить ссылку на возвращенную ячейку по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="f71e4-113">To get a reference to the Checked cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f71e4-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="f71e4-114">Cell name:</span></span>  <br/> |<span data-ttu-id="f71e4-115">Действия.</span><span class="sxs-lookup"><span data-stu-id="f71e4-115">Actions.</span></span> <span data-ttu-id="f71e4-116">*Name (имя* ). Отмеченные действия.</span><span class="sxs-lookup"><span data-stu-id="f71e4-116">*name*  .Checked           where Actions.</span></span> <span data-ttu-id="f71e4-117">*Name* — имя строки действий</span><span class="sxs-lookup"><span data-stu-id="f71e4-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="f71e4-118">Чтобы получить ссылку на отмеченную ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="f71e4-118">To get a reference to the Checked cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f71e4-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f71e4-119">Section index:</span></span>  <br/> |<span data-ttu-id="f71e4-120">**Виссектионактион**</span><span class="sxs-lookup"><span data-stu-id="f71e4-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="f71e4-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f71e4-121">Row index:</span></span>  <br/> |<span data-ttu-id="f71e4-122">**висровактион** +  *i* , где *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="f71e4-122">**visRowAction** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="f71e4-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f71e4-123">Cell index:</span></span>  <br/> |<span data-ttu-id="f71e4-124">**Висактиончеккед**</span><span class="sxs-lookup"><span data-stu-id="f71e4-124">**visActionChecked**</span></span> <br/> |
   

