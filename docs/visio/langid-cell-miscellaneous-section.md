---
title: Ячейка LangID (раздел "Прочее")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60051
localization_priority: Normal
ms.assetid: 815e0df8-5ebf-ef1b-d620-bce8abb69f1a
description: Указывает язык, на какие ячейки были созданы формулы.
ms.openlocfilehash: 669bde032daeda90b22cdab5d1758c6cbd4109d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814071"
---
# <a name="langid-cell-miscellaneous-section"></a><span data-ttu-id="31e68-103">Ячейка LangID (раздел "Прочее")</span><span class="sxs-lookup"><span data-stu-id="31e68-103">LangID Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="31e68-104">Указывает язык, на какие ячейки были созданы формулы.</span><span class="sxs-lookup"><span data-stu-id="31e68-104">Indicates the language in which cell formulas were created.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="31e68-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="31e68-105">Remarks</span></span>

<span data-ttu-id="31e68-106">Список языков, поддерживаемых приложений Microsoft Office приведены в разделе [DocLangID](doclangid-cell-document-properties-section.md) ячейки (раздел свойства документа).</span><span class="sxs-lookup"><span data-stu-id="31e68-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="31e68-107">Для получения ссылки на ячейки LangID по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="31e68-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="31e68-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="31e68-108">Cell name:</span></span>  <br/> | <span data-ttu-id="31e68-109">LangID</span><span class="sxs-lookup"><span data-stu-id="31e68-109">LangID</span></span>  <br/> |
   
<span data-ttu-id="31e68-110">Для получения ссылки на ячейки LangID по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="31e68-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="31e68-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="31e68-111">Section index:</span></span>  <br/> |<span data-ttu-id="31e68-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="31e68-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="31e68-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="31e68-113">Row index:</span></span>  <br/> |<span data-ttu-id="31e68-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="31e68-114">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="31e68-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="31e68-115">Cell index:</span></span>  <br/> |<span data-ttu-id="31e68-116">**visObjLangID**</span><span class="sxs-lookup"><span data-stu-id="31e68-116">**visObjLangID**</span></span> <br/> |
   

