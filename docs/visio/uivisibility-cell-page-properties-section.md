---
title: Ячейка UIVisibility (раздел "Свойства страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60090
localization_priority: Normal
ms.assetid: df7f79df-770a-4868-e7e2-05c3828e23eb
description: Определяет, является ли имя страницы, открытой в пользовательского интерфейса (UI).
ms.openlocfilehash: dcb4a14ff89c7f5c77916e6b188aaf87e1711ab0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815119"
---
# <a name="uivisibility-cell-page-properties-section"></a><span data-ttu-id="084c6-103">Ячейка UIVisibility (раздел "Свойства страницы")</span><span class="sxs-lookup"><span data-stu-id="084c6-103">UIVisibility Cell (Page Properties Section)</span></span>

<span data-ttu-id="084c6-104">Определяет, является ли имя страницы, открытой в пользовательского интерфейса (UI).</span><span class="sxs-lookup"><span data-stu-id="084c6-104">Determines whether the page name is exposed in the user interface (UI).</span></span>
  
|<span data-ttu-id="084c6-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="084c6-105">**Value**</span></span>|<span data-ttu-id="084c6-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="084c6-106">**Description**</span></span>|<span data-ttu-id="084c6-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="084c6-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="084c6-108">0</span><span class="sxs-lookup"><span data-stu-id="084c6-108">0</span></span>  <br/> |<span data-ttu-id="084c6-109">Отображаемое имя страницы в пользовательском Интерфейсе (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="084c6-109">Display the page name in the UI (the default).</span></span>  <br/> |<span data-ttu-id="084c6-110">**visUIVNormal**</span><span class="sxs-lookup"><span data-stu-id="084c6-110">**visUIVNormal**</span></span> <br/> |
|<span data-ttu-id="084c6-111">1</span><span class="sxs-lookup"><span data-stu-id="084c6-111">1</span></span>  <br/> |<span data-ttu-id="084c6-112">Имя страницы не отображаются в пользовательском Интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="084c6-112">Do not display the page name in the UI.</span></span>  <br/> |<span data-ttu-id="084c6-113">**visUIVHidden**</span><span class="sxs-lookup"><span data-stu-id="084c6-113">**visUIVHidden**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="084c6-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="084c6-114">Remarks</span></span>

<span data-ttu-id="084c6-115">Установка для ячейки UIVisibility **visUIVHidden** запрещает странице Отображение в любом месте в пользовательском Интерфейсе, где отображается строка, содержащая имя страницы.</span><span class="sxs-lookup"><span data-stu-id="084c6-115">Setting the UIVisibility cell to **visUIVHidden** prevents the page from appearing anywhere in the UI where the string containing the page name appears.</span></span> <span data-ttu-id="084c6-116">Например страницы не могут быть указаны как параметр в **Обозревателе документа** или на вкладки.</span><span class="sxs-lookup"><span data-stu-id="084c6-116">For example, the page would not be listed as an option in the **Drawing Explorer** or on the page tabs.</span></span> <span data-ttu-id="084c6-117">Страницы остается доступным, тем не менее, если вы используете автоматизации или пользовательского интерфейса путей, которые не включать имя страницы, например, команда **печати** .</span><span class="sxs-lookup"><span data-stu-id="084c6-117">The page remains accessible, however, if you use Automation or UI paths that do not include the page name, for example, the **Print** command.</span></span> 
  
 <span data-ttu-id="084c6-118">В этой ячейке предназначен для использования со страницы документа; он не предназначен для использования с разметки перекрытия страниц, которые имеют UIVisibility ячейки, значение **visUIVHidden** по умолчанию и не должно изменяться.</span><span class="sxs-lookup"><span data-stu-id="084c6-118">This cell is intended for use with document pages; it is not intended for use with markup overlay pages, which have the UIVisibility cell set to **visUIVHidden** by default and should not be changed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="084c6-119">Чтобы скрыть страницы из команды **Печать** документа, сделать его на страницу фон (**Тип** свойства — **visTypeBackground** ), который не используется как фон любую страницу (фигуры на фоне печати страниц при страницы, используя в качестве фона При выводе на печать).</span><span class="sxs-lookup"><span data-stu-id="084c6-119">To hide a page from the document's **Print** command, make it a background page (**Type** property is **visTypeBackground** ) that is not used as a background by any page (shapes on background pages are printed when a page using it as a background is printed).</span></span> <span data-ttu-id="084c6-120">Команда **Печать** документов работает только с индексированных страниц и фона страниц, не индексируются.</span><span class="sxs-lookup"><span data-stu-id="084c6-120">The document's **Print** command only works with indexed pages, and background pages are not indexed.</span></span> 
  
<span data-ttu-id="084c6-121">Чтобы получить ссылку на ячейку UIVisibility по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="084c6-121">To get a reference to the UIVisibility cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="084c6-122">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="084c6-122">Cell name:</span></span>  <br/> |<span data-ttu-id="084c6-123">UIVisibility</span><span class="sxs-lookup"><span data-stu-id="084c6-123">UIVisibility</span></span>  <br/> |
   
<span data-ttu-id="084c6-124">Для получения ссылки на ячейки UIVisibility по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="084c6-124">To get a reference to the UIVisibility cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="084c6-125">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="084c6-125">Section index:</span></span>  <br/> |<span data-ttu-id="084c6-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="084c6-126">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="084c6-127">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="084c6-127">Row index:</span></span>  <br/> |<span data-ttu-id="084c6-128">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="084c6-128">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="084c6-129">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="084c6-129">Cell index:</span></span>  <br/> |<span data-ttu-id="084c6-130">**visPageUIVisibility**</span><span class="sxs-lookup"><span data-stu-id="084c6-130">**visPageUIVisibility**</span></span> <br/> |
   

