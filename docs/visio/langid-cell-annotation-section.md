---
title: LangID Cell (Annotation Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60048
localization_priority: Normal
ms.assetid: b6f5ea5e-b350-0817-d631-f059b9b95c23
description: Указывает язык, на котором был введен комментарий.
ms.openlocfilehash: b3b2cba3d0a04f75ef2d87f0ee8dcd1f8115e15e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360552"
---
# <a name="langid-cell-annotation-section"></a><span data-ttu-id="3d9d1-103">LangID Cell (Annotation Section)</span><span class="sxs-lookup"><span data-stu-id="3d9d1-103">LangID Cell (Annotation Section)</span></span>

<span data-ttu-id="3d9d1-104">Указывает язык, на котором был введен комментарий.</span><span class="sxs-lookup"><span data-stu-id="3d9d1-104">Indicates the language in which the comment was entered.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3d9d1-105">Эта ячейка используется для отслеживания комментариев только при открытии VSD-файла в Microsoft Visio 2013 или при сохранении VSDX-файла в формате VSD-файла.</span><span class="sxs-lookup"><span data-stu-id="3d9d1-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="3d9d1-106">Она не используется для отслеживания комментариев в VSDX-документах в Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="3d9d1-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3d9d1-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="3d9d1-107">Remarks</span></span>

<span data-ttu-id="3d9d1-108">Это значение представляет собой код языка (LCID), который активен на языковой панели при вводе комментария.</span><span class="sxs-lookup"><span data-stu-id="3d9d1-108">This value is the locale ID (LCID) of the language that is active on the language bar when the comment was entered.</span></span> <span data-ttu-id="3d9d1-109">Список языков, поддерживаемых приложениями Microsoft Office, приведен в разделе [DocLangID](doclangid-cell-document-properties-section.md) Cell (раздел "Свойства документа").</span><span class="sxs-lookup"><span data-stu-id="3d9d1-109">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="3d9d1-110">Чтобы получить ссылку на ячейку LangID по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="3d9d1-110">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3d9d1-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="3d9d1-111">Cell name:</span></span>  <br/> | <span data-ttu-id="3d9d1-112">Аннотация. LangID [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="3d9d1-112">Annotation.LangID[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="3d9d1-113">Чтобы получить ссылку на ячейку LangID по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="3d9d1-113">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3d9d1-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="3d9d1-114">Section index:</span></span>  <br/> |<span data-ttu-id="3d9d1-115">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="3d9d1-115">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="3d9d1-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="3d9d1-116">Row index:</span></span>  <br/> |<span data-ttu-id="3d9d1-117">**visRowAnnotation** +  *i*, где *i* = 0, 1, 2…</span><span class="sxs-lookup"><span data-stu-id="3d9d1-117">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3d9d1-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="3d9d1-118">Cell index:</span></span>  <br/> |<span data-ttu-id="3d9d1-119">**Висаннотатионлангид**</span><span class="sxs-lookup"><span data-stu-id="3d9d1-119">**visAnnotationLangID**</span></span> <br/> |
   

