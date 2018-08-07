---
title: Ячейка ShdwForegndTrans (раздел "Формат заливки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253253
localization_priority: Normal
ms.assetid: c42d4d2e-f8f0-bc5b-6018-4bb4ffa81b64
description: Определяет уровень прозрачности цвета, используемого для переднего плана (числу штрихов) узора заливки тени фигуры.
ms.openlocfilehash: 5fd385fc2f46f1ff8eedc961833813ec16ba7b73
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814825"
---
# <a name="shdwforegndtrans-cell-fill-format-section"></a><span data-ttu-id="8536f-103">Ячейка ShdwForegndTrans (раздел "Формат заливки")</span><span class="sxs-lookup"><span data-stu-id="8536f-103">ShdwForegndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="8536f-104">Определяет уровень прозрачности цвета, используемого для переднего плана (числу штрихов) узора заливки тени фигуры.</span><span class="sxs-lookup"><span data-stu-id="8536f-104">Determines the transparency level for the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
|<span data-ttu-id="8536f-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="8536f-105">**Value**</span></span>|<span data-ttu-id="8536f-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8536f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8536f-107">0 — 100</span><span class="sxs-lookup"><span data-stu-id="8536f-107">0 - 100</span></span>  <br/> |<span data-ttu-id="8536f-108">Представляет собой процентную долю прозрачность.</span><span class="sxs-lookup"><span data-stu-id="8536f-108">Represents the percentage of transparency.</span></span> <span data-ttu-id="8536f-109">Значение по умолчанию — 0% (полностью непрозрачный).</span><span class="sxs-lookup"><span data-stu-id="8536f-109">The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8536f-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="8536f-110">Remarks</span></span>

<span data-ttu-id="8536f-111">Значения округляются до ближайшего большего половины процентов.</span><span class="sxs-lookup"><span data-stu-id="8536f-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="8536f-112">Значение 100% является полностью прозрачным.</span><span class="sxs-lookup"><span data-stu-id="8536f-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="8536f-113">Несмотря на то, что тени, полностью прозрачной заливкой отображается на странице документа как тени, без заливки, взаимодействия с других объектов на странице же образом как если бы его прозрачность 0%.</span><span class="sxs-lookup"><span data-stu-id="8536f-113">Although a shadow that has a completely transparent fill appears the same on the drawing page as a shadow that has no fill, it interacts with other objects on the page in the same ways as if its transparency were 0%.</span></span>
  
<span data-ttu-id="8536f-114">Также можно задать это значение с помощью элемента управления ползунок в диалоговом окне **теневой** (на вкладке **Главная** в группе **фигуру** нажмите кнопку **тень**и нажмите кнопку **Параметры тени**).</span><span class="sxs-lookup"><span data-stu-id="8536f-114">You can also set this value by using the slider control in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span> <span data-ttu-id="8536f-115">Это значение определяет значение теневой прозрачность переднего плана и фона.</span><span class="sxs-lookup"><span data-stu-id="8536f-115">This value controls the value of both the background and foreground shadow transparencies.</span></span> <span data-ttu-id="8536f-116">Чтобы задать эти значения независимо друг от друга, необходимо ввести их в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="8536f-116">To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="8536f-117">Чтобы получить ссылку на ячейку ShdwForegndTrans по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="8536f-117">To get a reference to the ShdwForegndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8536f-118">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="8536f-118">Cell name:</span></span>  <br/> |<span data-ttu-id="8536f-119">ShdwForegndTrans</span><span class="sxs-lookup"><span data-stu-id="8536f-119">ShdwForegndTrans</span></span>  <br/> |
   
<span data-ttu-id="8536f-120">Для получения ссылки на ячейки ShdwForegndTrans по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="8536f-120">To get a reference to the ShdwForegndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8536f-121">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8536f-121">Section index:</span></span>  <br/> |<span data-ttu-id="8536f-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8536f-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8536f-123">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8536f-123">Row index:</span></span>  <br/> |<span data-ttu-id="8536f-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="8536f-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="8536f-125">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8536f-125">Cell index:</span></span>  <br/> |<span data-ttu-id="8536f-126">**visFillShdwForegndTrans**</span><span class="sxs-lookup"><span data-stu-id="8536f-126">**visFillShdwForegndTrans**</span></span> <br/> |
   

