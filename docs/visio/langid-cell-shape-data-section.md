---
title: Ячейка LangID (раздел "Данные фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033771
localization_priority: Normal
ms.assetid: 6bd2781a-d4e7-136f-8996-62ebc5f890ab
description: Указывает язык, в котором было введено значение данных фигуры.
ms.openlocfilehash: 696c42483390509474eb82bd8cc0046beee345e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814051"
---
# <a name="langid-cell-shape-data-section"></a><span data-ttu-id="c18a3-103">Ячейка LangID (раздел "Данные фигуры")</span><span class="sxs-lookup"><span data-stu-id="c18a3-103">LangID Cell (Shape Data Section)</span></span>

<span data-ttu-id="c18a3-104">Указывает язык, в котором было введено значение данных фигуры.</span><span class="sxs-lookup"><span data-stu-id="c18a3-104">Indicates the language in which the shape data value was entered.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c18a3-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="c18a3-105">Remarks</span></span>

<span data-ttu-id="c18a3-106">Список языков, поддерживаемых приложениях системы Microsoft Office в разделе [DocLangID](doclangid-cell-document-properties-section.md) ячейки (раздел свойства документа).</span><span class="sxs-lookup"><span data-stu-id="c18a3-106">For a list of languages supported by Microsoft Office System applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section).</span></span> 
  
<span data-ttu-id="c18a3-107">Для получения ссылки на ячейки LangID по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="c18a3-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c18a3-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="c18a3-108">Cell name:</span></span>  <br/> | <span data-ttu-id="c18a3-109">Свойства.  *имя* . LangID где свойств.  *имя* — это имя строки</span><span class="sxs-lookup"><span data-stu-id="c18a3-109">Prop.  *name*  .LangID            where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="c18a3-110">Для получения ссылки на ячейки LangID по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="c18a3-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c18a3-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c18a3-111">Section index:</span></span>  <br/> |<span data-ttu-id="c18a3-112">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="c18a3-112">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="c18a3-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c18a3-113">Row index:</span></span>  <br/> |<span data-ttu-id="c18a3-114">**visRowProp** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c18a3-114">**visRowProp** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c18a3-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c18a3-115">Cell index:</span></span>  <br/> |<span data-ttu-id="c18a3-116">**visCustPropsLangID**</span><span class="sxs-lookup"><span data-stu-id="c18a3-116">**visCustPropsLangID**</span></span> <br/> |
   

