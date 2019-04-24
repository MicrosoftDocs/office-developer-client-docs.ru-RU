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
description: Определяет значок, который появляется рядом с элементом в контекстном меню или меню тегов действий.
ms.openlocfilehash: 7ee9c4e7e857acb34ce75429aa0aaf679320b0e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337550"
---
# <a name="buttonface-cell-actions-section"></a><span data-ttu-id="dd723-103">ButtonFace Cell (Actions Section)</span><span class="sxs-lookup"><span data-stu-id="dd723-103">ButtonFace Cell (Actions Section)</span></span>

<span data-ttu-id="dd723-104">Определяет значок, который появляется рядом с элементом в контекстном меню или меню тегов действий.</span><span class="sxs-lookup"><span data-stu-id="dd723-104">Identifies the icon that appears next to an item on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="dd723-105">В предыдущих версиях Microsoft Visio теги действий назывались смарт-тегами.</span><span class="sxs-lookup"><span data-stu-id="dd723-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dd723-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="dd723-106">Remarks</span></span>

<span data-ttu-id="dd723-107">Строка, которая находится в ячейке ButtonFace, представляет идентификатор изображения лицевой кнопки Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="dd723-107">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image.</span></span> <span data-ttu-id="dd723-108">Значение ноль (0) или пустое означает, что значок не отображается.</span><span class="sxs-lookup"><span data-stu-id="dd723-108">A value of zero (0) or blank means no icon appears.</span></span> 
  
<span data-ttu-id="dd723-109">Идентификаторы, которые можно использовать в ячейке ButtonFace, совпадают с идентификаторами, используемыми для свойства **FaceID** объекта **CommandBarButton** .</span><span class="sxs-lookup"><span data-stu-id="dd723-109">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="dd723-110">Для получения дополнительных сведений об этих идентификаторах выполните поиск по слову "работа с изображениями кнопок панели команд" на сайте MSDN.</span><span class="sxs-lookup"><span data-stu-id="dd723-110">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="dd723-111">Чтобы получить ссылку на ячейку ButtonFace по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="dd723-111">To get a reference to the ButtonFace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd723-112">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="dd723-112">Cell name:</span></span>  <br/> |<span data-ttu-id="dd723-113">**Действия**.</span><span class="sxs-lookup"><span data-stu-id="dd723-113">**Actions**.</span></span>  <span data-ttu-id="dd723-114">*Name (имя* ).</span><span class="sxs-lookup"><span data-stu-id="dd723-114">*name*  .</span></span> <span data-ttu-id="dd723-115">**ButtonFace** , \*\*\*\* где Actions.</span><span class="sxs-lookup"><span data-stu-id="dd723-115">**ButtonFace**         where **Actions**.</span></span>  <span data-ttu-id="dd723-116">*Name* — имя строки действий</span><span class="sxs-lookup"><span data-stu-id="dd723-116">*name*  is the name of the actions row</span></span>  <br/> |
   
<span data-ttu-id="dd723-117">Чтобы получить ссылку на ячейку ButtonFace по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="dd723-117">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd723-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="dd723-118">Section index:</span></span>  <br/> |<span data-ttu-id="dd723-119">**Виссектионактион**</span><span class="sxs-lookup"><span data-stu-id="dd723-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="dd723-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="dd723-120">Row index:</span></span>  <br/> |<span data-ttu-id="dd723-121">**висровактион** +  *i* , где **i** = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="dd723-121">**visRowAction** +  *i*           where **i** = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="dd723-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="dd723-122">Cell index:</span></span>  <br/> |<span data-ttu-id="dd723-123">**Висактионбуттонфаце**</span><span class="sxs-lookup"><span data-stu-id="dd723-123">**visActionButtonFace**</span></span> <br/> |
   

