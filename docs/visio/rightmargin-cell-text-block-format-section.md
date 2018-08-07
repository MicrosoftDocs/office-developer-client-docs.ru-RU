---
title: Ячейка RightMargin (раздел "Формат текстового блока")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251266
localization_priority: Normal
ms.assetid: bc8f5469-e79f-4a68-73cb-d11c938353a4
description: Определяет расстояние между правой границей блока текста и текст, которые он содержит. Значение по умолчанию — 0,1 дюйма.
ms.openlocfilehash: 57fdb320395a9a6562983a0148b37c4a70a9a9b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814613"
---
# <a name="rightmargin-cell-text-block-format-section"></a><span data-ttu-id="04f96-104">Ячейка RightMargin (раздел "Формат текстового блока")</span><span class="sxs-lookup"><span data-stu-id="04f96-104">RightMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="04f96-105">Определяет расстояние между правой границей блока текста и текст, которые он содержит.</span><span class="sxs-lookup"><span data-stu-id="04f96-105">Determines the distance between the right border of the text block and the text it contains.</span></span> <span data-ttu-id="04f96-106">Значение по умолчанию — 0,1 дюйма.</span><span class="sxs-lookup"><span data-stu-id="04f96-106">The default is 0.1 inch.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="04f96-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="04f96-107">Remarks</span></span>

<span data-ttu-id="04f96-108">Это значение не зависит от масштаба документа.</span><span class="sxs-lookup"><span data-stu-id="04f96-108">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="04f96-109">Если документа изменяется, правое остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="04f96-109">If the drawing is scaled, the right margin remains the same.</span></span>
  
<span data-ttu-id="04f96-110">Для получения ссылки на ячейки RightMargin по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="04f96-110">To get a reference to the RightMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="04f96-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="04f96-111">Cell name:</span></span>  <br/> | <span data-ttu-id="04f96-112">RightMargin</span><span class="sxs-lookup"><span data-stu-id="04f96-112">RightMargin</span></span>  <br/> |
   
<span data-ttu-id="04f96-113">Для получения ссылки на ячейки RightMargin по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="04f96-113">To get a reference to the RightMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="04f96-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="04f96-114">Section index:</span></span>  <br/> |<span data-ttu-id="04f96-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="04f96-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="04f96-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="04f96-116">Row index:</span></span>  <br/> |<span data-ttu-id="04f96-117">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="04f96-117">**visRowText**</span></span> <br/> |
| <span data-ttu-id="04f96-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="04f96-118">Cell index:</span></span>  <br/> |<span data-ttu-id="04f96-119">**visTxtBlkRightMargin**</span><span class="sxs-lookup"><span data-stu-id="04f96-119">**visTxtBlkRightMargin**</span></span> <br/> |
   

