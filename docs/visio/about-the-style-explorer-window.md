---
title: Сведения об окне обозревателя стилей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm60119
localization_priority: Normal
ms.assetid: bfdc1a63-c355-c759-bdfa-ce27e3ad10e7
description: Окно проводника стиль предоставляет разработчикам фигур быстрый способ для определения ячеек, которые фигуры наследуется из заданного стиля или стиля, из которой данная ячейка получает его значение.
ms.openlocfilehash: 25af478b8ac4e35c7ae0b88bf69aad21d679da17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813110"
---
# <a name="about-the-style-explorer-window"></a><span data-ttu-id="15dc0-103">Сведения об окне обозревателя стилей</span><span class="sxs-lookup"><span data-stu-id="15dc0-103">About the Style Explorer Window</span></span>

<span data-ttu-id="15dc0-104">Окно **Проводника стиль** предоставляет разработчикам фигур быстрый способ для определения ячеек, которые фигуры наследуется из заданного стиля или стиля, из которой данная ячейка получает его значение.</span><span class="sxs-lookup"><span data-stu-id="15dc0-104">The **Style Explorer** window provides shape developers with a quick way to determine which shape cells inherit from a given style, or the style from which a given cell inherits its value.</span></span> 
  
<span data-ttu-id="15dc0-105">Стили представляют собой именованные коллекции атрибутов, которые можно применять к фигуры форматирования.</span><span class="sxs-lookup"><span data-stu-id="15dc0-105">Styles are named collections of formatting attributes that you can apply to a shape.</span></span> <span data-ttu-id="15dc0-106">В Microsoft Visio один стиль можно определить текст, строки и атрибуты заливки как эффективный способ обеспечить соответствие фигур.</span><span class="sxs-lookup"><span data-stu-id="15dc0-106">In Microsoft Visio, a single style can define text, line, and fill attributes as an efficient way to ensure consistency in your shapes.</span></span> <span data-ttu-id="15dc0-107">Кроме того можно также определить стиль для любой один класс атрибута (текст, строки или заливки) или любое сочетание атрибутов.</span><span class="sxs-lookup"><span data-stu-id="15dc0-107">Additionally, you can also define a style for any one class of attribute (text, line, or fill) or any combination of attributes.</span></span> 
  
<span data-ttu-id="15dc0-108">В отличие от форм, с которыми вы применили атрибутов форматирования по отдельности фигур, производные от стиля их форматирование не только обеспечить согласованность, но также ответ лучше их создания, перемещения, масштабирования или вращаться.</span><span class="sxs-lookup"><span data-stu-id="15dc0-108">Unlike shapes to which you've applied formatting attributes individually, shapes that derive their formatting from a style not only ensure consistency but also respond better when they are created, moved, scaled, or rotated.</span></span> 
  
<span data-ttu-id="15dc0-109">Окно **Проводника стиль** предоставляет информацию, необходимую для лучше понять последствия изменения, внесенные с фигурами.</span><span class="sxs-lookup"><span data-stu-id="15dc0-109">The **Style Explorer** window provides the information you need to understand better the implications of changes you make to shapes.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="15dc0-110">Значения ячеек, которые отображаются черные в окне таблицы свойств фигуры наследуются; те, которые отображаются синий являются локальными.</span><span class="sxs-lookup"><span data-stu-id="15dc0-110">Cell values that appear black in the ShapeSheet window are inherited; those that appear blue are local.</span></span> 
  
## <a name="using-the-style-explorer-window"></a><span data-ttu-id="15dc0-111">С помощью окно проводника стилей</span><span class="sxs-lookup"><span data-stu-id="15dc0-111">Using the Style Explorer window</span></span>

<span data-ttu-id="15dc0-112">Для просмотра окно **Проводника стиль** , с помощью active, окно таблицы свойств фигуры на вкладке **Таблицы свойств фигуры средства разработки** в группе **Вид** выберите **Обозреватель стилей**.</span><span class="sxs-lookup"><span data-stu-id="15dc0-112">To view the **Style Explorer** window, with the ShapeSheet window active, on the **ShapeSheet Tools Design** tab, in the **View** group, select **Style Explorer**.</span></span> <span data-ttu-id="15dc0-113">Стиль появляется окно **Проводника закрепленного окна ShapeSheet по умолчанию** , но является привязанного окна, которую можно закрепить отсоединяться и располагаться или объединяются с другими доступные привязанного ShapeSheet windows, например окна **Трассировки формул** .</span><span class="sxs-lookup"><span data-stu-id="15dc0-113">The **Style Explorer** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated, or merged with other available anchored ShapeSheet windows, for example, the **Formula Tracing** window.</span></span> <span data-ttu-id="15dc0-114">В окне **Обозреватель стилей** находится в виде treeview все стили, определенные в текущем документе.</span><span class="sxs-lookup"><span data-stu-id="15dc0-114">The **Style Explorer** window contains a treeview display of all the styles defined in the current drawing.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="15dc0-115">Для получения сведений о стиля, щелкните правой кнопкой стиль в окне **Проводника стилей** для просмотра его таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="15dc0-115">To get information about a style, you can right-click the style in the **Style Explorer** window to view its ShapeSheet.</span></span> 
  
<span data-ttu-id="15dc0-116">Окно **Проводника стиль** представлены следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="15dc0-116">The **Style Explorer** window provides the following information:</span></span> 
  
- <span data-ttu-id="15dc0-117">Ячейки, наследующие от выбранного стиля их значения. При выборе стиля в окне **Проводника стиля** всем ячейкам в окне таблицы свойств фигуры, наследующие от этого стиля отображается без штриховки, а незначительно заштрихованная ячеек, которые не наследуются от этого стиля.</span><span class="sxs-lookup"><span data-stu-id="15dc0-117">The cells that inherit their values from a selected style.When you select a style in the **Style Explorer** window, all cells in the ShapeSheet window that inherit from that style appear without hatching, while cells that do not inherit from that style appear lightly hatched.</span></span> 
    
- <span data-ttu-id="15dc0-118">Стиль, из которого наследуется его значение выбранной ячейки. При выборе ячейки таблицы свойств фигуры, стиль, от которого он наследует его значение отображается на панели задач в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="15dc0-118">The style from which a selected cell inherits its value.When you select a ShapeSheet cell, the style from which it inherits its value is displayed on the taskbar under the ShapeSheet window.</span></span> 
    

