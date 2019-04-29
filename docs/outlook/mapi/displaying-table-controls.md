---
title: Отображение элементов управления таблицы
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0882be14-573c-440c-954f-76ef70eea33e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 37f6cd0320894d500416672c3dd0d90ee3324b40
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422693"
---
# <a name="displaying-table-controls"></a><span data-ttu-id="28247-103">Отображение элементов управления таблицы</span><span class="sxs-lookup"><span data-stu-id="28247-103">Displaying Table Controls</span></span>

  
  
<span data-ttu-id="28247-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28247-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28247-105">Существует множество различных типов элементов управления, нет уникальных для MAPI.</span><span class="sxs-lookup"><span data-stu-id="28247-105">There are many different types of controls, none unique to MAPI.</span></span> <span data-ttu-id="28247-106">Однако MAPI определяет собственные структуры, которые используются вместе с [буилддисплайтабле](builddisplaytable.md) , для описания уникального набора данных, связанных с каждым элементом управления.</span><span class="sxs-lookup"><span data-stu-id="28247-106">However, MAPI defines its own structures that are used in conjunction with [BuildDisplayTable](builddisplaytable.md) to describe the unique set of data involved with each control.</span></span> 
  
<span data-ttu-id="28247-107">В следующей таблице перечислены структуры, описывающие каждый тип элемента управления.</span><span class="sxs-lookup"><span data-stu-id="28247-107">The following table lists the structures that describe each type of control.</span></span> 
  
|<span data-ttu-id="28247-108">**Структура элемента управления**</span><span class="sxs-lookup"><span data-stu-id="28247-108">**Control structure**</span></span>|<span data-ttu-id="28247-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="28247-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28247-110">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="28247-110">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |<span data-ttu-id="28247-111">Описывает элемент управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="28247-111">Describes a button control.</span></span>  <br/> |
|[<span data-ttu-id="28247-112">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="28247-112">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |<span data-ttu-id="28247-113">Описывает элемент управления "флажок".</span><span class="sxs-lookup"><span data-stu-id="28247-113">Describes a check box control.</span></span>  <br/> |
|[<span data-ttu-id="28247-114">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="28247-114">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |<span data-ttu-id="28247-115">Описывает элемент управления "поле со списком".</span><span class="sxs-lookup"><span data-stu-id="28247-115">Describes a combo box control.</span></span>  <br/> |
|[<span data-ttu-id="28247-116">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="28247-116">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |<span data-ttu-id="28247-117">Описывает элемент управления "раскрывающийся список".</span><span class="sxs-lookup"><span data-stu-id="28247-117">Describes a drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="28247-118">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="28247-118">DTBLEDIT</span></span>](dtbledit.md) <br/> |<span data-ttu-id="28247-119">Описывает элемент управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="28247-119">Describes an edit control.</span></span>  <br/> |
|[<span data-ttu-id="28247-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="28247-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |<span data-ttu-id="28247-121">Описывает элемент управления "Группа".</span><span class="sxs-lookup"><span data-stu-id="28247-121">Describes a group box control.</span></span>  <br/> |
|[<span data-ttu-id="28247-122">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="28247-122">DTBLLABEL</span></span>](dtbllabel.md) <br/> |<span data-ttu-id="28247-123">Описывает элемент управления "метка".</span><span class="sxs-lookup"><span data-stu-id="28247-123">Describes a label control.</span></span>  <br/> |
|[<span data-ttu-id="28247-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="28247-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |<span data-ttu-id="28247-125">Описывает элемент управления "список".</span><span class="sxs-lookup"><span data-stu-id="28247-125">Describes a list box control.</span></span>  <br/> |
|[<span data-ttu-id="28247-126">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="28247-126">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |<span data-ttu-id="28247-127">Описывает элемент управления раскрывающегося списка с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="28247-127">Describes a multiple-value drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="28247-128">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="28247-128">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |<span data-ttu-id="28247-129">Описывает элемент управления "список с несколькими значениями".</span><span class="sxs-lookup"><span data-stu-id="28247-129">Describes a multiple-value list box control.</span></span>  <br/> |
|[<span data-ttu-id="28247-130">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="28247-130">DTBLPAGE</span></span>](dtblpage.md) <br/> |<span data-ttu-id="28247-131">Описывает элемент управления "Вкладка".</span><span class="sxs-lookup"><span data-stu-id="28247-131">Describes a tabbed page control.</span></span>  <br/> |
|[<span data-ttu-id="28247-132">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="28247-132">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |<span data-ttu-id="28247-133">Описывает элемент управления "переключатель".</span><span class="sxs-lookup"><span data-stu-id="28247-133">Describes an option button control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="28247-134">См. также</span><span class="sxs-lookup"><span data-stu-id="28247-134">See also</span></span>



[<span data-ttu-id="28247-135">Реализация таблицы отображения</span><span class="sxs-lookup"><span data-stu-id="28247-135">Display Table Implementation</span></span>](display-table-implementation.md)

