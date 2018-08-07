---
title: Ячейка BeginGroup (раздел "Действия")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60022
localization_priority: Normal
ms.assetid: 1ae7f629-fb9f-1a11-1194-b381d6c9de5b
description: Указывает, будет ли разделитель вставлен в меню над это действие.
ms.openlocfilehash: 749f611209d362811f5e4fb051780a4a642295c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813179"
---
# <a name="begingroup-cell-actions-section"></a><span data-ttu-id="dbb26-103">Ячейка BeginGroup (раздел "Действия")</span><span class="sxs-lookup"><span data-stu-id="dbb26-103">BeginGroup Cell (Actions Section)</span></span>

<span data-ttu-id="dbb26-104">Указывает, будет ли разделитель вставлен в меню над это действие.</span><span class="sxs-lookup"><span data-stu-id="dbb26-104">Indicates whether a separator is inserted into the menu above this action.</span></span> 
  
|<span data-ttu-id="dbb26-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="dbb26-105">**Value**</span></span>|<span data-ttu-id="dbb26-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dbb26-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dbb26-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="dbb26-107">TRUE</span></span>  <br/> |<span data-ttu-id="dbb26-108">Разделитель в меню над это действие.</span><span class="sxs-lookup"><span data-stu-id="dbb26-108">A separator is inserted into the menu above this action.</span></span>  <br/> |
|<span data-ttu-id="dbb26-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="dbb26-109">FALSE</span></span>  <br/> |<span data-ttu-id="dbb26-110">Разделитель не вставляется в меню над это действие (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="dbb26-110">A separator is not inserted into the menu above this action (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dbb26-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="dbb26-111">Remarks</span></span>

<span data-ttu-id="dbb26-112">Чтобы получить ссылку на ячейку BeginGroup по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="dbb26-112">To get a reference to the BeginGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dbb26-113">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="dbb26-113">Cell name:</span></span>  <br/> |<span data-ttu-id="dbb26-114">Действия.</span><span class="sxs-lookup"><span data-stu-id="dbb26-114">Actions.</span></span> <span data-ttu-id="dbb26-115">*имя*. BeginGroup где действия.</span><span class="sxs-lookup"><span data-stu-id="dbb26-115">*name*.BeginGroup where Actions.</span></span> <span data-ttu-id="dbb26-116">*имя* — это имя строки действий</span><span class="sxs-lookup"><span data-stu-id="dbb26-116">*name* is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="dbb26-117">Для получения ссылки на ячейки BeginGroup по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="dbb26-117">To get a reference to the BeginGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dbb26-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="dbb26-118">Section index:</span></span>  <br/> |<span data-ttu-id="dbb26-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="dbb26-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="dbb26-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="dbb26-120">Row index:</span></span>  <br/> |<span data-ttu-id="dbb26-121">**visRowAction** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="dbb26-121">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="dbb26-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="dbb26-122">Cell index:</span></span>  <br/> |<span data-ttu-id="dbb26-123">**visActionBeginGroup**</span><span class="sxs-lookup"><span data-stu-id="dbb26-123">**visActionBeginGroup**</span></span> <br/> |
   

