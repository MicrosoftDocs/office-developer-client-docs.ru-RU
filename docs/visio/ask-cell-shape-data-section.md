---
title: Попросите ячейки (раздел данных фигуры)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60
localization_priority: Normal
ms.assetid: b499a5eb-db8f-ebd0-d505-c9a002205e7d
description: Определяет, является ли пользователь будет опрошен для ввода данных фигур для фигуры при создании экземпляра или фигуры и копировании.
ms.openlocfilehash: 94e84be4bef5c8c13d5c8ef5108ab89b71f251b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813147"
---
# <a name="ask-cell-shape-data-section"></a><span data-ttu-id="1c2de-103">Попросите ячейки (раздел данных фигуры)</span><span class="sxs-lookup"><span data-stu-id="1c2de-103">Ask Cell (Shape Data Section)</span></span>

<span data-ttu-id="1c2de-104">Определяет, является ли пользователь будет опрошен для ввода данных фигур для фигуры при создании экземпляра или фигуры и копировании.</span><span class="sxs-lookup"><span data-stu-id="1c2de-104">Determines whether a user is queried to enter shape data for a shape when an instance is created or the shape is duplicated or copied.</span></span>
  
|<span data-ttu-id="1c2de-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="1c2de-105">**Value**</span></span>|<span data-ttu-id="1c2de-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1c2de-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1c2de-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="1c2de-107">TRUE</span></span>  <br/> |<span data-ttu-id="1c2de-108">Попросите пользователя ввести данные фигуры в диалоговом окне **Определение данных фигуры** .</span><span class="sxs-lookup"><span data-stu-id="1c2de-108">Ask user to enter shape data in the **Define Shape Data** dialog box.</span></span>  <br/> |
|<span data-ttu-id="1c2de-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="1c2de-109">FALSE</span></span>  <br/> |<span data-ttu-id="1c2de-110">Не запрашивать пользователя для ввода данных.</span><span class="sxs-lookup"><span data-stu-id="1c2de-110">Do not ask user to enter data.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c2de-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="1c2de-111">Remarks</span></span>

<span data-ttu-id="1c2de-112">Значение в этой ячейке соответствующий флажок **Запрашивать при перетаскивании** в диалоговом окне **Определение данных фигуры** (щелкните правой кнопкой мыши фигуру, выберите пункт **данные**и выберите **Определение данных фигуры**).</span><span class="sxs-lookup"><span data-stu-id="1c2de-112">The value in this cell corresponds to the **Ask on drop** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="1c2de-113">Для получения ссылки на ячейку Ask по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="1c2de-113">To get a reference to the Ask cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1c2de-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="1c2de-114">Cell name:</span></span>  <br/> |<span data-ttu-id="1c2de-115">Свойства. *имя* . Убедитесь, где свойств.  *имя* — это имя настраиваемого свойства строки.</span><span class="sxs-lookup"><span data-stu-id="1c2de-115">Prop. *name*  .Verify            where Prop.  *name*  is the name of the custom property row.</span></span>  <br/> |
   
<span data-ttu-id="1c2de-116">Для получения ссылки на ячейки Ask по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="1c2de-116">To get a reference to the Ask cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1c2de-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="1c2de-117">Section index:</span></span>  <br/> |<span data-ttu-id="1c2de-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="1c2de-118">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="1c2de-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="1c2de-119">Row index:</span></span>  <br/> |<span data-ttu-id="1c2de-120">**visRowProp** +  *i* где *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="1c2de-120">**visRowProp** +  *i*            where  *i*  = 0, 1, 2,...</span></span>  <br/> |
|<span data-ttu-id="1c2de-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="1c2de-121">Cell index:</span></span>  <br/> |<span data-ttu-id="1c2de-122">**visCustPropsAsk**</span><span class="sxs-lookup"><span data-stu-id="1c2de-122">**visCustPropsAsk**</span></span> <br/> |
   

