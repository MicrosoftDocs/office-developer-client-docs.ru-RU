---
title: DefaultTabstop Cell (Text Block Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm220
localization_priority: Normal
ms.assetid: 3b3e458a-206c-8699-8bf7-da80f4350706
description: Определяет интервал по умолчанию для табуляции в текстовом блоке.
ms.openlocfilehash: 1ae923f6373b9cee76238b1fb27ec5eb3acb43ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360272"
---
# <a name="defaulttabstop-cell-text-block-format-section"></a><span data-ttu-id="a5c81-103">DefaultTabstop Cell (Text Block Format Section)</span><span class="sxs-lookup"><span data-stu-id="a5c81-103">DefaultTabstop Cell (Text Block Format Section)</span></span>

<span data-ttu-id="a5c81-104">Определяет интервал по умолчанию для табуляции в текстовом блоке.</span><span class="sxs-lookup"><span data-stu-id="a5c81-104">Determines the interval of the default tab stops in a text block.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a5c81-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="a5c81-105">Remarks</span></span>

<span data-ttu-id="a5c81-106">Значение по умолчанию — 0,5 дюйма для документов, созданных в Империал единицах, и 1,5 сантиметра для документов, созданных в метрических единицах.</span><span class="sxs-lookup"><span data-stu-id="a5c81-106">The default value is 0.5 inches for documents created in imperial units and 1.5 centimeters for documents created in metric units.</span></span>
  
<span data-ttu-id="a5c81-107">Чтобы получить ссылку на ячейку DefaultTabstop по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="a5c81-107">To get a reference to the DefaultTabstop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a5c81-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="a5c81-108">Cell name:</span></span>  <br/> |<span data-ttu-id="a5c81-109">DefaultTabstop</span><span class="sxs-lookup"><span data-stu-id="a5c81-109">DefaultTabstop</span></span>  <br/> |
   
<span data-ttu-id="a5c81-110">Чтобы получить ссылку на ячейку DefaultTabstop по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="a5c81-110">To get a reference to the DefaultTabstop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a5c81-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a5c81-111">Section index:</span></span>  <br/> |<span data-ttu-id="a5c81-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a5c81-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a5c81-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a5c81-113">Row index:</span></span>  <br/> |<span data-ttu-id="a5c81-114">**Висровтекст**</span><span class="sxs-lookup"><span data-stu-id="a5c81-114">**visRowText**</span></span> <br/> |
|<span data-ttu-id="a5c81-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a5c81-115">Cell index:</span></span>  <br/> |<span data-ttu-id="a5c81-116">**Висткстблкдефаулттабстоп**</span><span class="sxs-lookup"><span data-stu-id="a5c81-116">**visTxtBlkDefaultTabStop**</span></span> <br/> |
   

