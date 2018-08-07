---
title: Ячейка LineColorTrans (раздел "Формат линий")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50120
localization_priority: Normal
ms.assetid: b68054b5-7efd-1156-9dc1-5ec94e18d227
description: Определяет уровень прозрачности цвета линии фигуры.
ms.openlocfilehash: 81c23b77c4663158819f9d5fe53765860183e039
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814079"
---
# <a name="linecolortrans-cell-line-format-section"></a><span data-ttu-id="975a6-103">Ячейка LineColorTrans (раздел "Формат линий")</span><span class="sxs-lookup"><span data-stu-id="975a6-103">LineColorTrans Cell (Line Format Section)</span></span>

<span data-ttu-id="975a6-104">Определяет уровень прозрачности цвета линии фигуры.</span><span class="sxs-lookup"><span data-stu-id="975a6-104">Determines the transparency level of a shape's line color.</span></span>
  
|<span data-ttu-id="975a6-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="975a6-105">**Value**</span></span>|<span data-ttu-id="975a6-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="975a6-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="975a6-107">0 — 100</span><span class="sxs-lookup"><span data-stu-id="975a6-107">0 - 100</span></span>  <br/> |<span data-ttu-id="975a6-108">Представляет собой процентную долю прозрачность.</span><span class="sxs-lookup"><span data-stu-id="975a6-108">Represents the percentage of transparency.</span></span> <span data-ttu-id="975a6-109">Значение по умолчанию — 0% (полностью непрозрачный).</span><span class="sxs-lookup"><span data-stu-id="975a6-109">The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="975a6-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="975a6-110">Remarks</span></span>

<span data-ttu-id="975a6-111">Значения округляются до ближайшего большего половины процентов.</span><span class="sxs-lookup"><span data-stu-id="975a6-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="975a6-112">Значение 100% является полностью прозрачным.</span><span class="sxs-lookup"><span data-stu-id="975a6-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="975a6-113">Несмотря на то, что фигуры с цветом полностью прозрачным строки отображается же, как фигуры, без строк на странице документа, он будет взаимодействовать с другими объектами на странице же образом как в случае его прозрачность 0%.</span><span class="sxs-lookup"><span data-stu-id="975a6-113">Although a shape with a completely transparent line color appears the same as a shape with no lines on the drawing page, it will interact with other objects on the page in the same ways as if its transparency is 0%.</span></span> 
  
<span data-ttu-id="975a6-114">Также можно задать это значение с помощью элемента управления ползунок в диалоговом окне " **строка** " (на вкладке **Главная** в группе **фигуры** щелкните **строку**, выберите пункт **Вес**и нажмите кнопку **Другие линии**).</span><span class="sxs-lookup"><span data-stu-id="975a6-114">You can also set this value by using the slider control in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="975a6-115">Чтобы получить ссылку на ячейку LineColorTrans по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="975a6-115">To get a reference to the LineColorTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="975a6-116">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="975a6-116">Cell name:</span></span>  <br/> |<span data-ttu-id="975a6-117">LineColorTrans</span><span class="sxs-lookup"><span data-stu-id="975a6-117">LineColorTrans</span></span>  <br/> |
   
<span data-ttu-id="975a6-118">Для получения ссылки на ячейки LineColorTrans по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="975a6-118">To get a reference to the LineColorTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="975a6-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="975a6-119">Section index:</span></span>  <br/> |<span data-ttu-id="975a6-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="975a6-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="975a6-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="975a6-121">Row index:</span></span>  <br/> |<span data-ttu-id="975a6-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="975a6-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="975a6-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="975a6-123">Cell index:</span></span>  <br/> |<span data-ttu-id="975a6-124">**visLineColorTrans**</span><span class="sxs-lookup"><span data-stu-id="975a6-124">**visLineColorTrans**</span></span> <br/> |
   

