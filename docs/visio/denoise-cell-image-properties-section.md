---
title: Ячейка Denoise (раздел "Свойства изображения")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm225
localization_priority: Normal
ms.assetid: e305585f-f0d8-0494-91d4-0c76929dc170
description: 'Удаление помех (точки со случайно распределенными уровнями цвета) из точечного рисунка. Значение по умолчанию: 0%.'
ms.openlocfilehash: f08d09126a24935c0dd4dcda5e88fdd559c8d176
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813605"
---
# <a name="denoise-cell-image-properties-section"></a><span data-ttu-id="fa990-104">Ячейка Denoise (раздел "Свойства изображения")</span><span class="sxs-lookup"><span data-stu-id="fa990-104">Denoise Cell (Image Properties Section)</span></span>

<span data-ttu-id="fa990-105">Удаление помех (точки со случайно распределенными уровнями цвета) из точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="fa990-105">Removes noise (pixels with randomly distributed color levels) from a bitmap image.</span></span> <span data-ttu-id="fa990-106">Значение по умолчанию: 0%.</span><span class="sxs-lookup"><span data-stu-id="fa990-106">The default value is 0%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fa990-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="fa990-107">Remarks</span></span>

<span data-ttu-id="fa990-108">Чтобы получить ссылку на ячейку Denoise по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="fa990-108">To get a reference to the Denoise cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fa990-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="fa990-109">Cell name:</span></span>  <br/> | <span data-ttu-id="fa990-110">Устранение шума</span><span class="sxs-lookup"><span data-stu-id="fa990-110">Denoise</span></span>  <br/> |
   
<span data-ttu-id="fa990-111">Для получения ссылки на ячейки Denoise по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="fa990-111">To get a reference to the Denoise cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fa990-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="fa990-112">Section index:</span></span>  <br/> |<span data-ttu-id="fa990-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fa990-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fa990-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="fa990-114">Row index:</span></span>  <br/> |<span data-ttu-id="fa990-115">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="fa990-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="fa990-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="fa990-116">Cell index:</span></span>  <br/> |<span data-ttu-id="fa990-117">**visImageDenoise**</span><span class="sxs-lookup"><span data-stu-id="fa990-117">**visImageDenoise**</span></span> <br/> |
   

