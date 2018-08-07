---
title: Ячейка LangID (раздел "Примечание")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60048
localization_priority: Normal
ms.assetid: b6f5ea5e-b350-0817-d631-f059b9b95c23
description: Указывает язык, в котором был введен комментарий.
ms.openlocfilehash: 0de5ed8136a3fb1bbdca9fea0ebb5894e62cf907
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814032"
---
# <a name="langid-cell-annotation-section"></a><span data-ttu-id="010c8-103">Ячейка LangID (раздел "Примечание")</span><span class="sxs-lookup"><span data-stu-id="010c8-103">LangID Cell (Annotation Section)</span></span>

<span data-ttu-id="010c8-104">Указывает язык, в котором был введен комментарий.</span><span class="sxs-lookup"><span data-stu-id="010c8-104">Indicates the language in which the comment was entered.</span></span>
  
> [!NOTE]
> <span data-ttu-id="010c8-105">В этой ячейке используется для контроля комментариев только при открытии VSD-файл в Microsoft Visio 2013 или при сохранении файла vsdx (en) в формате .vsd.</span><span class="sxs-lookup"><span data-stu-id="010c8-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="010c8-106">Он не используется для отслеживания комментариев в документах vsdx (en) в Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="010c8-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="010c8-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="010c8-107">Remarks</span></span>

<span data-ttu-id="010c8-108">Это значение — код языка (LCID) языка, который является активным на панели языка при вводе комментария.</span><span class="sxs-lookup"><span data-stu-id="010c8-108">This value is the locale ID (LCID) of the language that is active on the language bar when the comment was entered.</span></span> <span data-ttu-id="010c8-109">Список языков, поддерживаемых приложений Microsoft Office приведены в разделе [DocLangID](doclangid-cell-document-properties-section.md) ячейки (раздел свойства документа).</span><span class="sxs-lookup"><span data-stu-id="010c8-109">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="010c8-110">Для получения ссылки на ячейки LangID по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="010c8-110">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="010c8-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="010c8-111">Cell name:</span></span>  <br/> | <span data-ttu-id="010c8-112">Annotation.LangID [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="010c8-112">Annotation.LangID[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="010c8-113">Для получения ссылки на ячейки LangID по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="010c8-113">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="010c8-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="010c8-114">Section index:</span></span>  <br/> |<span data-ttu-id="010c8-115">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="010c8-115">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="010c8-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="010c8-116">Row index:</span></span>  <br/> |<span data-ttu-id="010c8-117">**visRowAnnotation** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="010c8-117">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="010c8-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="010c8-118">Cell index:</span></span>  <br/> |<span data-ttu-id="010c8-119">**visAnnotationLangID**</span><span class="sxs-lookup"><span data-stu-id="010c8-119">**visAnnotationLangID**</span></span> <br/> |
   

