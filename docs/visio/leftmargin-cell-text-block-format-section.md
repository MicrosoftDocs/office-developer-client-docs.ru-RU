---
title: Ячейка LeftMargin (раздел "Формат текстового блока")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251265
localization_priority: Normal
ms.assetid: 47d84d7d-08a0-1934-d156-702da848e01c
description: Определяет расстояние между левой границей блока текста и текст, которые он содержит. Значение по умолчанию — 0,1 дюйма. Это значение не зависит от масштаба документа. Если документа изменяется, левое поле остается неизменным.
ms.openlocfilehash: d24ba33bffea1529490b49e105fec5d01cd828b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814062"
---
# <a name="leftmargin-cell-text-block-format-section"></a><span data-ttu-id="cf23e-106">Ячейка LeftMargin (раздел "Формат текстового блока")</span><span class="sxs-lookup"><span data-stu-id="cf23e-106">LeftMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="cf23e-107">Определяет расстояние между левой границей блока текста и текст, которые он содержит.</span><span class="sxs-lookup"><span data-stu-id="cf23e-107">Determines the distance between the left border of the text block and the text it contains.</span></span> <span data-ttu-id="cf23e-108">Значение по умолчанию — 0,1 дюйма.</span><span class="sxs-lookup"><span data-stu-id="cf23e-108">The default is 0.1 inch.</span></span> <span data-ttu-id="cf23e-109">Это значение не зависит от масштаба документа.</span><span class="sxs-lookup"><span data-stu-id="cf23e-109">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="cf23e-110">Если документа изменяется, левое поле остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="cf23e-110">If the drawing is scaled, the left margin remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cf23e-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="cf23e-111">Remarks</span></span>

<span data-ttu-id="cf23e-112">Для получения ссылки на ячейки LeftMargin по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="cf23e-112">To get a reference to the LeftMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cf23e-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="cf23e-113">Cell name:</span></span>  <br/> | <span data-ttu-id="cf23e-114">LeftMargin</span><span class="sxs-lookup"><span data-stu-id="cf23e-114">LeftMargin</span></span>  <br/> |
   
<span data-ttu-id="cf23e-115">Для получения ссылки на ячейки LeftMargin по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="cf23e-115">To get a reference to the LeftMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cf23e-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="cf23e-116">Section index:</span></span>  <br/> |<span data-ttu-id="cf23e-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cf23e-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="cf23e-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="cf23e-118">Row index:</span></span>  <br/> |<span data-ttu-id="cf23e-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="cf23e-119">**visRowText**</span></span> <br/> |
| <span data-ttu-id="cf23e-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="cf23e-120">Cell index:</span></span>  <br/> |<span data-ttu-id="cf23e-121">**visTxtBlkLeftMargin**</span><span class="sxs-lookup"><span data-stu-id="cf23e-121">**visTxtBlkLeftMargin**</span></span> <br/> |
   

