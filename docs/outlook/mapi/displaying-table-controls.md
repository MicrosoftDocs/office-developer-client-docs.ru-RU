---
title: Отображение элементов управления таблицами
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0882be14-573c-440c-954f-76ef70eea33e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 11b3279582c4cfb0d2c2249c6f4eddd7f0260b49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808325"
---
# <a name="displaying-table-controls"></a><span data-ttu-id="5d08a-103">Отображение элементов управления таблицами</span><span class="sxs-lookup"><span data-stu-id="5d08a-103">Displaying Table Controls</span></span>

  
  
<span data-ttu-id="5d08a-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5d08a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5d08a-105">Существует несколько различных типов элементов управления, ни один уникальный MAPI.</span><span class="sxs-lookup"><span data-stu-id="5d08a-105">There are many different types of controls, none unique to MAPI.</span></span> <span data-ttu-id="5d08a-106">Тем не менее MAPI определяет собственные структуры, которые используются в сочетании с [BuildDisplayTable](builddisplaytable.md) для описания уникальный набор данных, связанных с каждым элементом управления.</span><span class="sxs-lookup"><span data-stu-id="5d08a-106">However, MAPI defines its own structures that are used in conjunction with [BuildDisplayTable](builddisplaytable.md) to describe the unique set of data involved with each control.</span></span> 
  
<span data-ttu-id="5d08a-107">В следующей таблице приведены структуры, которые описывают каждый тип элемента управления.</span><span class="sxs-lookup"><span data-stu-id="5d08a-107">The following table lists the structures that describe each type of control.</span></span> 
  
|<span data-ttu-id="5d08a-108">**Структура элемента управления**</span><span class="sxs-lookup"><span data-stu-id="5d08a-108">**Control structure**</span></span>|<span data-ttu-id="5d08a-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5d08a-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5d08a-110">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="5d08a-110">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |<span data-ttu-id="5d08a-111">Описание элемента управления button.</span><span class="sxs-lookup"><span data-stu-id="5d08a-111">Describes a button control.</span></span>  <br/> |
|[<span data-ttu-id="5d08a-112">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="5d08a-112">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |<span data-ttu-id="5d08a-113">Описывает элемент управления "флажок".</span><span class="sxs-lookup"><span data-stu-id="5d08a-113">Describes a check box control.</span></span>  <br/> |
|[<span data-ttu-id="5d08a-114">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="5d08a-114">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |<span data-ttu-id="5d08a-115">Описывает элемент управления ComboBox.</span><span class="sxs-lookup"><span data-stu-id="5d08a-115">Describes a combo box control.</span></span>  <br/> |
|[<span data-ttu-id="5d08a-116">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="5d08a-116">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |<span data-ttu-id="5d08a-117">Описывает элемент управления раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="5d08a-117">Describes a drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="5d08a-118">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="5d08a-118">DTBLEDIT</span></span>](dtbledit.md) <br/> |<span data-ttu-id="5d08a-119">Описание элемента управления.</span><span class="sxs-lookup"><span data-stu-id="5d08a-119">Describes an edit control.</span></span>  <br/> |
|[<span data-ttu-id="5d08a-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="5d08a-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |<span data-ttu-id="5d08a-121">Описывает элемент управления поля группы.</span><span class="sxs-lookup"><span data-stu-id="5d08a-121">Describes a group box control.</span></span>  <br/> |
|[<span data-ttu-id="5d08a-122">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="5d08a-122">DTBLLABEL</span></span>](dtbllabel.md) <br/> |<span data-ttu-id="5d08a-123">Описываются элементы управления label.</span><span class="sxs-lookup"><span data-stu-id="5d08a-123">Describes a label control.</span></span>  <br/> |
|[<span data-ttu-id="5d08a-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="5d08a-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |<span data-ttu-id="5d08a-125">Описывает элемент управления списка.</span><span class="sxs-lookup"><span data-stu-id="5d08a-125">Describes a list box control.</span></span>  <br/> |
|[<span data-ttu-id="5d08a-126">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="5d08a-126">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |<span data-ttu-id="5d08a-127">Описывает элемент управления несколькими значениями раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="5d08a-127">Describes a multiple-value drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="5d08a-128">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="5d08a-128">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |<span data-ttu-id="5d08a-129">Описывает элемент управления списка несколько значений.</span><span class="sxs-lookup"><span data-stu-id="5d08a-129">Describes a multiple-value list box control.</span></span>  <br/> |
|[<span data-ttu-id="5d08a-130">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="5d08a-130">DTBLPAGE</span></span>](dtblpage.md) <br/> |<span data-ttu-id="5d08a-131">Описание управления страницы с вкладками.</span><span class="sxs-lookup"><span data-stu-id="5d08a-131">Describes a tabbed page control.</span></span>  <br/> |
|[<span data-ttu-id="5d08a-132">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="5d08a-132">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |<span data-ttu-id="5d08a-133">Описывает элемент управления.</span><span class="sxs-lookup"><span data-stu-id="5d08a-133">Describes an option button control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5d08a-134">См. также</span><span class="sxs-lookup"><span data-stu-id="5d08a-134">See also</span></span>



[<span data-ttu-id="5d08a-135">Реализация таблицы отображения</span><span class="sxs-lookup"><span data-stu-id="5d08a-135">Display Table Implementation</span></span>](display-table-implementation.md)

