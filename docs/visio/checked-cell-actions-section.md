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
description: Указывает, проверяется ли элемент в меню ярлыка или тега действий.
ms.openlocfilehash: 870823f28d802e7cafa81efbe5617f27b6714885
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438332"
---
# <a name="checked-cell-actions-section"></a><span data-ttu-id="95477-103">Checked Cell (Actions Section)</span><span class="sxs-lookup"><span data-stu-id="95477-103">Checked Cell (Actions Section)</span></span>

<span data-ttu-id="95477-104">Указывает, проверяется ли элемент в меню ярлыка или тега действий.</span><span class="sxs-lookup"><span data-stu-id="95477-104">Indicates whether an item is checked on the shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="95477-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="95477-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="95477-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="95477-106">**Value**</span></span>|<span data-ttu-id="95477-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="95477-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95477-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="95477-108">TRUE</span></span>  <br/> |<span data-ttu-id="95477-109">Отображается контрольный знак.</span><span class="sxs-lookup"><span data-stu-id="95477-109">Check mark is displayed.</span></span>  <br/> |
|<span data-ttu-id="95477-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="95477-110">FALSE</span></span>  <br/> |<span data-ttu-id="95477-111">Контрольный знак не отображается (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="95477-111">Check mark is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95477-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="95477-112">Remarks</span></span>

<span data-ttu-id="95477-113">Чтобы получить ссылку на ячейку Checked по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="95477-113">To get a reference to the Checked cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95477-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="95477-114">Cell name:</span></span>  <br/> |<span data-ttu-id="95477-115">Действия.</span><span class="sxs-lookup"><span data-stu-id="95477-115">Actions.</span></span> <span data-ttu-id="95477-116">*имя*  . Проверено, где действия.</span><span class="sxs-lookup"><span data-stu-id="95477-116">*name*  .Checked           where Actions.</span></span> <span data-ttu-id="95477-117">*имя*  — это имя строки Действия</span><span class="sxs-lookup"><span data-stu-id="95477-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="95477-118">Чтобы получить ссылку на ячейку Checked by index из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="95477-118">To get a reference to the Checked cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95477-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="95477-119">Section index:</span></span>  <br/> |<span data-ttu-id="95477-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="95477-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="95477-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="95477-121">Row index:</span></span>  <br/> |<span data-ttu-id="95477-122">**visRowAction**  +   *i,* *где i* = 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="95477-122">**visRowAction** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="95477-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="95477-123">Cell index:</span></span>  <br/> |<span data-ttu-id="95477-124">**visActionChecked**</span><span class="sxs-lookup"><span data-stu-id="95477-124">**visActionChecked**</span></span> <br/> |
   

