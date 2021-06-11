---
title: TxtLocPinY Cell (Text Transform Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251276
localization_priority: Normal
ms.assetid: 3f46cfcf-7eac-4a37-e782-39f4e7f8fc43
description: 'Определяет y-координату центра вращения текстового блока относительно происхождения текстового блока. Формула по умолчанию:'
ms.openlocfilehash: 937c4e9928d32d55e8336d192b1ecc6140fd8381
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414062"
---
# <a name="txtlocpiny-cell-text-transform-section"></a><span data-ttu-id="17329-104">TxtLocPinY Cell (Text Transform Section)</span><span class="sxs-lookup"><span data-stu-id="17329-104">TxtLocPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="17329-105">Определяет  *y-координату*  центра вращения текстового блока относительно происхождения текстового блока.</span><span class="sxs-lookup"><span data-stu-id="17329-105">Determines the  *y*  -coordinate of the text block's center of rotation relative to the origin of the text block.</span></span> <span data-ttu-id="17329-106">Формула по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="17329-106">The default formula is:</span></span> 
  
<span data-ttu-id="17329-107">= TxtHeight \* 0.5</span><span class="sxs-lookup"><span data-stu-id="17329-107">= TxtHeight \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="17329-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="17329-108">Remarks</span></span>

<span data-ttu-id="17329-109">Чтобы получить ссылку на ячейку TxtLocPinY по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="17329-109">To get a reference to the TxtLocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17329-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="17329-110">Cell name:</span></span>  <br/> | <span data-ttu-id="17329-111">TxtLocPinY</span><span class="sxs-lookup"><span data-stu-id="17329-111">TxtLocPinY</span></span>  <br/> |
   
<span data-ttu-id="17329-112">Чтобы получить ссылку на ячейку TxtLocPinY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="17329-112">To get a reference to the TxtLocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17329-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="17329-113">Section index:</span></span>  <br/> |<span data-ttu-id="17329-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="17329-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="17329-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="17329-115">Row index:</span></span>  <br/> |<span data-ttu-id="17329-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="17329-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="17329-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="17329-117">Cell index:</span></span>  <br/> |<span data-ttu-id="17329-118">**visXFormLocPinY**</span><span class="sxs-lookup"><span data-stu-id="17329-118">**visXFormLocPinY**</span></span> <br/> |
   

