---
title: Ячейка PaperSource (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60068
localization_priority: Normal
ms.assetid: 771a2ab4-578d-51c3-fabd-138f7952bb11
description: Определяет источник бумаги для страницы.
ms.openlocfilehash: f1dedf210dfe0dd8cac3d36fdec03fb497f6572c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814347"
---
# <a name="papersource-cell-printproperties-section"></a><span data-ttu-id="e33a5-103">Ячейка PaperSource (раздел "Свойства печати")</span><span class="sxs-lookup"><span data-stu-id="e33a5-103">PaperSource Cell (PrintProperties Section)</span></span>

<span data-ttu-id="e33a5-104">Определяет источник бумаги для страницы.</span><span class="sxs-lookup"><span data-stu-id="e33a5-104">Determines the paper source for the page.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e33a5-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="e33a5-105">Remarks</span></span>

<span data-ttu-id="e33a5-106">Этот параметр соответствует параметру **Источник бумаги** в диалоговом окне " **Настройка печати** " (на вкладке " **Конструктор** ", нажмите стрелку **Параметры страницы** и нажмите кнопку **программы установки**на вкладке **Настройка печати** ).</span><span class="sxs-lookup"><span data-stu-id="e33a5-106">This setting corresponds to the **Paper Source** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click **Setup**).</span></span>
  
<span data-ttu-id="e33a5-107">Числовые значения в с помощью этой карты ячейки для константы (с DMBIN префиксом), заданных для ячейки выбранные элементы в файле wingdi.h Microsoft Windows; Например DMBIN_AUTO представляет значение 7.</span><span class="sxs-lookup"><span data-stu-id="e33a5-107">The numeric values in this cell map to constants (prefixed with DMBIN) defined for bin selections in the Microsoft Windows wingdi.h file; for example, the value 7 represents DMBIN_AUTO.</span></span> 
  
<span data-ttu-id="e33a5-108">Чтобы получить ссылку на ячейку PaperSource по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e33a5-108">To get a reference to the PaperSource cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e33a5-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="e33a5-109">Cell name:</span></span>  <br/> |<span data-ttu-id="e33a5-110">PaperSource</span><span class="sxs-lookup"><span data-stu-id="e33a5-110">PaperSource</span></span>  <br/> |
   
<span data-ttu-id="e33a5-111">Для получения ссылки на ячейки PaperSource по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="e33a5-111">To get a reference to the PaperSource cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e33a5-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e33a5-112">Section index:</span></span>  <br/> |<span data-ttu-id="e33a5-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e33a5-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e33a5-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e33a5-114">Row index:</span></span>  <br/> |<span data-ttu-id="e33a5-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="e33a5-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="e33a5-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e33a5-116">Cell index:</span></span>  <br/> |<span data-ttu-id="e33a5-117">**visPrintPropertiesPaperSource**</span><span class="sxs-lookup"><span data-stu-id="e33a5-117">**visPrintPropertiesPaperSource**</span></span> <br/> |
   

