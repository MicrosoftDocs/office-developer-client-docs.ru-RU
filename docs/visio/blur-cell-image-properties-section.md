---
title: Blur Cell (Image Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm115
localization_priority: Normal
ms.assetid: 8b077cdb-6036-4f77-dc20-a476bb75b0f7
description: 'Размытие или смягчение растрового изображения. Значение по умолчанию: 0%.'
ms.openlocfilehash: 599810d126c853e37552045d0ef83cb580606ae2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348981"
---
# <a name="blur-cell-image-properties-section"></a><span data-ttu-id="97537-104">Blur Cell (Image Properties Section)</span><span class="sxs-lookup"><span data-stu-id="97537-104">Blur Cell (Image Properties Section)</span></span>

<span data-ttu-id="97537-105">Размытие или смягчение растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="97537-105">Blurs or softens a bitmap image.</span></span> <span data-ttu-id="97537-106">Значение по умолчанию: 0%.</span><span class="sxs-lookup"><span data-stu-id="97537-106">The default value is 0%.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="97537-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="97537-107">Remarks</span></span>

<span data-ttu-id="97537-108">Чтобы получить ссылку на ячейку "Размытие" по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="97537-108">To get a reference to the Blur cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97537-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="97537-109">Cell name:</span></span>  <br/> | <span data-ttu-id="97537-110">Размытие</span><span class="sxs-lookup"><span data-stu-id="97537-110">Blur</span></span>  <br/> |
   
<span data-ttu-id="97537-111">Чтобы получить ссылку на ячейку "Размытие" по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="97537-111">To get a reference to the Blur cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97537-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="97537-112">Section index:</span></span>  <br/> |<span data-ttu-id="97537-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="97537-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="97537-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="97537-114">Row index:</span></span>  <br/> |<span data-ttu-id="97537-115">**Висровимаже**</span><span class="sxs-lookup"><span data-stu-id="97537-115">**visRowImage**</span></span> <br/> |
| <span data-ttu-id="97537-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="97537-116">Cell index:</span></span>  <br/> |<span data-ttu-id="97537-117">**Висимажеблур**</span><span class="sxs-lookup"><span data-stu-id="97537-117">**visImageBlur**</span></span> <br/> |
   

