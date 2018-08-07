---
title: Ячейка Action (раздел "Действия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm5
localization_priority: Normal
ms.assetid: 435e49ee-0b51-8ce3-0589-3f0717026f4a
description: Содержит формулу для выполнения, если пользователь выбирает команду меню тега ярлык или действие.
ms.openlocfilehash: 123b05f9a08c4ffa656e08a51f019f888cf83ed4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813127"
---
# <a name="action-cell-actions-section"></a><span data-ttu-id="5e810-103">Ячейка Action (раздел "Действия")</span><span class="sxs-lookup"><span data-stu-id="5e810-103">Action Cell (Actions Section)</span></span>

<span data-ttu-id="5e810-104">Содержит формулу для выполнения, если пользователь выбирает команду меню тега ярлык или действие.</span><span class="sxs-lookup"><span data-stu-id="5e810-104">Contains the formula to be executed when a user chooses a command on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5e810-105">В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="5e810-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5e810-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="5e810-106">Remarks</span></span>

<span data-ttu-id="5e810-107">В действие ячейки вычисляется только в том случае, когда происходит действие, не при вводе формулы.</span><span class="sxs-lookup"><span data-stu-id="5e810-107">An Action cell is evaluated only when the action occurs, not when the formula is entered.</span></span>
  
<span data-ttu-id="5e810-108">Для получения ссылки на ячейки действие по имени из другой формулы или из файла с помощью свойства **CellsU** использования:</span><span class="sxs-lookup"><span data-stu-id="5e810-108">To get a reference to the the Action cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5e810-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="5e810-109">Cell name:</span></span>  <br/> | <span data-ttu-id="5e810-110">Действия.</span><span class="sxs-lookup"><span data-stu-id="5e810-110">Actions.</span></span>  <span data-ttu-id="5e810-111">*имя* . Действие которых действия.</span><span class="sxs-lookup"><span data-stu-id="5e810-111">*name*  .Action           where Actions.</span></span> <span data-ttu-id="5e810-112">*имя* — это имя строки действий</span><span class="sxs-lookup"><span data-stu-id="5e810-112">*name*  is the name of the actions row</span></span>  <br/> |
   
<span data-ttu-id="5e810-113">Для получения ссылки на ячейки thethe действие по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="5e810-113">To get a reference to thethe Action cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5e810-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5e810-114">Section index:</span></span>  <br/> |<span data-ttu-id="5e810-115">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="5e810-115">**visSectionAction**</span></span> <br/> |
| <span data-ttu-id="5e810-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5e810-116">Row index:</span></span>  <br/> |<span data-ttu-id="5e810-117">**visRowAction** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="5e810-117">**visRowAction** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5e810-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5e810-118">Cell index:</span></span>  <br/> |<span data-ttu-id="5e810-119">**visActionAction**</span><span class="sxs-lookup"><span data-stu-id="5e810-119">**visActionAction**</span></span> <br/> |
   

