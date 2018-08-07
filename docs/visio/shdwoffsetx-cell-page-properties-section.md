---
title: Ячейка ShdwOffsetX (раздел "Свойства страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251373
localization_priority: Normal
ms.assetid: 92ec9b11-f53f-a1c9-832a-6cac08aa5379
description: Определяет расстояние смещения тени фигуры по горизонтали относительно фигуры в единицах страницы.
ms.openlocfilehash: 9aec108146e329d7a8161acc4ca7cdcb19424eff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814833"
---
# <a name="shdwoffsetx-cell-page-properties-section"></a><span data-ttu-id="6a53c-103">Ячейка ShdwOffsetX (раздел "Свойства страницы")</span><span class="sxs-lookup"><span data-stu-id="6a53c-103">ShdwOffsetX Cell (Page Properties Section)</span></span>

<span data-ttu-id="6a53c-104">Определяет расстояние смещения тени фигуры по горизонтали относительно фигуры в единицах страницы.</span><span class="sxs-lookup"><span data-stu-id="6a53c-104">Determines the distance in page units that a shape's drop shadow is offset horizontally from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6a53c-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="6a53c-105">Remarks</span></span>

<span data-ttu-id="6a53c-106">Это значение в диалоговом окне " **Параметры страницы** " (на вкладке " **Конструктор** ", щелкните стрелку **Параметры страницы** ).</span><span class="sxs-lookup"><span data-stu-id="6a53c-106">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="6a53c-107">Это значение не зависит от масштаба документа.</span><span class="sxs-lookup"><span data-stu-id="6a53c-107">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="6a53c-108">Если документа изменяется, смещение тени остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="6a53c-108">If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="6a53c-109">Чтобы получить ссылку на ячейку ShdwOffsetX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="6a53c-109">To get a reference to the ShdwOffsetX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6a53c-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="6a53c-110">Cell name:</span></span>  <br/> | <span data-ttu-id="6a53c-111">ShdwOffsetX</span><span class="sxs-lookup"><span data-stu-id="6a53c-111">ShdwOffsetX</span></span>  <br/> |
   
<span data-ttu-id="6a53c-112">Для получения ссылки на ячейки ShdwOffsetX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="6a53c-112">To get a reference to the ShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6a53c-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="6a53c-113">Section index:</span></span>  <br/> |<span data-ttu-id="6a53c-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6a53c-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6a53c-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="6a53c-115">Row index:</span></span>  <br/> |<span data-ttu-id="6a53c-116">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="6a53c-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="6a53c-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="6a53c-117">Cell index:</span></span>  <br/> |<span data-ttu-id="6a53c-118">**visPageShdwOffsetX**</span><span class="sxs-lookup"><span data-stu-id="6a53c-118">**visPageShdwOffsetX**</span></span> <br/> |
   

