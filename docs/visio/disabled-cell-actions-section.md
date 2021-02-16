---
title: Disabled Cell (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251337
localization_priority: Normal
ms.assetid: ebf66729-d794-a398-268a-84d761bf06b6
description: Указывает, отключен ли элемент в меню ярлыка или тега действия.
ms.openlocfilehash: ddf55f40056d7df7a2403e500bb4bae335930433
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431353"
---
# <a name="disabled-cell-actions-section"></a><span data-ttu-id="f2b20-103">Disabled Cell (Actions Section)</span><span class="sxs-lookup"><span data-stu-id="f2b20-103">Disabled Cell (Actions Section)</span></span>

<span data-ttu-id="f2b20-104">Указывает, отключен ли элемент в меню ярлыка или тега действия.</span><span class="sxs-lookup"><span data-stu-id="f2b20-104">Indicates whether an item on a shortcut or action tag menu is disabled.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f2b20-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="f2b20-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="f2b20-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="f2b20-106">**Value**</span></span>|<span data-ttu-id="f2b20-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f2b20-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f2b20-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="f2b20-108">TRUE</span></span>  <br/> |<span data-ttu-id="f2b20-109">Отключение (dim) имени команды.</span><span class="sxs-lookup"><span data-stu-id="f2b20-109">Disable (dim) command name.</span></span>  <br/> |
|<span data-ttu-id="f2b20-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="f2b20-110">FALSE</span></span>  <br/> |<span data-ttu-id="f2b20-111">В enable the command name (the default).</span><span class="sxs-lookup"><span data-stu-id="f2b20-111">Enable the command name (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2b20-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="f2b20-112">Remarks</span></span>

<span data-ttu-id="f2b20-113">Чтобы получить ссылку на ячейку Disabled по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="f2b20-113">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f2b20-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="f2b20-114">Cell name:</span></span>  <br/> |<span data-ttu-id="f2b20-115">Действия.</span><span class="sxs-lookup"><span data-stu-id="f2b20-115">Actions.</span></span> <span data-ttu-id="f2b20-116">*name*  . Отключено, где действия.</span><span class="sxs-lookup"><span data-stu-id="f2b20-116">*name*  .Disabled           where Actions.</span></span> <span data-ttu-id="f2b20-117">*имя*  — это имя строки "Действия"</span><span class="sxs-lookup"><span data-stu-id="f2b20-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="f2b20-118">Чтобы получить ссылку на ячейку Disabled по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="f2b20-118">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f2b20-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f2b20-119">Section index:</span></span>  <br/> |<span data-ttu-id="f2b20-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="f2b20-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="f2b20-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f2b20-121">Row index:</span></span>  <br/> |<span data-ttu-id="f2b20-122">**visRowAction**  +   *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f2b20-122">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="f2b20-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f2b20-123">Cell index:</span></span>  <br/> |<span data-ttu-id="f2b20-124">**visActionDisabled**</span><span class="sxs-lookup"><span data-stu-id="f2b20-124">**visActionDisabled**</span></span> <br/> |
   

