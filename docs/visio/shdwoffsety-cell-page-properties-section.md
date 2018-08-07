---
title: Ячейка ShdwOffsetY (раздел "Свойства страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm930
localization_priority: Normal
ms.assetid: f3f53a7d-7450-b2b0-b508-6044a87450d9
description: Определяет расстояние смещения тени фигуры по вертикали относительно фигуры в единицах страницы.
ms.openlocfilehash: 0228fef00230dd1517d20067fda855225cef5533
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814850"
---
# <a name="shdwoffsety-cell-page-properties-section"></a><span data-ttu-id="bf402-103">Ячейка ShdwOffsetY (раздел "Свойства страницы")</span><span class="sxs-lookup"><span data-stu-id="bf402-103">ShdwOffsetY Cell (Page Properties Section)</span></span>

<span data-ttu-id="bf402-104">Определяет расстояние смещения тени фигуры по вертикали относительно фигуры в единицах страницы.</span><span class="sxs-lookup"><span data-stu-id="bf402-104">Determines the distance in page units that a shape's drop shadow is offset vertically from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bf402-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="bf402-105">Remarks</span></span>

<span data-ttu-id="bf402-106">Это значение в диалоговом окне " **Параметры страницы** " (на вкладке " **Конструктор** ", щелкните стрелку **Параметры страницы** ).</span><span class="sxs-lookup"><span data-stu-id="bf402-106">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="bf402-107">Это значение не зависит от масштаба документа.</span><span class="sxs-lookup"><span data-stu-id="bf402-107">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="bf402-108">Если документа изменяется, смещение тени остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="bf402-108">If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="bf402-109">Чтобы получить ссылку на ячейку ShdwOffsetY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="bf402-109">To get a reference to the ShdwOffsetY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bf402-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="bf402-110">Cell name:</span></span>  <br/> | <span data-ttu-id="bf402-111">ShdwOffsetY</span><span class="sxs-lookup"><span data-stu-id="bf402-111">ShdwOffsetY</span></span>  <br/> |
   
<span data-ttu-id="bf402-112">Для получения ссылки на ячейки ShdwOffsetY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="bf402-112">To get a reference to the ShdwOffsetY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bf402-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="bf402-113">Section index:</span></span>  <br/> |<span data-ttu-id="bf402-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bf402-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bf402-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="bf402-115">Row index:</span></span>  <br/> |<span data-ttu-id="bf402-116">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="bf402-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="bf402-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="bf402-117">Cell index:</span></span>  <br/> |<span data-ttu-id="bf402-118">**visPageShdwOffsetY**</span><span class="sxs-lookup"><span data-stu-id="bf402-118">**visPageShdwOffsetY**</span></span> <br/> |
   

