---
title: Ячейка Tip (раздел "Элементы управления")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1010
localization_priority: Normal
ms.assetid: 7fd11650-fffa-1316-d302-3122ac5feb14
description: Представляет строку описательный текст, который отображается в виде подсказки при наведении указателя мыши на элемент управления маркера фигуры. Приложение автоматически заключает строку подсказки в кавычки в ячейке, но кавычки не отображаются в подсказке.
ms.openlocfilehash: ff593ee95dc27ba7192ee31d35791127b666eac0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815041"
---
# <a name="tip-cell-controls-section"></a><span data-ttu-id="26708-104">Ячейка Tip (раздел "Элементы управления")</span><span class="sxs-lookup"><span data-stu-id="26708-104">Tip Cell (Controls Section)</span></span>

<span data-ttu-id="26708-105">Представляет строку описательный текст, который отображается в виде подсказки при наведении указателя мыши на элемент управления маркера фигуры.</span><span class="sxs-lookup"><span data-stu-id="26708-105">Represents a descriptive text string that appears as a tool tip when a user pauses the pointer over a shape's control handle.</span></span> <span data-ttu-id="26708-106">Приложение автоматически заключает строку подсказки в кавычки в ячейке, но кавычки не отображаются в подсказке.</span><span class="sxs-lookup"><span data-stu-id="26708-106">The application automatically encloses the tip string in quotation marks in the cell, but the quotation marks are not displayed in the tool tip.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="26708-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="26708-107">Remarks</span></span>

<span data-ttu-id="26708-108">Для получения ссылки на ячейки совет по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="26708-108">To get a reference to the Tip cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="26708-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="26708-109">Cell name:</span></span>  <br/> | <span data-ttu-id="26708-110">Элементы управления.</span><span class="sxs-lookup"><span data-stu-id="26708-110">Controls.</span></span>  <span data-ttu-id="26708-111">*имя* . Элементы управления Tipwhere.</span><span class="sxs-lookup"><span data-stu-id="26708-111">*name*  .Tipwhere Controls.</span></span>  <span data-ttu-id="26708-112">*имя* — это имя строки элементов управления.</span><span class="sxs-lookup"><span data-stu-id="26708-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="26708-113">Для получения ссылки на ячейки совет по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="26708-113">To get a reference to the Tip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="26708-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="26708-114">Section index:</span></span>  <br/> |<span data-ttu-id="26708-115">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="26708-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="26708-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="26708-116">Row index:</span></span>  <br/> |<span data-ttu-id="26708-117">**visRowControl** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="26708-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="26708-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="26708-118">Cell index:</span></span>  <br/> |<span data-ttu-id="26708-119">**visCtlTip**</span><span class="sxs-lookup"><span data-stu-id="26708-119">**visCtlTip**</span></span> <br/> |
   

