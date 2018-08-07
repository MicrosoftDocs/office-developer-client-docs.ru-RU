---
title: Ячейка Label (раздел "Данные фигуры")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm510
localization_priority: Normal
ms.assetid: 6d328b1c-8d92-eb1a-7317-7dd85c674ff9
description: Метка, которая отображается для пользователей в окне данных фигуры. Элемент label состоит из буквенно-цифровых символов, включая символ подчеркивания (_).
ms.openlocfilehash: 087bcb87a9e47131e6dbcd2d8df5c5da8a06894b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814011"
---
# <a name="label-cell-shape-data-section"></a><span data-ttu-id="d9b3f-104">Ячейка Label (раздел "Данные фигуры")</span><span class="sxs-lookup"><span data-stu-id="d9b3f-104">Label Cell (Shape Data Section)</span></span>

<span data-ttu-id="d9b3f-105">Метка, которая отображается для пользователей в окне **Данных фигуры** .</span><span class="sxs-lookup"><span data-stu-id="d9b3f-105">Specifies the label that appears to users in the **Shape Data** window.</span></span> <span data-ttu-id="d9b3f-106">Элемент label состоит из буквенно-цифровых символов, включая символ подчеркивания (_).</span><span class="sxs-lookup"><span data-stu-id="d9b3f-106">A label consists of alphanumeric characters, including the underscore (_) character.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d9b3f-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="d9b3f-107">Remarks</span></span>

<span data-ttu-id="d9b3f-108">Приложение автоматически заключает строку подписи в кавычки в ячейке, но кавычки не отображаются в окне **Данных фигуры** .</span><span class="sxs-lookup"><span data-stu-id="d9b3f-108">The application automatically encloses the Label string in quotation marks in the cell, but the quotation marks are not displayed in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="d9b3f-109">Если текст не метка не найден, Visio имя строки (Prop.Row) в окне **Данных фигуры** .</span><span class="sxs-lookup"><span data-stu-id="d9b3f-109">If no label text is found, Visio displays the row name (Prop.Row) in the **Shape Data** window.</span></span> 
  
<span data-ttu-id="d9b3f-110">Для получения ссылки на ячейки метки по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d9b3f-110">To get a reference to the Label cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d9b3f-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="d9b3f-111">Cell name:</span></span>  <br/> |<span data-ttu-id="d9b3f-112">Свойства. *Имя* . Метка где свойств.  *Имя* — это имя строки</span><span class="sxs-lookup"><span data-stu-id="d9b3f-112">Prop. *Name*  .Label where Prop.  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="d9b3f-113">Для получения ссылки на ячейки метки по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="d9b3f-113">To get a reference to the Label cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d9b3f-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d9b3f-114">Section index:</span></span>  <br/> |<span data-ttu-id="d9b3f-115">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="d9b3f-115">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="d9b3f-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d9b3f-116">Row index:</span></span>  <br/> |<span data-ttu-id="d9b3f-117">**visRowProp** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d9b3f-117">**visRowProp** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="d9b3f-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d9b3f-118">Cell index:</span></span>  <br/> |<span data-ttu-id="d9b3f-119">**visCustPropsLabel**</span><span class="sxs-lookup"><span data-stu-id="d9b3f-119">**visCustPropsLabel**</span></span> <br/> |
   

