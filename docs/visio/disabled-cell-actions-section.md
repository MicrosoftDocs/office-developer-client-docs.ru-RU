---
title: Ячейка Disabled (раздел "Действия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251337
localization_priority: Normal
ms.assetid: ebf66729-d794-a398-268a-84d761bf06b6
description: Указывает, отключена ли пункт меню тега ярлык или действие.
ms.openlocfilehash: 3956b6cf5ccb870255d6943e74b4f02650952d09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813599"
---
# <a name="disabled-cell-actions-section"></a><span data-ttu-id="45fa2-103">Ячейка Disabled (раздел "Действия")</span><span class="sxs-lookup"><span data-stu-id="45fa2-103">Disabled Cell (Actions Section)</span></span>

<span data-ttu-id="45fa2-104">Указывает, отключена ли пункт меню тега ярлык или действие.</span><span class="sxs-lookup"><span data-stu-id="45fa2-104">Indicates whether an item on a shortcut or action tag menu is disabled.</span></span>
  
> [!NOTE]
> <span data-ttu-id="45fa2-105">В предыдущих версиях Microsoft Visio теги действий, называются смарт-тегов.</span><span class="sxs-lookup"><span data-stu-id="45fa2-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="45fa2-106">**Значение**</span><span class="sxs-lookup"><span data-stu-id="45fa2-106">**Value**</span></span>|<span data-ttu-id="45fa2-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="45fa2-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="45fa2-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="45fa2-108">TRUE</span></span>  <br/> |<span data-ttu-id="45fa2-109">Отключите имя команды (dim).</span><span class="sxs-lookup"><span data-stu-id="45fa2-109">Disable (dim) command name.</span></span>  <br/> |
|<span data-ttu-id="45fa2-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="45fa2-110">FALSE</span></span>  <br/> |<span data-ttu-id="45fa2-111">Включите имя команды (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="45fa2-111">Enable the command name (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45fa2-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="45fa2-112">Remarks</span></span>

<span data-ttu-id="45fa2-113">Чтобы получить ссылку на ячейку отключено по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="45fa2-113">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="45fa2-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="45fa2-114">Cell name:</span></span>  <br/> |<span data-ttu-id="45fa2-115">Действия.</span><span class="sxs-lookup"><span data-stu-id="45fa2-115">Actions.</span></span> <span data-ttu-id="45fa2-116">*имя* . Этот параметр отключен где действия.</span><span class="sxs-lookup"><span data-stu-id="45fa2-116">*name*  .Disabled           where Actions.</span></span> <span data-ttu-id="45fa2-117">*имя* — это имя строки действий</span><span class="sxs-lookup"><span data-stu-id="45fa2-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="45fa2-118">Для получения ссылки на ячейки отключено по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="45fa2-118">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="45fa2-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="45fa2-119">Section index:</span></span>  <br/> |<span data-ttu-id="45fa2-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="45fa2-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="45fa2-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="45fa2-121">Row index:</span></span>  <br/> |<span data-ttu-id="45fa2-122">**visRowAction** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="45fa2-122">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="45fa2-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="45fa2-123">Cell index:</span></span>  <br/> |<span data-ttu-id="45fa2-124">**visActionDisabled**</span><span class="sxs-lookup"><span data-stu-id="45fa2-124">**visActionDisabled**</span></span> <br/> |
   

