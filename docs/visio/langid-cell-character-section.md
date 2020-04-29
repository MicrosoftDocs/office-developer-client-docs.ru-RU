---
title: LangID Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033769
localization_priority: Normal
ms.assetid: c68289b8-ef45-9e1e-12ae-6613587e4990
description: Указывает язык ввода текста.
ms.openlocfilehash: e1f244d6d8e31201576a9a88ace9701814b0e0a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419284"
---
# <a name="langid-cell-character-section"></a><span data-ttu-id="41c56-103">LangID Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="41c56-103">LangID Cell (Character Section)</span></span>

<span data-ttu-id="41c56-104">Указывает язык ввода текста.</span><span class="sxs-lookup"><span data-stu-id="41c56-104">Indicates the language in which the text was entered.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="41c56-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="41c56-105">Remarks</span></span>

<span data-ttu-id="41c56-106">Список языков, поддерживаемых приложениями Microsoft Office, приведен в разделе [DocLangID](doclangid-cell-document-properties-section.md) Cell (раздел "Свойства документа").</span><span class="sxs-lookup"><span data-stu-id="41c56-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="41c56-107">Чтобы получить ссылку на ячейку LangID по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="41c56-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="41c56-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="41c56-108">Cell name:</span></span>  <br/> | <span data-ttu-id="41c56-109">Char. LangID [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="41c56-109">Char.LangID[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="41c56-110">Чтобы получить ссылку на ячейку LangID по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="41c56-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="41c56-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="41c56-111">Section index:</span></span>  <br/> |<span data-ttu-id="41c56-112">**виссектиончарактер**</span><span class="sxs-lookup"><span data-stu-id="41c56-112">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="41c56-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="41c56-113">Row index:</span></span>  <br/> |<span data-ttu-id="41c56-114">**висровчарактер** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="41c56-114">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="41c56-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="41c56-115">Cell index:</span></span>  <br/> |<span data-ttu-id="41c56-116">**висчарактерлангид**</span><span class="sxs-lookup"><span data-stu-id="41c56-116">**visCharacterLangID**</span></span> <br/> |
   

