---
title: Ячейка Value (раздел "Текстовые поля")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1095
localization_priority: Normal
ms.assetid: 3ca662c8-1ce4-89a9-3264-1ba533fcd444
description: Содержит функции для поля.
ms.openlocfilehash: 9bce4cbb1b3955f749cefa18130c6b01fe61244e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815126"
---
# <a name="value-cell-text-fields-section"></a><span data-ttu-id="cc90e-103">Ячейка Value (раздел "Текстовые поля")</span><span class="sxs-lookup"><span data-stu-id="cc90e-103">Value Cell (Text Fields Section)</span></span>

<span data-ttu-id="cc90e-104">Содержит функции для поля.</span><span class="sxs-lookup"><span data-stu-id="cc90e-104">Contains the function for a field.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cc90e-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="cc90e-105">Remarks</span></span>

<span data-ttu-id="cc90e-106">Можно задать значение ячейки с помощью диалогового окна **поля** (на вкладке **Вставка** в группе **текст** щелкните **поле**).</span><span class="sxs-lookup"><span data-stu-id="cc90e-106">You can set the value of this cell using the **Field** dialog box (on the **Insert** tab, in the **Text** group, click **Field**).</span></span>
  
<span data-ttu-id="cc90e-107">Чтобы получить ссылку на значение ячейки по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="cc90e-107">To get a reference to the Value cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc90e-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="cc90e-108">Cell name:</span></span>  <br/> |<span data-ttu-id="cc90e-109">Fields.Value [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="cc90e-109">Fields.Value[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="cc90e-110">Для получения ссылки на ячейки значение по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="cc90e-110">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc90e-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="cc90e-111">Section index:</span></span>  <br/> |<span data-ttu-id="cc90e-112">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="cc90e-112">**visSectionTextField**</span></span> <br/> |
|<span data-ttu-id="cc90e-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="cc90e-113">Row index:</span></span>  <br/> |<span data-ttu-id="cc90e-114">**visRowField** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="cc90e-114">**visRowField** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="cc90e-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="cc90e-115">Cell index:</span></span>  <br/> |<span data-ttu-id="cc90e-116">**visFieldCell**</span><span class="sxs-lookup"><span data-stu-id="cc90e-116">**visFieldCell**</span></span> <br/> |
   

