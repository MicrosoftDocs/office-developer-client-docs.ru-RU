---
title: LocalizeMerge Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033773
localization_priority: Normal
ms.assetid: 734d4415-05dd-4c4d-763e-e035fa56dcec
description: Определяет, локализуются ли формы при их копировании в документы.
ms.openlocfilehash: ddd6041ec6531652deb38a0c16be2c741bac91a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405676"
---
# <a name="localizemerge-cell-miscellaneous-section"></a><span data-ttu-id="71660-103">LocalizeMerge Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="71660-103">LocalizeMerge Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="71660-104">Определяет, локализуются ли формы при их копировании в документы.</span><span class="sxs-lookup"><span data-stu-id="71660-104">Determines whether shapes are localized when copied between documents.</span></span>
  
|<span data-ttu-id="71660-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="71660-105">**Value**</span></span>|<span data-ttu-id="71660-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="71660-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="71660-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="71660-107">TRUE</span></span>  <br/> | <span data-ttu-id="71660-108">Локализация фигуры на языке целевого документа.</span><span class="sxs-lookup"><span data-stu-id="71660-108">Localize a shape in the language of the destination document.</span></span>  <br/> |
| <span data-ttu-id="71660-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="71660-109">FALSE</span></span>  <br/> | <span data-ttu-id="71660-110">Не следует локализовать фигуру на основе языка конечного документа (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="71660-110">Do not localize a shape based on the language of the destination document (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71660-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="71660-111">Remarks</span></span>

<span data-ttu-id="71660-112">Чтобы получить ссылку на ячейку LocalizeMerge по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="71660-112">To get a reference to the LocalizeMerge cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="71660-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="71660-113">Cell name:</span></span>  <br/> | <span data-ttu-id="71660-114">LocalizeMerge</span><span class="sxs-lookup"><span data-stu-id="71660-114">LocalizeMerge</span></span>  <br/> |
   
<span data-ttu-id="71660-115">Чтобы получить ссылку на ячейку LocalizeMerge по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="71660-115">To get a reference to the LocalizeMerge cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="71660-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="71660-116">Section index:</span></span>  <br/> |<span data-ttu-id="71660-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="71660-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="71660-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="71660-118">Row index:</span></span>  <br/> |<span data-ttu-id="71660-119">**Висровмиск**</span><span class="sxs-lookup"><span data-stu-id="71660-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="71660-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="71660-120">Cell index:</span></span>  <br/> |<span data-ttu-id="71660-121">**Висобжлокализемерже**</span><span class="sxs-lookup"><span data-stu-id="71660-121">**visObjLocalizeMerge**</span></span> <br/> |
   

