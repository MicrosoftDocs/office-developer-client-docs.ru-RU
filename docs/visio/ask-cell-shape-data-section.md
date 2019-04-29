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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426866"
---
# <a name="ask-cell-shape-data-section"></a><span data-ttu-id="f6c0c-103">Ask Cell (Shape Data Section)</span><span class="sxs-lookup"><span data-stu-id="f6c0c-103">Ask Cell (Shape Data Section)</span></span>

<span data-ttu-id="f6c0c-104">Определяет, запрашивается ли пользователю ввод данных фигуры для фигуры при создании экземпляра или дублировании или копировании фигуры.</span><span class="sxs-lookup"><span data-stu-id="f6c0c-104">Determines whether a user is queried to enter shape data for a shape when an instance is created or the shape is duplicated or copied.</span></span>
  
|<span data-ttu-id="f6c0c-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="f6c0c-105">**Value**</span></span>|<span data-ttu-id="f6c0c-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f6c0c-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f6c0c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="f6c0c-107">TRUE</span></span>  <br/> |<span data-ttu-id="f6c0c-108">ПоПросите пользователя ввести данные фигуры в диалоговом окне **Определение данных фигуры** .</span><span class="sxs-lookup"><span data-stu-id="f6c0c-108">Ask user to enter shape data in the **Define Shape Data** dialog box.</span></span>  <br/> |
|<span data-ttu-id="f6c0c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f6c0c-109">FALSE</span></span>  <br/> |<span data-ttu-id="f6c0c-110">Не рекомендуйте пользователю ввести данные.</span><span class="sxs-lookup"><span data-stu-id="f6c0c-110">Do not ask user to enter data.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6c0c-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="f6c0c-111">Remarks</span></span>

<span data-ttu-id="f6c0c-112">Значение в этой ячейке соответствует флажку **запрос на удаление** в диалоговом окне **Определение данных фигуры** (щелкните фигуру правой кнопкой мыши, наведите указатель мыши на пункт **данные**и выберите команду **определить данные фигуры**).</span><span class="sxs-lookup"><span data-stu-id="f6c0c-112">The value in this cell corresponds to the **Ask on drop** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="f6c0c-113">Чтобы получить ссылку на ячейку Ask по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="f6c0c-113">To get a reference to the Ask cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6c0c-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="f6c0c-114">Cell name:</span></span>  <br/> |<span data-ttu-id="f6c0c-115">Установите. *Name (имя* ). Проверьте, где prop.  *Name* имя строки настраиваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="f6c0c-115">Prop. *name*  .Verify            where Prop.  *name*  is the name of the custom property row.</span></span>  <br/> |
   
<span data-ttu-id="f6c0c-116">Чтобы получить ссылку на ячейку Ask по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="f6c0c-116">To get a reference to the Ask cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6c0c-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f6c0c-117">Section index:</span></span>  <br/> |<span data-ttu-id="f6c0c-118">**Виссектионпроп**</span><span class="sxs-lookup"><span data-stu-id="f6c0c-118">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="f6c0c-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f6c0c-119">Row index:</span></span>  <br/> |<span data-ttu-id="f6c0c-120">**висровпроп** +  *i* , где *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="f6c0c-120">**visRowProp** +  *i*            where  *i*  = 0, 1, 2,...</span></span>  <br/> |
|<span data-ttu-id="f6c0c-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f6c0c-121">Cell index:</span></span>  <br/> |<span data-ttu-id="f6c0c-122">**Вискустпропсаск**</span><span class="sxs-lookup"><span data-stu-id="f6c0c-122">**visCustPropsAsk**</span></span> <br/> |
   

