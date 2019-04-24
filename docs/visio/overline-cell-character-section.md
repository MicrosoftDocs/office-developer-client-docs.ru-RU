---
title: Overline Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251728
localization_priority: Normal
ms.assetid: 102cce17-43ee-e313-3412-a72d6ee18fe6
description: Определяет, содержит ли текст линию над ним.
ms.openlocfilehash: d5df39c2f12890d5fb4881346516abdb4f2b8099
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327050"
---
# <a name="overline-cell-character-section"></a><span data-ttu-id="71be7-103">Overline Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="71be7-103">Overline Cell (Character Section)</span></span>

<span data-ttu-id="71be7-104">Определяет, содержит ли текст линию над ним.</span><span class="sxs-lookup"><span data-stu-id="71be7-104">Determines whether the text has a line above it.</span></span>
  
|<span data-ttu-id="71be7-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="71be7-105">**Value**</span></span>|<span data-ttu-id="71be7-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="71be7-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="71be7-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="71be7-107">TRUE</span></span>  <br/> |<span data-ttu-id="71be7-108">Над текстом есть линия.</span><span class="sxs-lookup"><span data-stu-id="71be7-108">Text has a line above it.</span></span>  <br/> |
|<span data-ttu-id="71be7-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="71be7-109">FALSE</span></span>  <br/> |<span data-ttu-id="71be7-110">Текст не содержит линию.</span><span class="sxs-lookup"><span data-stu-id="71be7-110">Text does not have a line above it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71be7-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="71be7-111">Remarks</span></span>

<span data-ttu-id="71be7-112">Значение этой ячейки также можно задать с помощью диалогового окна **текст** (на вкладке **Главная** щелкните значок со стрелкой **шрифта** ).</span><span class="sxs-lookup"><span data-stu-id="71be7-112">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="71be7-113">Чтобы получить ссылку на ячейку "строка" по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="71be7-113">To get a reference to the Overline cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="71be7-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="71be7-114">Cell name:</span></span>  <br/> |<span data-ttu-id="71be7-115">Char. перечеркивание [ *i* ], где *i* = <1>, 2.</span><span class="sxs-lookup"><span data-stu-id="71be7-115">Char.Overline[ *i*  ] where  *i*  = <1>, 2.</span></span> <span data-ttu-id="71be7-116">3...</span><span class="sxs-lookup"><span data-stu-id="71be7-116">3...</span></span>  <br/> |
   
<span data-ttu-id="71be7-117">Чтобы получить ссылку на ячейку с подчеркиванием по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="71be7-117">To get a reference to the Overline cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="71be7-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="71be7-118">Section index:</span></span>  <br/> |<span data-ttu-id="71be7-119">**Виссектиончарактер**</span><span class="sxs-lookup"><span data-stu-id="71be7-119">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="71be7-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="71be7-120">Row index:</span></span>  <br/> |<span data-ttu-id="71be7-121">**висровчарактер** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="71be7-121">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="71be7-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="71be7-122">Cell index:</span></span>  <br/> |<span data-ttu-id="71be7-123">**Висчарактероверлине**</span><span class="sxs-lookup"><span data-stu-id="71be7-123">**visCharacterOverline**</span></span> <br/> |
   

