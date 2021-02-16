---
title: ButtonFace Cell (Actions Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60025
localization_priority: Normal
ms.assetid: cf15b879-a47e-a5a5-bfdd-1d7ea423742f
description: Определяет значок, который отображается рядом с элементом в меню ярлыка или тега действия.
ms.openlocfilehash: 7ee9c4e7e857acb34ce75429aa0aaf679320b0e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407377"
---
# <a name="buttonface-cell-actions-section"></a><span data-ttu-id="f358f-103">ButtonFace Cell (Actions Section)</span><span class="sxs-lookup"><span data-stu-id="f358f-103">ButtonFace Cell (Actions Section)</span></span>

<span data-ttu-id="f358f-104">Определяет значок, который отображается рядом с элементом в меню ярлыка или тега действия.</span><span class="sxs-lookup"><span data-stu-id="f358f-104">Identifies the icon that appears next to an item on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f358f-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="f358f-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f358f-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="f358f-106">Remarks</span></span>

<span data-ttu-id="f358f-107">Строка, содержаная в ячейке ButtonFace, представляет ИД Microsoft Office кнопок.</span><span class="sxs-lookup"><span data-stu-id="f358f-107">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image.</span></span> <span data-ttu-id="f358f-108">Нулевое (0) или пустое значение означает, что значок не отображается.</span><span class="sxs-lookup"><span data-stu-id="f358f-108">A value of zero (0) or blank means no icon appears.</span></span> 
  
<span data-ttu-id="f358f-109">ИД, которые можно использовать в ячейке ButtonFace, такие же, как и для свойств **FaceID** объекта **CommandBarButton.**</span><span class="sxs-lookup"><span data-stu-id="f358f-109">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="f358f-110">Для получения дополнительных сведений об этих ИД на сайте MSDN найди поиск по запросу "Работа с изображениями кнопок панели команд".</span><span class="sxs-lookup"><span data-stu-id="f358f-110">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="f358f-111">Чтобы получить ссылку на ячейку ButtonFace по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="f358f-111">To get a reference to the ButtonFace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f358f-112">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="f358f-112">Cell name:</span></span>  <br/> |<span data-ttu-id="f358f-113">**Действия**.</span><span class="sxs-lookup"><span data-stu-id="f358f-113">**Actions**.</span></span>  <span data-ttu-id="f358f-114">*name*  .</span><span class="sxs-lookup"><span data-stu-id="f358f-114">*name*  .</span></span> <span data-ttu-id="f358f-115">**ButtonFace,**         где **действия**.</span><span class="sxs-lookup"><span data-stu-id="f358f-115">**ButtonFace**         where **Actions**.</span></span>  <span data-ttu-id="f358f-116">*имя*  — это имя строки действий</span><span class="sxs-lookup"><span data-stu-id="f358f-116">*name*  is the name of the actions row</span></span>  <br/> |
   
<span data-ttu-id="f358f-117">Чтобы получить ссылку на ячейку ButtonFace по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="f358f-117">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f358f-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f358f-118">Section index:</span></span>  <br/> |<span data-ttu-id="f358f-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="f358f-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="f358f-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f358f-120">Row index:</span></span>  <br/> |<span data-ttu-id="f358f-121">**visRowAction**  +   *i* где **i** = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f358f-121">**visRowAction** +  *i*           where **i** = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="f358f-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f358f-122">Cell index:</span></span>  <br/> |<span data-ttu-id="f358f-123">**visActionButtonFace**</span><span class="sxs-lookup"><span data-stu-id="f358f-123">**visActionButtonFace**</span></span> <br/> |
   

