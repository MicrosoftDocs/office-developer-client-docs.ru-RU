---
title: Ячейка ShdwForegnd (раздел "Формат заливки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251244
localization_priority: Normal
ms.assetid: ea153390-631d-79fd-c1ba-4c281239a24e
description: Определяет цвет, используемый для переднего плана (числу штрихов) узора заливки тени фигуры.
ms.openlocfilehash: f39109a296949d23142017661bb55f0708402d8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814839"
---
# <a name="shdwforegnd-cell-fill-format-section"></a><span data-ttu-id="158a0-103">Ячейка ShdwForegnd (раздел "Формат заливки")</span><span class="sxs-lookup"><span data-stu-id="158a0-103">ShdwForegnd Cell (Fill Format Section)</span></span>

<span data-ttu-id="158a0-104">Определяет цвет, используемый для переднего плана (числу штрихов) узора заливки тени фигуры.</span><span class="sxs-lookup"><span data-stu-id="158a0-104">Determines the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="158a0-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="158a0-105">Remarks</span></span>

<span data-ttu-id="158a0-106">Для настройки цвета, введите число от 0 до 23, которая является индексом в коллекции цветов.</span><span class="sxs-lookup"><span data-stu-id="158a0-106">To set the color, enter a number from 0 to 23, which is an index into a collection of colors.</span></span>
  
<span data-ttu-id="158a0-107">Чтобы ввести другой цвет, используйте функцию RGB или HSL.</span><span class="sxs-lookup"><span data-stu-id="158a0-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="158a0-108">Настраиваемые цвета значение цвета RGB, а RGB ( *r, g, b*), а не числа, будут отображаться в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="158a0-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="158a0-109">При использовании в операции, настраиваемые цвета имеют значения из 24 и выше.</span><span class="sxs-lookup"><span data-stu-id="158a0-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="158a0-110">В ячейке ShdwForegndTrans можно задать прозрачность цвет переднего плана узора заливки тени фигуры.</span><span class="sxs-lookup"><span data-stu-id="158a0-110">You can set the transparency of the foreground color of the shape's drop shadow fill pattern in the ShdwForegndTrans cell.</span></span>
  
<span data-ttu-id="158a0-111">Чтобы получить ссылку на ячейку ShdwForegnd по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="158a0-111">To get a reference to the ShdwForegnd cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="158a0-112">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="158a0-112">Cell name:</span></span>  <br/> | <span data-ttu-id="158a0-113">ShdwForegnd</span><span class="sxs-lookup"><span data-stu-id="158a0-113">ShdwForegnd</span></span>  <br/> |
   
<span data-ttu-id="158a0-114">Для получения ссылки на ячейки ShdwForegnd по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="158a0-114">To get a reference to the ShdwForegnd cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="158a0-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="158a0-115">Section index:</span></span>  <br/> |<span data-ttu-id="158a0-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="158a0-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="158a0-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="158a0-117">Row index:</span></span>  <br/> |<span data-ttu-id="158a0-118">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="158a0-118">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="158a0-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="158a0-119">Cell index:</span></span>  <br/> |<span data-ttu-id="158a0-120">**visFillShdwForegnd**</span><span class="sxs-lookup"><span data-stu-id="158a0-120">**visFillShdwForegnd**</span></span> <br/> |
   

