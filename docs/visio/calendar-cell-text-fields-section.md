---
title: Ячейка Calendar (раздел "Текстовые поля")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60029
localization_priority: Normal
ms.assetid: 0c3e275e-25f0-3681-03f4-257145c19690
description: Определяет календарь, который используется для текстового поля, когда тип данных даты.
ms.openlocfilehash: 6d9d3ef0addb1d6081e2046ca7a5a663eb2a9c8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813302"
---
# <a name="calendar-cell-text-fields-section"></a><span data-ttu-id="60747-103">Ячейка Calendar (раздел "Текстовые поля")</span><span class="sxs-lookup"><span data-stu-id="60747-103">Calendar Cell (Text Fields Section)</span></span>

<span data-ttu-id="60747-104">Определяет календарь, который используется для текстового поля, когда тип данных даты.</span><span class="sxs-lookup"><span data-stu-id="60747-104">Determines the calendar that is used for a text field when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="60747-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="60747-105">Remarks</span></span>

<span data-ttu-id="60747-106">Возможные значения: 0 (западное), 1 (арабский хиджра), 2 (Еврейский лунный), 3 (тайваньский), 4 (японский Мэйдзи Reign), 5 (тайский), 6 (корейский Danki), 7 (эра Сака), (транслитерированный английский) 8 и 9 (Транслитерированный французский).</span><span class="sxs-lookup"><span data-stu-id="60747-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="60747-107">Для получения ссылки на ячейки календаря по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="60747-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="60747-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="60747-108">Cell name:</span></span>  <br/> | <span data-ttu-id="60747-109">Fields.Calendar [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="60747-109">Fields.Calendar[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="60747-110">Для получения ссылки на ячейки календаря по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="60747-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="60747-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="60747-111">Section index:</span></span>  <br/> |<span data-ttu-id="60747-112">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="60747-112">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="60747-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="60747-113">Row index:</span></span>  <br/> |<span data-ttu-id="60747-114">**visRowField** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="60747-114">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="60747-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="60747-115">Cell index:</span></span>  <br/> |<span data-ttu-id="60747-116">**visFieldCalendar**</span><span class="sxs-lookup"><span data-stu-id="60747-116">**visFieldCalendar**</span></span> <br/> |
   

