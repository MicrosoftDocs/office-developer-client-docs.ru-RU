---
title: Ячейка TxtPinX (раздел "Преобразование текста")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1040
localization_priority: Normal
ms.assetid: d0c0fe52-6a9e-e40e-394e-83a851db55a4
description: 'Определяет значение x-координаты центра блок текста из ротации относительно начала фигуры. Формула по умолчанию имеет вид:'
ms.openlocfilehash: df103557d103dbde7e4a1c8d67cabe37a0af9311
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815078"
---
# <a name="txtpinx-cell-text-transform-section"></a><span data-ttu-id="6282e-104">Ячейка TxtPinX (раздел "Преобразование текста")</span><span class="sxs-lookup"><span data-stu-id="6282e-104">TxtPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="6282e-105">Определяет значение *x* -координаты центра блок текста из ротации относительно начала фигуры.</span><span class="sxs-lookup"><span data-stu-id="6282e-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="6282e-106">Формула по умолчанию имеет вид:</span><span class="sxs-lookup"><span data-stu-id="6282e-106">The default formula is:</span></span> 
  
<span data-ttu-id="6282e-107">= Ширина \* 0,5</span><span class="sxs-lookup"><span data-stu-id="6282e-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6282e-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="6282e-108">Remarks</span></span>

<span data-ttu-id="6282e-109">Чтобы получить ссылку на ячейку TxtPinX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="6282e-109">To get a reference to the TxtPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6282e-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="6282e-110">Cell name:</span></span>  <br/> | <span data-ttu-id="6282e-111">TxtPinX</span><span class="sxs-lookup"><span data-stu-id="6282e-111">TxtPinX</span></span>  <br/> |
   
<span data-ttu-id="6282e-112">Для получения ссылки на ячейки TxtPinX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="6282e-112">To get a reference to the TxtPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6282e-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="6282e-113">Section index:</span></span>  <br/> |<span data-ttu-id="6282e-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6282e-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6282e-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="6282e-115">Row index:</span></span>  <br/> |<span data-ttu-id="6282e-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="6282e-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="6282e-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="6282e-117">Cell index:</span></span>  <br/> |<span data-ttu-id="6282e-118">**visXFormPinX**</span><span class="sxs-lookup"><span data-stu-id="6282e-118">**visXFormPinX**</span></span> <br/> |
   

