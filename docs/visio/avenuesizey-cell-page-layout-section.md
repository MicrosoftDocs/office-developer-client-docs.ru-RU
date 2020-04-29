---
title: AvenueSizeY Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm70
localization_priority: Normal
ms.assetid: 9ff2893c-afe5-505e-0b55-48ec1de08a5f
description: Определяет интервал по вертикали между фигурами на странице документа при размещении фигур с помощью диалогового окна "Настройка макета" (на вкладке Конструктор в группе Макет выберите пункт изменить макет страницы, а затем щелкните Дополнительные параметры макета).
ms.openlocfilehash: 283de8925e34c470fd1f9e78b8ae58882be8b7fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420208"
---
# <a name="avenuesizey-cell-page-layout-section"></a><span data-ttu-id="500ad-103">AvenueSizeY Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="500ad-103">AvenueSizeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="500ad-104">Определяет интервал по вертикали между фигурами на странице документа при размещении фигур с помощью диалогового окна " **Настройка макета** " (на вкладке **конструктор** в группе **Макет** выберите пункт **изменить** макет страницы, а затем щелкните **Дополнительные параметры макета**).</span><span class="sxs-lookup"><span data-stu-id="500ad-104">Determines the amount of vertical space between shapes on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout** Page, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="500ad-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="500ad-105">Remarks</span></span>

<span data-ttu-id="500ad-106">Вы также можете задать это значение в диалоговом окне **Макет и интервалы маршрутизации** (на вкладке **конструктор** щелкните стрелку в группе **Параметры страницы** , перейдите на вкладку **Макет и маршрутизация** , а затем выберите **интервал**).</span><span class="sxs-lookup"><span data-stu-id="500ad-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="500ad-107">Динамическая сетка использует параметр в ячейке AvenueSizeY, когда доступна только одна фигура для вычисления вертикального интервала.</span><span class="sxs-lookup"><span data-stu-id="500ad-107">The dynamic grid uses the setting in the AvenueSizeY cell when only one shape is available for calculating vertical spacing.</span></span> <span data-ttu-id="500ad-108">Чтобы использовать динамическую сетку, на вкладке **вид** в группе **визуальные подсказки** выберите **Динамическая сетка**.</span><span class="sxs-lookup"><span data-stu-id="500ad-108">To use the dynamic grid, on the **View** tab, in the **Visual Aids** group, select **Dynamic Grid**.</span></span>
  
<span data-ttu-id="500ad-109">Чтобы получить ссылку на ячейку AvenueSizeY по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="500ad-109">To get a reference to the AvenueSizeY cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="500ad-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="500ad-110">Cell name:</span></span>  <br/> | <span data-ttu-id="500ad-111">AvenueSizeY</span><span class="sxs-lookup"><span data-stu-id="500ad-111">AvenueSizeY</span></span>  <br/> |
   
<span data-ttu-id="500ad-112">Чтобы получить ссылку на ячейку AvenueSizeY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="500ad-112">To get a reference to the AvenueSizeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="500ad-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="500ad-113">Section index:</span></span>  <br/> |<span data-ttu-id="500ad-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="500ad-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="500ad-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="500ad-115">Row index:</span></span>  <br/> |<span data-ttu-id="500ad-116">**висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="500ad-116">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="500ad-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="500ad-117">Cell index:</span></span>  <br/> |<span data-ttu-id="500ad-118">**висплоавенуесизэй**</span><span class="sxs-lookup"><span data-stu-id="500ad-118">**visPLOAvenueSizeY**</span></span> <br/> |
   

