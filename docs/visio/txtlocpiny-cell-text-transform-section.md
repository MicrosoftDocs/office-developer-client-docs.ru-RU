---
title: Ячейка TxtLocPinY (раздел Преобразование текст)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251276
localization_priority: Normal
ms.assetid: 3f46cfcf-7eac-4a37-e782-39f4e7f8fc43
description: 'Определяет, y-координаты центра блок текста ротации относительно начала блока текста. Формула по умолчанию имеет вид:'
ms.openlocfilehash: 7d43f63b8560df5fc5daf09a429ce30ec976d131
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815076"
---
# <a name="txtlocpiny-cell-text-transform-section"></a><span data-ttu-id="40501-104">Ячейка TxtLocPinY (раздел Преобразование текст)</span><span class="sxs-lookup"><span data-stu-id="40501-104">TxtLocPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="40501-105">Определяет, *y* -координаты центра блок текста ротации относительно начала блока текста.</span><span class="sxs-lookup"><span data-stu-id="40501-105">Determines the  *y*  -coordinate of the text block's center of rotation relative to the origin of the text block.</span></span> <span data-ttu-id="40501-106">Формула по умолчанию имеет вид:</span><span class="sxs-lookup"><span data-stu-id="40501-106">The default formula is:</span></span> 
  
<span data-ttu-id="40501-107">= ВысотаТекста \* 0,5</span><span class="sxs-lookup"><span data-stu-id="40501-107">= TxtHeight \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="40501-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="40501-108">Remarks</span></span>

<span data-ttu-id="40501-109">Чтобы получить ссылку на ячейку TxtLocPinY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="40501-109">To get a reference to the TxtLocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="40501-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="40501-110">Cell name:</span></span>  <br/> | <span data-ttu-id="40501-111">TxtLocPinY</span><span class="sxs-lookup"><span data-stu-id="40501-111">TxtLocPinY</span></span>  <br/> |
   
<span data-ttu-id="40501-112">Для получения ссылки на ячейки TxtLocPinY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="40501-112">To get a reference to the TxtLocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="40501-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="40501-113">Section index:</span></span>  <br/> |<span data-ttu-id="40501-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="40501-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="40501-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="40501-115">Row index:</span></span>  <br/> |<span data-ttu-id="40501-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="40501-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="40501-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="40501-117">Cell index:</span></span>  <br/> |<span data-ttu-id="40501-118">**visXFormLocPinY**</span><span class="sxs-lookup"><span data-stu-id="40501-118">**visXFormLocPinY**</span></span> <br/> |
   

