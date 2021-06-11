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
description: Определяет, запрашивается ли пользователь для ввода данных фигуры при создания экземпляра или их копировании.
ms.openlocfilehash: 0aa270ff918866d8f683a6408ccd71b6a22d555d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426866"
---
# <a name="ask-cell-shape-data-section"></a><span data-ttu-id="23b57-103">Ask Cell (Shape Data Section)</span><span class="sxs-lookup"><span data-stu-id="23b57-103">Ask Cell (Shape Data Section)</span></span>

<span data-ttu-id="23b57-104">Определяет, запрашивается ли пользователь для ввода данных фигуры при создания экземпляра или их копировании.</span><span class="sxs-lookup"><span data-stu-id="23b57-104">Determines whether a user is queried to enter shape data for a shape when an instance is created or the shape is duplicated or copied.</span></span>
  
|<span data-ttu-id="23b57-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="23b57-105">**Value**</span></span>|<span data-ttu-id="23b57-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="23b57-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="23b57-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="23b57-107">TRUE</span></span>  <br/> |<span data-ttu-id="23b57-108">Попросите пользователя ввести данные фигуры в диалоговом окне **Определить форму** данных.</span><span class="sxs-lookup"><span data-stu-id="23b57-108">Ask user to enter shape data in the **Define Shape Data** dialog box.</span></span>  <br/> |
|<span data-ttu-id="23b57-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="23b57-109">FALSE</span></span>  <br/> |<span data-ttu-id="23b57-110">Не просите пользователя вводить данные.</span><span class="sxs-lookup"><span data-stu-id="23b57-110">Do not ask user to enter data.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23b57-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="23b57-111">Remarks</span></span>

<span data-ttu-id="23b57-112">Значение в этой ячейке соответствует чековому окну **Ask on drop** в диалоговом окне **Определить** фигуру Данных (щелкните правой кнопкой мыши фигуру, указать на **данные,** а затем нажмите кнопку Определить данные **фигуры).**</span><span class="sxs-lookup"><span data-stu-id="23b57-112">The value in this cell corresponds to the **Ask on drop** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="23b57-113">Чтобы получить ссылку на ячейку Ask по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="23b57-113">To get a reference to the Ask cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23b57-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="23b57-114">Cell name:</span></span>  <br/> |<span data-ttu-id="23b57-115">Prop. *name*  . Проверьте, где prop.  *имя*  — это имя строки настраиваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="23b57-115">Prop. *name*  .Verify            where Prop.  *name*  is the name of the custom property row.</span></span>  <br/> |
   
<span data-ttu-id="23b57-116">Чтобы получить ссылку на ячейку Ask по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="23b57-116">To get a reference to the Ask cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23b57-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="23b57-117">Section index:</span></span>  <br/> |<span data-ttu-id="23b57-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="23b57-118">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="23b57-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="23b57-119">Row index:</span></span>  <br/> |<span data-ttu-id="23b57-120">**visRowProp**  +   *i,* *где i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="23b57-120">**visRowProp** +  *i*            where  *i*  = 0, 1, 2,...</span></span>  <br/> |
|<span data-ttu-id="23b57-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="23b57-121">Cell index:</span></span>  <br/> |<span data-ttu-id="23b57-122">**visCustPropsAsk**</span><span class="sxs-lookup"><span data-stu-id="23b57-122">**visCustPropsAsk**</span></span> <br/> |
   

