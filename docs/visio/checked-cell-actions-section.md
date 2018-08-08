---
title: Ячейка Checked (раздел "Действия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm155
localization_priority: Normal
ms.assetid: 50937e29-eaa1-0cd0-53cc-dc17e7793e55
description: Указывает, установлен ли флажок элемента в меню тега ярлык или действие.
ms.openlocfilehash: 7c5bcdbfe5b7d8e796af49c8da6ef0fc233e3d62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813402"
---
# <a name="checked-cell-actions-section"></a><span data-ttu-id="1b73b-103">Ячейка Checked (раздел "Действия")</span><span class="sxs-lookup"><span data-stu-id="1b73b-103">Checked Cell (Actions Section)</span></span>

<span data-ttu-id="1b73b-104">Указывает, установлен ли флажок элемента в меню тега ярлык или действие.</span><span class="sxs-lookup"><span data-stu-id="1b73b-104">Indicates whether an item is checked on the shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1b73b-105">В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="1b73b-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="1b73b-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="1b73b-106">**Value**</span></span>|<span data-ttu-id="1b73b-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1b73b-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1b73b-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="1b73b-108">TRUE</span></span>  <br/> |<span data-ttu-id="1b73b-109">Галочка.</span><span class="sxs-lookup"><span data-stu-id="1b73b-109">Check mark is displayed.</span></span>  <br/> |
|<span data-ttu-id="1b73b-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="1b73b-110">FALSE</span></span>  <br/> |<span data-ttu-id="1b73b-111">Флажок не отображаются (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="1b73b-111">Check mark is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b73b-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="1b73b-112">Remarks</span></span>

<span data-ttu-id="1b73b-113">Чтобы получить ссылку на установленное состояние ячейки по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="1b73b-113">To get a reference to the Checked cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1b73b-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="1b73b-114">Cell name:</span></span>  <br/> |<span data-ttu-id="1b73b-115">Действия.</span><span class="sxs-lookup"><span data-stu-id="1b73b-115">Actions.</span></span> <span data-ttu-id="1b73b-116">*имя* . Где проверяются действия.</span><span class="sxs-lookup"><span data-stu-id="1b73b-116">*name*  .Checked           where Actions.</span></span> <span data-ttu-id="1b73b-117">*имя* — это имя строки действий</span><span class="sxs-lookup"><span data-stu-id="1b73b-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="1b73b-118">Для получения ссылки на ячейки установлен по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="1b73b-118">To get a reference to the Checked cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1b73b-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="1b73b-119">Section index:</span></span>  <br/> |<span data-ttu-id="1b73b-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="1b73b-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="1b73b-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="1b73b-121">Row index:</span></span>  <br/> |<span data-ttu-id="1b73b-122">**visRowAction** +  *i* где *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="1b73b-122">**visRowAction** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="1b73b-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="1b73b-123">Cell index:</span></span>  <br/> |<span data-ttu-id="1b73b-124">**visActionChecked**</span><span class="sxs-lookup"><span data-stu-id="1b73b-124">**visActionChecked**</span></span> <br/> |
   

