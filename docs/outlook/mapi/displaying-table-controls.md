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
# <a name="displaying-table-controls"></a><span data-ttu-id="5943f-103">Отображение элементов управления таблицы</span><span class="sxs-lookup"><span data-stu-id="5943f-103">Displaying Table Controls</span></span>

  
  
<span data-ttu-id="5943f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5943f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5943f-105">Существует множество различных типов элементов управления, не уникальных для MAPI.</span><span class="sxs-lookup"><span data-stu-id="5943f-105">There are many different types of controls, none unique to MAPI.</span></span> <span data-ttu-id="5943f-106">Однако MAPI определяет собственные структуры, которые используются в сочетании с [BuildDisplayTable](builddisplaytable.md) для описания уникального набора данных, используемых для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="5943f-106">However, MAPI defines its own structures that are used in conjunction with [BuildDisplayTable](builddisplaytable.md) to describe the unique set of data involved with each control.</span></span> 
  
<span data-ttu-id="5943f-107">В следующей таблице перечислены структуры, описывая каждый тип управления.</span><span class="sxs-lookup"><span data-stu-id="5943f-107">The following table lists the structures that describe each type of control.</span></span> 
  
|<span data-ttu-id="5943f-108">**Структура управления**</span><span class="sxs-lookup"><span data-stu-id="5943f-108">**Control structure**</span></span>|<span data-ttu-id="5943f-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5943f-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5943f-110">DTBLBUTTON</span><span class="sxs-lookup"><span data-stu-id="5943f-110">DTBLBUTTON</span></span>](dtblbutton.md) <br/> |<span data-ttu-id="5943f-111">Описывает кнопку управления.</span><span class="sxs-lookup"><span data-stu-id="5943f-111">Describes a button control.</span></span>  <br/> |
|[<span data-ttu-id="5943f-112">DTBLCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="5943f-112">DTBLCHECKBOX</span></span>](dtblcheckbox.md) <br/> |<span data-ttu-id="5943f-113">Описание контрольного окна.</span><span class="sxs-lookup"><span data-stu-id="5943f-113">Describes a check box control.</span></span>  <br/> |
|[<span data-ttu-id="5943f-114">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="5943f-114">DTBLCOMBOBOX</span></span>](dtblcombobox.md) <br/> |<span data-ttu-id="5943f-115">Описание управления полем со combo.</span><span class="sxs-lookup"><span data-stu-id="5943f-115">Describes a combo box control.</span></span>  <br/> |
|[<span data-ttu-id="5943f-116">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="5943f-116">DTBLDDLBX</span></span>](dtblddlbx.md) <br/> |<span data-ttu-id="5943f-117">Описание выпадаемого списка.</span><span class="sxs-lookup"><span data-stu-id="5943f-117">Describes a drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="5943f-118">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="5943f-118">DTBLEDIT</span></span>](dtbledit.md) <br/> |<span data-ttu-id="5943f-119">Описывает изменение.</span><span class="sxs-lookup"><span data-stu-id="5943f-119">Describes an edit control.</span></span>  <br/> |
|[<span data-ttu-id="5943f-120">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="5943f-120">DTBLGROUPBOX</span></span>](dtblgroupbox.md) <br/> |<span data-ttu-id="5943f-121">Описывает групповую групповую группу.</span><span class="sxs-lookup"><span data-stu-id="5943f-121">Describes a group box control.</span></span>  <br/> |
|[<span data-ttu-id="5943f-122">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="5943f-122">DTBLLABEL</span></span>](dtbllabel.md) <br/> |<span data-ttu-id="5943f-123">Описывает метку.</span><span class="sxs-lookup"><span data-stu-id="5943f-123">Describes a label control.</span></span>  <br/> |
|[<span data-ttu-id="5943f-124">DTBLLBX</span><span class="sxs-lookup"><span data-stu-id="5943f-124">DTBLLBX</span></span>](dtbllbx.md) <br/> |<span data-ttu-id="5943f-125">Описание списка.</span><span class="sxs-lookup"><span data-stu-id="5943f-125">Describes a list box control.</span></span>  <br/> |
|[<span data-ttu-id="5943f-126">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="5943f-126">DTBLMVDDLBOX</span></span>](dtblmvddlbox.md) <br/> |<span data-ttu-id="5943f-127">Описание выпадаемого списка с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="5943f-127">Describes a multiple-value drop-down list box control.</span></span>  <br/> |
|[<span data-ttu-id="5943f-128">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="5943f-128">DTBLMVLISTBOX</span></span>](dtblmvlistbox.md) <br/> |<span data-ttu-id="5943f-129">Описывает список с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="5943f-129">Describes a multiple-value list box control.</span></span>  <br/> |
|[<span data-ttu-id="5943f-130">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="5943f-130">DTBLPAGE</span></span>](dtblpage.md) <br/> |<span data-ttu-id="5943f-131">Описывает вкладку управления страницей.</span><span class="sxs-lookup"><span data-stu-id="5943f-131">Describes a tabbed page control.</span></span>  <br/> |
|[<span data-ttu-id="5943f-132">DTBLRADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="5943f-132">DTBLRADIOBUTTON</span></span>](dtblradiobutton.md) <br/> |<span data-ttu-id="5943f-133">Описывает параметр управления кнопкой.</span><span class="sxs-lookup"><span data-stu-id="5943f-133">Describes an option button control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5943f-134">См. также</span><span class="sxs-lookup"><span data-stu-id="5943f-134">See also</span></span>



[<span data-ttu-id="5943f-135">Реализация таблицы отображения</span><span class="sxs-lookup"><span data-stu-id="5943f-135">Display Table Implementation</span></span>](display-table-implementation.md)

