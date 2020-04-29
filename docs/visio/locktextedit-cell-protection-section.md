---
title: LockTextEdit Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm665
localization_priority: Normal
ms.assetid: d8de5fa4-826b-e869-4d9f-997361d05fd8
description: Блокирует текст фигуры, чтобы его нельзя было редактировать.
ms.openlocfilehash: f6e5176e3ab654b76c0641b8f642abcf6b1050dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404500"
---
# <a name="locktextedit-cell-protection-section"></a><span data-ttu-id="b69d7-103">LockTextEdit Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="b69d7-103">LockTextEdit Cell (Protection Section)</span></span>

<span data-ttu-id="b69d7-104">Блокирует текст фигуры, чтобы его нельзя было редактировать.</span><span class="sxs-lookup"><span data-stu-id="b69d7-104">Locks the text of a shape so that it cannot be edited.</span></span>
  
|<span data-ttu-id="b69d7-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="b69d7-105">**Value**</span></span>|<span data-ttu-id="b69d7-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b69d7-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b69d7-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b69d7-107">TRUE</span></span>  <br/> |<span data-ttu-id="b69d7-108">Текст не может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="b69d7-108">Text cannot be edited.</span></span>  <br/> |
| <span data-ttu-id="b69d7-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b69d7-109">FALSE</span></span>  <br/> | <span data-ttu-id="b69d7-110">Текст можно редактировать.</span><span class="sxs-lookup"><span data-stu-id="b69d7-110">Text can be edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b69d7-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="b69d7-111">Remarks</span></span>

<span data-ttu-id="b69d7-112">Вы по-прежнему можете форматировать текст, применяя стиль в диалоговом окне " **текст** " (на вкладке " **Главная** " щелкните стрелку **шрифта** ).</span><span class="sxs-lookup"><span data-stu-id="b69d7-112">You can still format text by applying a style in the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="b69d7-113">Чтобы получить ссылку на ячейку LockTextEdit по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="b69d7-113">To get a reference to the LockTextEdit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b69d7-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b69d7-114">Cell name:</span></span>  <br/> | <span data-ttu-id="b69d7-115">LockTextEdit</span><span class="sxs-lookup"><span data-stu-id="b69d7-115">LockTextEdit</span></span>  <br/> |
   
<span data-ttu-id="b69d7-116">Чтобы получить ссылку на ячейку LockTextEdit по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b69d7-116">To get a reference to the LockTextEdit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b69d7-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b69d7-117">Section index:</span></span>  <br/> |<span data-ttu-id="b69d7-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b69d7-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b69d7-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b69d7-119">Row index:</span></span>  <br/> |<span data-ttu-id="b69d7-120">**висровлокк**</span><span class="sxs-lookup"><span data-stu-id="b69d7-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="b69d7-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b69d7-121">Cell index:</span></span>  <br/> |<span data-ttu-id="b69d7-122">**вислокктекстедит**</span><span class="sxs-lookup"><span data-stu-id="b69d7-122">**visLockTextEdit**</span></span> <br/> |
   

