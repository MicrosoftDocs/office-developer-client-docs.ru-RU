---
title: Invisible Cell (Shape Data Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251341
localization_priority: Normal
ms.assetid: 5f368c2e-2a40-38ee-3568-ed5c57633345
description: Указывает, отображается ли элемент данных фигуры в окне "данные фигуры".
ms.openlocfilehash: 8671fcc249b7ca81c011f697721093e7842c1558
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357269"
---
# <a name="invisible-cell-shape-data-section"></a><span data-ttu-id="d231a-103">Invisible Cell (Shape Data Section)</span><span class="sxs-lookup"><span data-stu-id="d231a-103">Invisible Cell (Shape Data Section)</span></span>

<span data-ttu-id="d231a-104">Указывает, отображается ли элемент данных фигуры в окне " **данные фигуры** ".</span><span class="sxs-lookup"><span data-stu-id="d231a-104">Specifies whether the shape data item is visible in the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="d231a-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="d231a-105">**Value**</span></span>|<span data-ttu-id="d231a-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d231a-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d231a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d231a-107">TRUE</span></span>  <br/> | <span data-ttu-id="d231a-108">Элемент данных фигуры не отображается.</span><span class="sxs-lookup"><span data-stu-id="d231a-108">Shape data item is not visible.</span></span>  <br/> |
| <span data-ttu-id="d231a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d231a-109">FALSE</span></span>  <br/> | <span data-ttu-id="d231a-110">Элемент данных фигуры является видимым.</span><span class="sxs-lookup"><span data-stu-id="d231a-110">Shape data item is visible.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d231a-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="d231a-111">Remarks</span></span>

<span data-ttu-id="d231a-112">Значение в этой ячейке соответствует флажку **скрытый** в диалоговом окне **Определение данных фигуры** (щелкните фигуру правой кнопкой мыши, наведите указатель мыши на пункт **данные**и выберите команду **определить данные фигуры**).</span><span class="sxs-lookup"><span data-stu-id="d231a-112">The value in this cell corresponds to the **Hidden** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="d231a-113">Чтобы получить ссылку на неВидимую ячейку по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="d231a-113">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d231a-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="d231a-114">Cell name:</span></span>  <br/> | <span data-ttu-id="d231a-115">Установите.  *Name (имя* ). НеВидимое, где prop.  *Name* — имя строки</span><span class="sxs-lookup"><span data-stu-id="d231a-115">Prop.  *name*  .Invisible where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="d231a-116">Чтобы получить ссылку на неВидимую ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="d231a-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d231a-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d231a-117">Section index:</span></span>  <br/> |<span data-ttu-id="d231a-118">**Виссектионпроп**</span><span class="sxs-lookup"><span data-stu-id="d231a-118">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="d231a-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d231a-119">Row index:</span></span>  <br/> |<span data-ttu-id="d231a-120">**висровпроп** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d231a-120">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d231a-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d231a-121">Cell index:</span></span>  <br/> |<span data-ttu-id="d231a-122">**Вискустпропсинвис**</span><span class="sxs-lookup"><span data-stu-id="d231a-122">**visCustPropsInvis**</span></span> <br/> |
   

