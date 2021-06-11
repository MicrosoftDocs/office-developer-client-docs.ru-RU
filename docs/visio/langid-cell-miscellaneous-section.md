---
title: LangID Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60051
localization_priority: Normal
ms.assetid: 815e0df8-5ebf-ef1b-d620-bce8abb69f1a
description: Указывает язык, на котором были созданы формулы ячейки.
ms.openlocfilehash: e1e5b92f01e97bc63003a4b195c159a50f61e77b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406677"
---
# <a name="langid-cell-miscellaneous-section"></a><span data-ttu-id="b9de8-103">LangID Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="b9de8-103">LangID Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="b9de8-104">Указывает язык, на котором были созданы формулы ячейки.</span><span class="sxs-lookup"><span data-stu-id="b9de8-104">Indicates the language in which cell formulas were created.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b9de8-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="b9de8-105">Remarks</span></span>

<span data-ttu-id="b9de8-106">Список языков, поддерживаемых Microsoft Office приложениями, см. в разделе [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section).</span><span class="sxs-lookup"><span data-stu-id="b9de8-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="b9de8-107">Чтобы получить ссылку на ячейку LangID по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="b9de8-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b9de8-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b9de8-108">Cell name:</span></span>  <br/> | <span data-ttu-id="b9de8-109">LangID</span><span class="sxs-lookup"><span data-stu-id="b9de8-109">LangID</span></span>  <br/> |
   
<span data-ttu-id="b9de8-110">Чтобы получить ссылку на ячейку LangID по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b9de8-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b9de8-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b9de8-111">Section index:</span></span>  <br/> |<span data-ttu-id="b9de8-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b9de8-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b9de8-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b9de8-113">Row index:</span></span>  <br/> |<span data-ttu-id="b9de8-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="b9de8-114">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="b9de8-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b9de8-115">Cell index:</span></span>  <br/> |<span data-ttu-id="b9de8-116">**visObjLangID**</span><span class="sxs-lookup"><span data-stu-id="b9de8-116">**visObjLangID**</span></span> <br/> |
   

