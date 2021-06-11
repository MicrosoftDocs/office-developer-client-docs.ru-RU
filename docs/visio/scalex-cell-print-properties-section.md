---
title: ScaleX Cell (Print Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60072
localization_priority: Normal
ms.assetid: 5916eadc-37f8-47af-fe54-f6062aea318f
description: Указывает процент увеличения страницы рисования на странице принтера.
ms.openlocfilehash: d1c2f6c184f987e1e7190b1c208310b83a823ee3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410212"
---
# <a name="scalex-cell-print-properties-section"></a><span data-ttu-id="13281-103">ScaleX Cell (Print Properties Section)</span><span class="sxs-lookup"><span data-stu-id="13281-103">ScaleX Cell (Print Properties Section)</span></span>

<span data-ttu-id="13281-104">Указывает процент увеличения страницы рисования на странице принтера.</span><span class="sxs-lookup"><span data-stu-id="13281-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="13281-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="13281-105">Remarks</span></span>

<span data-ttu-id="13281-106">Это значение используется только в том случае, если значение ячейки OnPage false.</span><span class="sxs-lookup"><span data-stu-id="13281-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="13281-107">Ячейки ScaleX и ScaleY всегда имеют одно и то  же значение,  соответствующее значению  в вкладке Настройка  печати в диалоговом окне Установка страницы (на вкладке Design щелкните стрелку **установки** страницы).</span><span class="sxs-lookup"><span data-stu-id="13281-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="13281-108">Чтобы получить ссылку на ячейку ScaleX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="13281-108">To get a reference to the ScaleX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="13281-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="13281-109">Cell name:</span></span>  <br/> |<span data-ttu-id="13281-110">ScaleX</span><span class="sxs-lookup"><span data-stu-id="13281-110">ScaleX</span></span>  <br/> |
   
<span data-ttu-id="13281-111">Чтобы получить ссылку на ячейку ScaleX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="13281-111">To get a reference to the ScaleX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="13281-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="13281-112">Section index:</span></span>  <br/> |<span data-ttu-id="13281-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="13281-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="13281-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="13281-114">Row index:</span></span>  <br/> |<span data-ttu-id="13281-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="13281-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="13281-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="13281-116">Cell index:</span></span>  <br/> |<span data-ttu-id="13281-117">**visPrintPropertiesScaleX**</span><span class="sxs-lookup"><span data-stu-id="13281-117">**visPrintPropertiesScaleX**</span></span> <br/> |
   

