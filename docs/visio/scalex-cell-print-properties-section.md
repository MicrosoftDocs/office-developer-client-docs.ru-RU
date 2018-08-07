---
title: Ячейка ScaleX (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60072
localization_priority: Normal
ms.assetid: 5916eadc-37f8-47af-fe54-f6062aea318f
description: Указывает процент увеличения страницы документа на странице принтера.
ms.openlocfilehash: 1713e88f06dc93a2806e64cae3d7af20c9df1fc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814728"
---
# <a name="scalex-cell-print-properties-section"></a><span data-ttu-id="cc701-103">Ячейка ScaleX (раздел "Свойства печати")</span><span class="sxs-lookup"><span data-stu-id="cc701-103">ScaleX Cell (Print Properties Section)</span></span>

<span data-ttu-id="cc701-104">Указывает процент увеличения страницы документа на странице принтера.</span><span class="sxs-lookup"><span data-stu-id="cc701-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cc701-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="cc701-105">Remarks</span></span>

<span data-ttu-id="cc701-106">Это значение используется только в том случае, если значение ячейки OnPage — FALSE.</span><span class="sxs-lookup"><span data-stu-id="cc701-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="cc701-107">Ячейки ScaleX и ScaleY всегда с таким же значением, который соответствует значению в параметре **обеспечить, чтобы** на вкладке **Параметры печати** в диалоговом окне " **Параметры страницы** " (на вкладке " **Конструктор** ", щелкните стрелку **Параметры страницы** ).</span><span class="sxs-lookup"><span data-stu-id="cc701-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="cc701-108">Чтобы получить ссылку на ячейку ScaleX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="cc701-108">To get a reference to the ScaleX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc701-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="cc701-109">Cell name:</span></span>  <br/> |<span data-ttu-id="cc701-110">ScaleX</span><span class="sxs-lookup"><span data-stu-id="cc701-110">ScaleX</span></span>  <br/> |
   
<span data-ttu-id="cc701-111">Для получения ссылки на ячейки ScaleX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="cc701-111">To get a reference to the ScaleX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc701-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="cc701-112">Section index:</span></span>  <br/> |<span data-ttu-id="cc701-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cc701-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="cc701-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="cc701-114">Row index:</span></span>  <br/> |<span data-ttu-id="cc701-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="cc701-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="cc701-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="cc701-116">Cell index:</span></span>  <br/> |<span data-ttu-id="cc701-117">**visPrintPropertiesScaleX**</span><span class="sxs-lookup"><span data-stu-id="cc701-117">**visPrintPropertiesScaleX**</span></span> <br/> |
   

