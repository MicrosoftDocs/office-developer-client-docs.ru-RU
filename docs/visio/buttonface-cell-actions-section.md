---
title: Ячейка ButtonFace (раздел "Действия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60025
localization_priority: Normal
ms.assetid: cf15b879-a47e-a5a5-bfdd-1d7ea423742f
description: Определяет значок, который отображается рядом с элементом меню тега ярлык или действие.
ms.openlocfilehash: 29ff71bc04e94f97f1526b28bd52c2846327eff1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813314"
---
# <a name="buttonface-cell-actions-section"></a><span data-ttu-id="432f2-103">Ячейка ButtonFace (раздел "Действия")</span><span class="sxs-lookup"><span data-stu-id="432f2-103">ButtonFace Cell (Actions Section)</span></span>

<span data-ttu-id="432f2-104">Определяет значок, который отображается рядом с элементом меню тега ярлык или действие.</span><span class="sxs-lookup"><span data-stu-id="432f2-104">Identifies the icon that appears next to an item on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="432f2-105">В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="432f2-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="432f2-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="432f2-106">Remarks</span></span>

<span data-ttu-id="432f2-107">Строка, содержащихся в ячейке ButtonFace представляет идентификатор изображения кнопки Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="432f2-107">The string contained in the ButtonFace cell represents the ID of a Microsoft Office button face image.</span></span> <span data-ttu-id="432f2-108">Значение нуль (0) или пустая означает, что значок не отображается.</span><span class="sxs-lookup"><span data-stu-id="432f2-108">A value of zero (0) or blank means no icon appears.</span></span> 
  
<span data-ttu-id="432f2-109">Идентификаторы, которые могут использоваться в ячейке ButtonFace такие же, как идентификаторы, используется совместно со свойством **FaceID** **CommandBarButton** объекта.</span><span class="sxs-lookup"><span data-stu-id="432f2-109">The IDs that can be used in the ButtonFace cell are the same as the IDs used with the **FaceID** property of a **CommandBarButton** object.</span></span> <span data-ttu-id="432f2-110">Для получения дополнительных сведений об этих кодов поиск «работа с изображениями кнопки панели команд» на сайте MSDN.</span><span class="sxs-lookup"><span data-stu-id="432f2-110">For more details about these IDs, search for "working with command bar button images" on MSDN.</span></span> 
  
<span data-ttu-id="432f2-111">Чтобы получить ссылку на ячейку ButtonFace по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="432f2-111">To get a reference to the ButtonFace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="432f2-112">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="432f2-112">Cell name:</span></span>  <br/> |<span data-ttu-id="432f2-113">**Действия**.</span><span class="sxs-lookup"><span data-stu-id="432f2-113">**Actions**.</span></span>  <span data-ttu-id="432f2-114">*имя* .</span><span class="sxs-lookup"><span data-stu-id="432f2-114">*name*  .</span></span> <span data-ttu-id="432f2-115">**ButtonFace** где **действия**.</span><span class="sxs-lookup"><span data-stu-id="432f2-115">**ButtonFace**         where **Actions**.</span></span>  <span data-ttu-id="432f2-116">*имя* — это имя строки действий</span><span class="sxs-lookup"><span data-stu-id="432f2-116">*name*  is the name of the actions row</span></span>  <br/> |
   
<span data-ttu-id="432f2-117">Для получения ссылки на ячейки ButtonFace по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="432f2-117">To get a reference to the ButtonFace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="432f2-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="432f2-118">Section index:</span></span>  <br/> |<span data-ttu-id="432f2-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="432f2-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="432f2-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="432f2-120">Row index:</span></span>  <br/> |<span data-ttu-id="432f2-121">**visRowAction** +  *i* где **i** = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="432f2-121">**visRowAction** +  *i*           where **i** = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="432f2-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="432f2-122">Cell index:</span></span>  <br/> |<span data-ttu-id="432f2-123">**visActionButtonFace**</span><span class="sxs-lookup"><span data-stu-id="432f2-123">**visActionButtonFace**</span></span> <br/> |
   

