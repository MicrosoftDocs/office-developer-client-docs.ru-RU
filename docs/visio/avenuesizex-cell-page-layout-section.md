---
title: Ячейка AvenueSizeX (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm65
localization_priority: Normal
ms.assetid: 86fe25ed-590d-b2f0-5dfe-9746a19c6b04
description: Определяет горизонтальную расстояние между фигурами на странице документа при расположении фигур с помощью диалогового окна "Настройка макета" (на вкладке конструктор в группе макет нажмите кнопку Изменить расположение и нажмите кнопку Дополнительные параметры расположения).
ms.openlocfilehash: efb29181414957063e038b97c2d7b79720aa0405
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813183"
---
# <a name="avenuesizex-cell-page-layout-section"></a><span data-ttu-id="34075-103">Ячейка AvenueSizeX (раздел "Макет страницы")</span><span class="sxs-lookup"><span data-stu-id="34075-103">AvenueSizeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="34075-104">Определяет горизонтальную расстояние между фигурами на странице документа при расположении фигур с помощью диалогового окна " **Настройка макета** " (на вкладке **Конструктор** в группе **Макет** нажмите кнопку **Изменить расположение**и нажмите кнопку ** более Параметры расположения **).</span><span class="sxs-lookup"><span data-stu-id="34075-104">Determines the amount of horizontal space between shapes on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click ** More Layout Options **).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="34075-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="34075-105">Remarks</span></span>

<span data-ttu-id="34075-106">Также можно задать это значение в диалоговом окне **Макет и маршрутизация интервалы** (на вкладку **Конструктор** , щелкните стрелку в группе **Параметры страницы** , перейдите на вкладку **Макет и маршрутизации** и нажмите кнопку **интервала**).</span><span class="sxs-lookup"><span data-stu-id="34075-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="34075-107">Динамические сетки используется в ячейке AvenueSizeX Если доступен только один фигуры для расчета интервал по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="34075-107">The dynamic grid uses the setting in the AvenueSizeX cell when only one shape is available for calculating horizontal spacing.</span></span> <span data-ttu-id="34075-108">Использование динамических сетки на вкладке **Вид** в группе **Вспомогательные элементы** выберите **Динамических сетки**.</span><span class="sxs-lookup"><span data-stu-id="34075-108">To use the dynamic grid, on the **View** tab, in the **Visual Aids** group, select **Dynamic Grid**.</span></span>
  
<span data-ttu-id="34075-109">Чтобы получить ссылку на ячейку AvenueSizeX по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="34075-109">To get a reference to the AvenueSizeX cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="34075-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="34075-110">Cell name:</span></span>  <br/> | <span data-ttu-id="34075-111">AvenueSizeY</span><span class="sxs-lookup"><span data-stu-id="34075-111">AvenueSizeY</span></span>  <br/> |
   
<span data-ttu-id="34075-112">Для получения ссылки на ячейки AvenueSizeX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="34075-112">To get a reference to the AvenueSizeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="34075-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="34075-113">Section index:</span></span>  <br/> |<span data-ttu-id="34075-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="34075-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="34075-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="34075-115">Row index:</span></span>  <br/> |<span data-ttu-id="34075-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="34075-116">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="34075-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="34075-117">Cell index:</span></span>  <br/> |<span data-ttu-id="34075-118">**visPLOAvenueSizeX**</span><span class="sxs-lookup"><span data-stu-id="34075-118">**visPLOAvenueSizeX**</span></span> <br/> |
   

