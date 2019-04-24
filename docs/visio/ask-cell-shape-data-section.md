---
title: Ask Cell (Shape Data Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60
localization_priority: Normal
ms.assetid: b499a5eb-db8f-ebd0-d505-c9a002205e7d
description: Определяет, запрашивается ли пользователю ввод данных фигуры для фигуры при создании экземпляра или дублировании или копировании фигуры.
ms.openlocfilehash: 0aa270ff918866d8f683a6408ccd71b6a22d555d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341442"
---
# <a name="ask-cell-shape-data-section"></a><span data-ttu-id="6ce5a-103">Ask Cell (Shape Data Section)</span><span class="sxs-lookup"><span data-stu-id="6ce5a-103">Ask Cell (Shape Data Section)</span></span>

<span data-ttu-id="6ce5a-104">Определяет, запрашивается ли пользователю ввод данных фигуры для фигуры при создании экземпляра или дублировании или копировании фигуры.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-104">Determines whether a user is queried to enter shape data for a shape when an instance is created or the shape is duplicated or copied.</span></span>
  
|<span data-ttu-id="6ce5a-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="6ce5a-105">**Value**</span></span>|<span data-ttu-id="6ce5a-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6ce5a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6ce5a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="6ce5a-107">TRUE</span></span>  <br/> |<span data-ttu-id="6ce5a-108">ПоПросите пользователя ввести данные фигуры в диалоговом окне **Определение данных фигуры** .</span><span class="sxs-lookup"><span data-stu-id="6ce5a-108">Ask user to enter shape data in the **Define Shape Data** dialog box.</span></span>  <br/> |
|<span data-ttu-id="6ce5a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="6ce5a-109">FALSE</span></span>  <br/> |<span data-ttu-id="6ce5a-110">Не рекомендуйте пользователю ввести данные.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-110">Do not ask user to enter data.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ce5a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6ce5a-111">Remarks</span></span>

<span data-ttu-id="6ce5a-112">Значение в этой ячейке соответствует флажку **запрос на удаление** в диалоговом окне **Определение данных фигуры** (щелкните фигуру правой кнопкой мыши, наведите указатель мыши на пункт **данные**и выберите команду **определить данные фигуры**).</span><span class="sxs-lookup"><span data-stu-id="6ce5a-112">The value in this cell corresponds to the **Ask on drop** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="6ce5a-113">Чтобы получить ссылку на ячейку Ask по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="6ce5a-113">To get a reference to the Ask cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6ce5a-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="6ce5a-114">Cell name:</span></span>  <br/> |<span data-ttu-id="6ce5a-115">Установите. *Name (имя* ). Проверьте, где prop.  *Name* имя строки настраиваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="6ce5a-115">Prop. *name*  .Verify            where Prop.  *name*  is the name of the custom property row.</span></span>  <br/> |
   
<span data-ttu-id="6ce5a-116">Чтобы получить ссылку на ячейку Ask по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="6ce5a-116">To get a reference to the Ask cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6ce5a-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="6ce5a-117">Section index:</span></span>  <br/> |<span data-ttu-id="6ce5a-118">**Виссектионпроп**</span><span class="sxs-lookup"><span data-stu-id="6ce5a-118">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="6ce5a-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="6ce5a-119">Row index:</span></span>  <br/> |<span data-ttu-id="6ce5a-120">**висровпроп** +  *i* , где *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="6ce5a-120">**visRowProp** +  *i*            where  *i*  = 0, 1, 2,...</span></span>  <br/> |
|<span data-ttu-id="6ce5a-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="6ce5a-121">Cell index:</span></span>  <br/> |<span data-ttu-id="6ce5a-122">**Вискустпропсаск**</span><span class="sxs-lookup"><span data-stu-id="6ce5a-122">**visCustPropsAsk**</span></span> <br/> |
   

