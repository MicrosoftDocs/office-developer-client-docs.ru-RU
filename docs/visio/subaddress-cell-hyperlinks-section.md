---
title: SubAddress Cell (Hyperlinks Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm985
localization_priority: Normal
ms.assetid: 949448fd-0f85-b56a-945e-1da0e48609e8
description: Указывает расположение в целевом документе для ссылки.
ms.openlocfilehash: 092a53bd7c9d5adb77ed35f3e2ef53888bd6ebea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349324"
---
# <a name="subaddress-cell-hyperlinks-section"></a><span data-ttu-id="85626-103">SubAddress Cell (Hyperlinks Section)</span><span class="sxs-lookup"><span data-stu-id="85626-103">SubAddress Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="85626-104">Указывает расположение в целевом документе для ссылки.</span><span class="sxs-lookup"><span data-stu-id="85626-104">Specifies a location within the target document to link to.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="85626-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="85626-105">Remarks</span></span>

<span data-ttu-id="85626-106">Например, если ячейка Address называется "Drawing1.vsdx", ячейка SubAddress может указать имя страницы, например "Page-3".</span><span class="sxs-lookup"><span data-stu-id="85626-106">For example, if the Address cell is "Drawing1.vsdx", the SubAddress cell can specify a page name such as "Page-3".</span></span> <span data-ttu-id="85626-107">Если ячейка Address является Microsoft Excel файлом "Samples.xlsx", значение этой ячейки может быть листом или диапазоном в листе, например "Функции листа" или "Sheet1! A1:D10".</span><span class="sxs-lookup"><span data-stu-id="85626-107">If the Address cell is the Microsoft Excel file "Samples.xlsx", the value of this cell can be a worksheet or range within a worksheet, such as "Worksheet Functions" or "Sheet1!A1:D10".</span></span> <span data-ttu-id="85626-108">Если ячейка Address является ", значение этой ячейки может быть именем якоря в документе, например https://www.microsoft.com/office/ "решения".</span><span class="sxs-lookup"><span data-stu-id="85626-108">If the Address cell is "https://www.microsoft.com/office/", the value of this cell can be a named anchor within the document, such as "solutions".</span></span>
  
<span data-ttu-id="85626-109">Вы также можете установить значение этой ячейки в диалоговом окне **Гиперссылки** (в группе **Ссылки** на вкладке **Вставка** нажмите **кнопку Hyperlink).**</span><span class="sxs-lookup"><span data-stu-id="85626-109">You can also set the value of this cell in the **Hyperlinks** dialog box (in the **Links** group on the **Insert** tab, click **Hyperlink**).</span></span>
  
<span data-ttu-id="85626-110">Чтобы получить ссылку на ячейку SubAddress по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="85626-110">To get a reference to the SubAddress cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="85626-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="85626-111">Cell name:</span></span>  <br/> | <span data-ttu-id="85626-112">Гиперссылка.</span><span class="sxs-lookup"><span data-stu-id="85626-112">Hyperlink.</span></span>  <span data-ttu-id="85626-113">*имя*  . SubAddress, где  *Hyperlink .name*  — это имя строки</span><span class="sxs-lookup"><span data-stu-id="85626-113">*name*  .SubAddress where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="85626-114">Чтобы получить ссылку на ячейку **SubAddress** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="85626-114">To get a reference to the **SubAddress** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="85626-115">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="85626-115">Section index:</span></span>  <br/> |<span data-ttu-id="85626-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="85626-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="85626-117">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="85626-117">Row index:</span></span>  <br/> |<span data-ttu-id="85626-118">**visRow1stHyperlink**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="85626-118">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="85626-119">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="85626-119">Cell index:</span></span>  <br/> |<span data-ttu-id="85626-120">**visHLinkSubAddress**</span><span class="sxs-lookup"><span data-stu-id="85626-120">**visHLinkSubAddress**</span></span> <br/> |
   

