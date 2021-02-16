---
title: UIVisibility Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60090
localization_priority: Normal
ms.assetid: df7f79df-770a-4868-e7e2-05c3828e23eb
description: Определяет, будет ли имя страницы открыно в пользовательском интерфейсе.
ms.openlocfilehash: 51ccd34cb40c286fe6b61818aea5a6b9c0b6d1a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437331"
---
# <a name="uivisibility-cell-page-properties-section"></a><span data-ttu-id="7f5bd-103">UIVisibility Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="7f5bd-103">UIVisibility Cell (Page Properties Section)</span></span>

<span data-ttu-id="7f5bd-104">Определяет, будет ли имя страницы открыно в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="7f5bd-104">Determines whether the page name is exposed in the user interface (UI).</span></span>
  
|<span data-ttu-id="7f5bd-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="7f5bd-105">**Value**</span></span>|<span data-ttu-id="7f5bd-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7f5bd-106">**Description**</span></span>|<span data-ttu-id="7f5bd-107">**Константа автоматизации**</span><span class="sxs-lookup"><span data-stu-id="7f5bd-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7f5bd-108">0</span><span class="sxs-lookup"><span data-stu-id="7f5bd-108">0</span></span>  <br/> |<span data-ttu-id="7f5bd-109">Отображение имени страницы в пользовательском интерфейсе (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="7f5bd-109">Display the page name in the UI (the default).</span></span>  <br/> |<span data-ttu-id="7f5bd-110">**visUIVNormal**</span><span class="sxs-lookup"><span data-stu-id="7f5bd-110">**visUIVNormal**</span></span> <br/> |
|<span data-ttu-id="7f5bd-111">1 </span><span class="sxs-lookup"><span data-stu-id="7f5bd-111">1</span></span>  <br/> |<span data-ttu-id="7f5bd-112">Не отображать имя страницы в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="7f5bd-112">Do not display the page name in the UI.</span></span>  <br/> |<span data-ttu-id="7f5bd-113">**visUIVHidden**</span><span class="sxs-lookup"><span data-stu-id="7f5bd-113">**visUIVHidden**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f5bd-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="7f5bd-114">Remarks</span></span>

<span data-ttu-id="7f5bd-115">При установке ячейки UIVisibility в **visUIVHidden** страница не отображается в любом месте пользовательского интерфейса, где отображается строка, содержащая имя страницы.</span><span class="sxs-lookup"><span data-stu-id="7f5bd-115">Setting the UIVisibility cell to **visUIVHidden** prevents the page from appearing anywhere in the UI where the string containing the page name appears.</span></span> <span data-ttu-id="7f5bd-116">Например, страница не будет указана в качестве параметра в проводнике **или** на вкладке страницы.</span><span class="sxs-lookup"><span data-stu-id="7f5bd-116">For example, the page would not be listed as an option in the **Drawing Explorer** or on the page tabs.</span></span> <span data-ttu-id="7f5bd-117">Однако страница остается доступной, если вы используете пути автоматизации или пользовательского интерфейса, которые не включают имя страницы, например команду **"Печать".**</span><span class="sxs-lookup"><span data-stu-id="7f5bd-117">The page remains accessible, however, if you use Automation or UI paths that do not include the page name, for example, the **Print** command.</span></span> 
  
 <span data-ttu-id="7f5bd-118">Эта ячейка предназначена для использования со страницами документов; Он не предназначен для использования со страницами наложения разметки, для которых ячейка UIVisibility по умолчанию имеет значение **visUIVHidden** и не должна быть изменена.</span><span class="sxs-lookup"><span data-stu-id="7f5bd-118">This cell is intended for use with document pages; it is not intended for use with markup overlay pages, which have the UIVisibility cell set to **visUIVHidden** by default and should not be changed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7f5bd-119">Чтобы скрыть страницу из  команды "Печать" документа, сделайте ее фоновой страницей (свойство **Type** **— visTypeBackground),** которая не используется в качестве фона для любой страницы (фигуры на фоновых страницах печатаются при печати страницы, использующей ее в качестве фона).</span><span class="sxs-lookup"><span data-stu-id="7f5bd-119">To hide a page from the document's **Print** command, make it a background page (**Type** property is **visTypeBackground** ) that is not used as a background by any page (shapes on background pages are printed when a page using it as a background is printed).</span></span> <span data-ttu-id="7f5bd-120">Команда **"Печать"** документа работает только с индексными страницами, а фоновые страницы не индексироваться.</span><span class="sxs-lookup"><span data-stu-id="7f5bd-120">The document's **Print** command only works with indexed pages, and background pages are not indexed.</span></span> 
  
<span data-ttu-id="7f5bd-121">Чтобы получить ссылку на ячейку UIVisibility по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="7f5bd-121">To get a reference to the UIVisibility cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7f5bd-122">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="7f5bd-122">Cell name:</span></span>  <br/> |<span data-ttu-id="7f5bd-123">UIVisibility</span><span class="sxs-lookup"><span data-stu-id="7f5bd-123">UIVisibility</span></span>  <br/> |
   
<span data-ttu-id="7f5bd-124">Чтобы получить ссылку на ячейку UIVisibility по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="7f5bd-124">To get a reference to the UIVisibility cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7f5bd-125">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="7f5bd-125">Section index:</span></span>  <br/> |<span data-ttu-id="7f5bd-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7f5bd-126">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="7f5bd-127">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="7f5bd-127">Row index:</span></span>  <br/> |<span data-ttu-id="7f5bd-128">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="7f5bd-128">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="7f5bd-129">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="7f5bd-129">Cell index:</span></span>  <br/> |<span data-ttu-id="7f5bd-130">**visPageUIVisibility**</span><span class="sxs-lookup"><span data-stu-id="7f5bd-130">**visPageUIVisibility**</span></span> <br/> |
   

