---
title: Ячейка AvenueSizeY (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm70
localization_priority: Normal
ms.assetid: 9ff2893c-afe5-505e-0b55-48ec1de08a5f
description: Определяет интервал по вертикали между фигурами на странице документа при расположении фигур с помощью диалогового окна "Настройка макета" (на вкладке конструктор в группе макет нажмите кнопку Изменить расположение и нажмите кнопку Дополнительные параметры расположения).
ms.openlocfilehash: af4089a3b215efaf49b8a45929ca94799fffcba5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813176"
---
# <a name="avenuesizey-cell-page-layout-section"></a><span data-ttu-id="1166f-103">Ячейка AvenueSizeY (раздел "Макет страницы")</span><span class="sxs-lookup"><span data-stu-id="1166f-103">AvenueSizeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="1166f-104">Определяет интервал по вертикали между фигурами на странице документа при расположении фигур с помощью диалогового окна " **Настройка макета** " (на вкладке **Конструктор** в группе **Макет** выберите пункт **Изменить** расположение и нажмите кнопку **более Параметры расположения**).</span><span class="sxs-lookup"><span data-stu-id="1166f-104">Determines the amount of vertical space between shapes on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout** Page, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1166f-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="1166f-105">Remarks</span></span>

<span data-ttu-id="1166f-106">Также можно задать это значение в диалоговом окне **Макет и маршрутизация интервалы** (на вкладку **Конструктор** , щелкните стрелку в группе **Параметры страницы** , перейдите на вкладку **Макет и маршрутизации** и нажмите кнопку **интервала**).</span><span class="sxs-lookup"><span data-stu-id="1166f-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="1166f-107">Динамические сетки используется в ячейке AvenueSizeY Если доступен только один фигуры для расчета интервал по вертикали.</span><span class="sxs-lookup"><span data-stu-id="1166f-107">The dynamic grid uses the setting in the AvenueSizeY cell when only one shape is available for calculating vertical spacing.</span></span> <span data-ttu-id="1166f-108">Использование динамических сетки на вкладке **Вид** в группе **Вспомогательные элементы** выберите **Динамических сетки**.</span><span class="sxs-lookup"><span data-stu-id="1166f-108">To use the dynamic grid, on the **View** tab, in the **Visual Aids** group, select **Dynamic Grid**.</span></span>
  
<span data-ttu-id="1166f-109">Чтобы получить ссылку на ячейку AvenueSizeY по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="1166f-109">To get a reference to the AvenueSizeY cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1166f-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="1166f-110">Cell name:</span></span>  <br/> | <span data-ttu-id="1166f-111">AvenueSizeY</span><span class="sxs-lookup"><span data-stu-id="1166f-111">AvenueSizeY</span></span>  <br/> |
   
<span data-ttu-id="1166f-112">Для получения ссылки на ячейки AvenueSizeY по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="1166f-112">To get a reference to the AvenueSizeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1166f-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="1166f-113">Section index:</span></span>  <br/> |<span data-ttu-id="1166f-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1166f-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1166f-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="1166f-115">Row index:</span></span>  <br/> |<span data-ttu-id="1166f-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="1166f-116">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="1166f-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="1166f-117">Cell index:</span></span>  <br/> |<span data-ttu-id="1166f-118">**visPLOAvenueSizeY**</span><span class="sxs-lookup"><span data-stu-id="1166f-118">**visPLOAvenueSizeY**</span></span> <br/> |
   

