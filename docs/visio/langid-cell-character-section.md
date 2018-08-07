---
title: Ячейка LangID (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033769
localization_priority: Normal
ms.assetid: c68289b8-ef45-9e1e-12ae-6613587e4990
description: Указывает язык, на котором был введен текст.
ms.openlocfilehash: e503abb2365635fa25a4dbec54b7fe3da4043fa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814028"
---
# <a name="langid-cell-character-section"></a><span data-ttu-id="97d28-103">Ячейка LangID (раздел "Символ")</span><span class="sxs-lookup"><span data-stu-id="97d28-103">LangID Cell (Character Section)</span></span>

<span data-ttu-id="97d28-104">Указывает язык, на котором был введен текст.</span><span class="sxs-lookup"><span data-stu-id="97d28-104">Indicates the language in which the text was entered.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="97d28-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="97d28-105">Remarks</span></span>

<span data-ttu-id="97d28-106">Список языков, поддерживаемых приложений Microsoft Office приведены в разделе [DocLangID](doclangid-cell-document-properties-section.md) ячейки (раздел свойства документа).</span><span class="sxs-lookup"><span data-stu-id="97d28-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="97d28-107">Для получения ссылки на ячейки LangID по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="97d28-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97d28-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="97d28-108">Cell name:</span></span>  <br/> | <span data-ttu-id="97d28-109">Char.LangID [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="97d28-109">Char.LangID[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="97d28-110">Для получения ссылки на ячейки LangID по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="97d28-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97d28-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="97d28-111">Section index:</span></span>  <br/> |<span data-ttu-id="97d28-112">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="97d28-112">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="97d28-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="97d28-113">Row index:</span></span>  <br/> |<span data-ttu-id="97d28-114">**visRowCharacter** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="97d28-114">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="97d28-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="97d28-115">Cell index:</span></span>  <br/> |<span data-ttu-id="97d28-116">**visCharacterLangID**</span><span class="sxs-lookup"><span data-stu-id="97d28-116">**visCharacterLangID**</span></span> <br/> |
   

