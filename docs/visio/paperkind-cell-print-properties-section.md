---
title: Ячейка PaperKind (раздел "Свойства печати")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60067
localization_priority: Normal
ms.assetid: b2c9616f-a144-eb99-54b6-b53745c7b4d6
description: Указывает тип бумаги для печати на странице.
ms.openlocfilehash: 03659553ab32afd20d1a5a40b85a8bbf107dbb08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814351"
---
# <a name="paperkind-cell-print-properties-section"></a><span data-ttu-id="1fac6-103">Ячейка PaperKind (раздел "Свойства печати")</span><span class="sxs-lookup"><span data-stu-id="1fac6-103">PaperKind Cell (Print Properties Section)</span></span>

<span data-ttu-id="1fac6-104">Указывает тип бумаги для печати на странице.</span><span class="sxs-lookup"><span data-stu-id="1fac6-104">Specifies the type of paper on which to print the page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1fac6-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="1fac6-105">Remarks</span></span>

<span data-ttu-id="1fac6-106">Этот параметр соответствует параметру **Размер бумаги** в диалоговом окне " **Настройка печати** " (на вкладке " **Конструктор** ", щелкните стрелку **Параметры страницы** и на вкладке **Настройка печати** нажмите кнопку **программы установки** ).</span><span class="sxs-lookup"><span data-stu-id="1fac6-106">This setting corresponds to the **Paper Size** setting in the **Print Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then on the **Print Setup** tab, click the **Setup** button).</span></span> 
  
<span data-ttu-id="1fac6-107">Числовые значения в этой ячейке сопоставить с константы (с DMPAPER префиксом), определенных для выбранных элементов документ в файле wingdi.h Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1fac6-107">The numeric values in this cell map to constants (prefixed with DMPAPER) defined for paper selections in the Microsoft Windows wingdi.h file.</span></span> 
  
<span data-ttu-id="1fac6-108">Чтобы получить ссылку на ячейку PaperKind по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="1fac6-108">To get a reference to the PaperKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1fac6-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="1fac6-109">Cell name:</span></span>  <br/> |<span data-ttu-id="1fac6-110">PaperKind</span><span class="sxs-lookup"><span data-stu-id="1fac6-110">PaperKind</span></span>  <br/> |
   
<span data-ttu-id="1fac6-111">Для получения ссылки на ячейки PaperKind по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="1fac6-111">To get a reference to the PaperKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1fac6-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="1fac6-112">Section index:</span></span>  <br/> |<span data-ttu-id="1fac6-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1fac6-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1fac6-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="1fac6-114">Row index:</span></span>  <br/> |<span data-ttu-id="1fac6-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="1fac6-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="1fac6-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="1fac6-116">Cell index:</span></span>  <br/> |<span data-ttu-id="1fac6-117">**visPrintPropertiesPaperKind**</span><span class="sxs-lookup"><span data-stu-id="1fac6-117">**visPrintPropertiesPaperKind**</span></span> <br/> |
   

