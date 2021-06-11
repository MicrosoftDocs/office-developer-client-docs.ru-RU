---
title: Label Cell (Shape Data Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm510
localization_priority: Normal
ms.assetid: 6d328b1c-8d92-eb1a-7317-7dd85c674ff9
description: Указывает метку, которая отображается пользователям в окне Shape Data. Метка состоит из символов альфа-цифр, включая символ underscore (_).
ms.openlocfilehash: d341acfbd47446a5b6dbee51ed821d1e1f34e15d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420180"
---
# <a name="label-cell-shape-data-section"></a><span data-ttu-id="a01a9-104">Label Cell (Shape Data Section)</span><span class="sxs-lookup"><span data-stu-id="a01a9-104">Label Cell (Shape Data Section)</span></span>

<span data-ttu-id="a01a9-105">Указывает метку, которая отображается пользователям в **окне Shape Data.**</span><span class="sxs-lookup"><span data-stu-id="a01a9-105">Specifies the label that appears to users in the **Shape Data** window.</span></span> <span data-ttu-id="a01a9-106">Метка состоит из символов альфа-цифр, включая символ underscore (_).</span><span class="sxs-lookup"><span data-stu-id="a01a9-106">A label consists of alphanumeric characters, including the underscore (_) character.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a01a9-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="a01a9-107">Remarks</span></span>

<span data-ttu-id="a01a9-108">Приложение автоматически заключит строку Label в кавычках в ячейке, но кавычка не отображается в окне **Shape Data.**</span><span class="sxs-lookup"><span data-stu-id="a01a9-108">The application automatically encloses the Label string in quotation marks in the cell, but the quotation marks are not displayed in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="a01a9-109">Если текст метки не найден, Visio отображает имя строки (Prop.Row) в **окне Shape Data.**</span><span class="sxs-lookup"><span data-stu-id="a01a9-109">If no label text is found, Visio displays the row name (Prop.Row) in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="a01a9-110">Чтобы получить ссылку на ячейку Label по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="a01a9-110">To get a reference to the Label cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a01a9-111">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="a01a9-111">Cell name:</span></span>  <br/> |<span data-ttu-id="a01a9-112">Prop. *Name*  . Метка, на которой проп.  *Имя*  — это имя строки</span><span class="sxs-lookup"><span data-stu-id="a01a9-112">Prop. *Name*  .Label where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="a01a9-113">Чтобы получить ссылку на ячейку Label по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="a01a9-113">To get a reference to the Label cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a01a9-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a01a9-114">Section index:</span></span>  <br/> |<span data-ttu-id="a01a9-115">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="a01a9-115">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="a01a9-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a01a9-116">Row index:</span></span>  <br/> |<span data-ttu-id="a01a9-117">**visRowProp**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="a01a9-117">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="a01a9-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a01a9-118">Cell index:</span></span>  <br/> |<span data-ttu-id="a01a9-119">**visCustPropsLabel**</span><span class="sxs-lookup"><span data-stu-id="a01a9-119">**visCustPropsLabel**</span></span> <br/> |
   

