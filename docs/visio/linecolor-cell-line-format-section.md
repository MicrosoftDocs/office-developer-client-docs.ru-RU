---
title: Ячейка LineColor (раздел "Формат линий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm535
localization_priority: Normal
ms.assetid: d857b48b-9a3d-a1e1-5ad2-6816a492c8ab
description: Определяет цвет линии фигуры.
ms.openlocfilehash: 6086a45108b88475e250c4d833ab4b740f33b8e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814082"
---
# <a name="linecolor-cell-line-format-section"></a><span data-ttu-id="b14db-103">Ячейка LineColor (раздел "Формат линий")</span><span class="sxs-lookup"><span data-stu-id="b14db-103">LineColor Cell (Line Format Section)</span></span>

<span data-ttu-id="b14db-104">Определяет цвет линии фигуры.</span><span class="sxs-lookup"><span data-stu-id="b14db-104">Determines the line color of the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b14db-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="b14db-105">Remarks</span></span>

<span data-ttu-id="b14db-106">Чтобы задать цвет линии, введите число от 0 до 23, которого является индексом в коллекцию цвета строк.</span><span class="sxs-lookup"><span data-stu-id="b14db-106">To set the line color, enter a number from 0 to 23, which is an index into a collection of line colors.</span></span> <span data-ttu-id="b14db-107">Можно просмотреть семейства цвет строки в поле **строка** (на вкладке **Главная** в группе **фигуры** щелкните **строку**, выберите пункт **Вес**и нажмите кнопку **Другие линии**).</span><span class="sxs-lookup"><span data-stu-id="b14db-107">You can view the line color collection in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span> <span data-ttu-id="b14db-108">Также можно задать значение цвет линии в диалоговом окне **строки** .</span><span class="sxs-lookup"><span data-stu-id="b14db-108">You can also set the value of LineColor in the **Line** dialog box.</span></span> 
  
<span data-ttu-id="b14db-109">Чтобы ввести другой цвет, используйте функцию RGB или HSL.</span><span class="sxs-lookup"><span data-stu-id="b14db-109">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="b14db-110">Настраиваемые цвета значение цвета RGB, а RGB ( *r, g, b*), а не числа, будут отображаться в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="b14db-110">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="b14db-111">При использовании в операции, настраиваемые цвета имеют значения из 24 и выше.</span><span class="sxs-lookup"><span data-stu-id="b14db-111">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="b14db-112">Можно задать прозрачность цвета строки в ячейке LineColorTrans.</span><span class="sxs-lookup"><span data-stu-id="b14db-112">You can set the transparency of the line color in the LineColorTrans cell.</span></span>
  
<span data-ttu-id="b14db-113">Чтобы получить ссылку на ячейку цвет линии по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="b14db-113">To get a reference to the LineColor cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b14db-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="b14db-114">Cell name:</span></span>  <br/> |<span data-ttu-id="b14db-115">Цвет линии</span><span class="sxs-lookup"><span data-stu-id="b14db-115">LineColor</span></span>  <br/> |
   
<span data-ttu-id="b14db-116">Для получения ссылки на ячейки цвет линии по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="b14db-116">To get a reference to the LineColor cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b14db-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b14db-117">Section index:</span></span>  <br/> |<span data-ttu-id="b14db-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b14db-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b14db-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b14db-119">Row index:</span></span>  <br/> |<span data-ttu-id="b14db-120">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="b14db-120">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="b14db-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b14db-121">Cell index:</span></span>  <br/> |<span data-ttu-id="b14db-122">**visLineColor**</span><span class="sxs-lookup"><span data-stu-id="b14db-122">**visLineColor**</span></span> <br/> |
   

