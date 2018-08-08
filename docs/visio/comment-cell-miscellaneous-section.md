---
title: Ячейка Comment (раздел "Прочее")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm170
localization_priority: Normal
ms.assetid: 6f52ed60-d58b-86e6-f7e2-2ef19d4afa75
description: Содержит текст комментария в формате строки для фигуры.
ms.openlocfilehash: f5222836b29a26cc26ca8093576d0962f0592fae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813412"
---
# <a name="comment-cell-miscellaneous-section"></a><span data-ttu-id="c6ab0-103">Ячейка Comment (раздел "Прочее")</span><span class="sxs-lookup"><span data-stu-id="c6ab0-103">Comment Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="c6ab0-104">Содержит текст комментария в формате строки для фигуры.</span><span class="sxs-lookup"><span data-stu-id="c6ab0-104">Contains the comment text in string format for a shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c6ab0-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="c6ab0-105">Remarks</span></span>

<span data-ttu-id="c6ab0-106">Также можно добавить примечание, нажав кнопку **Создать примечание** на вкладке **Обзор** .</span><span class="sxs-lookup"><span data-stu-id="c6ab0-106">You can also insert a comment by clicking **New Comment** on the **Review** tab.</span></span> 
  
<span data-ttu-id="c6ab0-107">Чтобы получить ссылку на ячейку комментария по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="c6ab0-107">To get a reference to the Comment cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c6ab0-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="c6ab0-108">Cell name:</span></span>  <br/> |<span data-ttu-id="c6ab0-109">Comment</span><span class="sxs-lookup"><span data-stu-id="c6ab0-109">Comment</span></span>  <br/> |
   
<span data-ttu-id="c6ab0-110">Для получения ссылки на ячейки комментарий по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="c6ab0-110">To get a reference to the Comment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c6ab0-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c6ab0-111">Section index:</span></span>  <br/> |<span data-ttu-id="c6ab0-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c6ab0-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c6ab0-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c6ab0-113">Row index:</span></span>  <br/> |<span data-ttu-id="c6ab0-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="c6ab0-114">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="c6ab0-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c6ab0-115">Cell index:</span></span>  <br/> |<span data-ttu-id="c6ab0-116">**visComment**</span><span class="sxs-lookup"><span data-stu-id="c6ab0-116">**visComment**</span></span> <br/> |
   

