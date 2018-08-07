---
title: Ячейка BulletFont (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60023
localization_priority: Normal
ms.assetid: a75ff1f3-2f4d-89e3-108b-e16a34f5184f
description: Представляет номер шрифта, используемого для форматирования текста, когда указана строка пользовательского маркера и значение в ячейке маркера больше нуля.
ms.openlocfilehash: 7cd3333afc30d30ea7b0e5d35650681074744235
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813327"
---
# <a name="bulletfont-cell-paragraph-section"></a><span data-ttu-id="9e60f-103">Ячейка BulletFont (раздел "Абзац")</span><span class="sxs-lookup"><span data-stu-id="9e60f-103">BulletFont Cell (Paragraph Section)</span></span>

<span data-ttu-id="9e60f-104">Представляет номер шрифта, используемого для форматирования текста, когда указана строка пользовательского маркера и значение в ячейке маркера больше нуля.</span><span class="sxs-lookup"><span data-stu-id="9e60f-104">Represents the number of the font used to format the text when a custom bullet string is specified and the value in the Bullet cell is non-zero.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9e60f-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="9e60f-105">Remarks</span></span>

<span data-ttu-id="9e60f-106">Номера шрифтов зависят шрифты, установленные в системе.</span><span class="sxs-lookup"><span data-stu-id="9e60f-106">Font numbers vary according to the fonts installed on your system.</span></span> <span data-ttu-id="9e60f-107">Если значение равно 0, а строка пользовательского маркера, шрифт, используемый совпадает с шрифт первого знака абзаца.</span><span class="sxs-lookup"><span data-stu-id="9e60f-107">If the value is 0 and there is a custom bullet string, the font used is the same as the font of the first character of the paragraph.</span></span>
  
<span data-ttu-id="9e60f-108">Чтобы получить ссылку на ячейку BulletFont по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="9e60f-108">To get a reference to the BulletFont cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9e60f-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="9e60f-109">Cell name:</span></span>  <br/> | <span data-ttu-id="9e60f-110">Para.BulletFont [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="9e60f-110">Para.BulletFont[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="9e60f-111">Для получения ссылки на ячейки BulletFont по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="9e60f-111">To get a reference to the BulletFont cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9e60f-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="9e60f-112">Section index:</span></span>  <br/> |<span data-ttu-id="9e60f-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="9e60f-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="9e60f-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="9e60f-114">Row index:</span></span>  <br/> |<span data-ttu-id="9e60f-115">**visRowParagraph** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9e60f-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9e60f-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="9e60f-116">Cell index:</span></span>  <br/> |<span data-ttu-id="9e60f-117">**visBulletFont**</span><span class="sxs-lookup"><span data-stu-id="9e60f-117">**visBulletFont**</span></span> <br/> |
   

