---
title: LangID Cell (Shape Data Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033771
localization_priority: Normal
ms.assetid: 6bd2781a-d4e7-136f-8996-62ebc5f890ab
description: Указывает язык, на котором было введено значение данных фигуры.
ms.openlocfilehash: c5a0cca5f71bc5520337ad2bdcf354a2b4affe92
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420327"
---
# <a name="langid-cell-shape-data-section"></a><span data-ttu-id="74033-103">LangID Cell (Shape Data Section)</span><span class="sxs-lookup"><span data-stu-id="74033-103">LangID Cell (Shape Data Section)</span></span>

<span data-ttu-id="74033-104">Указывает язык, на котором было введено значение данных фигуры.</span><span class="sxs-lookup"><span data-stu-id="74033-104">Indicates the language in which the shape data value was entered.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="74033-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="74033-105">Remarks</span></span>

<span data-ttu-id="74033-106">Список языков, поддерживаемых приложениями Microsoft Office, представлен в ячейке [DocLangID](doclangid-cell-document-properties-section.md) (раздел "Свойства документа").</span><span class="sxs-lookup"><span data-stu-id="74033-106">For a list of languages supported by Microsoft Office System applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section).</span></span> 
  
<span data-ttu-id="74033-107">Чтобы получить ссылку на ячейку LangID по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="74033-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="74033-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="74033-108">Cell name:</span></span>  <br/> | <span data-ttu-id="74033-109">Установите.  *Name (имя* ). LangID, где prop.  *Name* — имя строки</span><span class="sxs-lookup"><span data-stu-id="74033-109">Prop.  *name*  .LangID            where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="74033-110">Чтобы получить ссылку на ячейку LangID по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="74033-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="74033-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="74033-111">Section index:</span></span>  <br/> |<span data-ttu-id="74033-112">**виссектионпроп**</span><span class="sxs-lookup"><span data-stu-id="74033-112">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="74033-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="74033-113">Row index:</span></span>  <br/> |<span data-ttu-id="74033-114">**висровпроп** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="74033-114">**visRowProp** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="74033-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="74033-115">Cell index:</span></span>  <br/> |<span data-ttu-id="74033-116">**вискустпропслангид**</span><span class="sxs-lookup"><span data-stu-id="74033-116">**visCustPropsLangID**</span></span> <br/> |
   

