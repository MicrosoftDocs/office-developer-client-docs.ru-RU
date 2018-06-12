---
title: Ячейка LockTextEdit (раздел Защита)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm665
localization_priority: Normal
ms.assetid: d8de5fa4-826b-e869-4d9f-997361d05fd8
description: Блокирует текст фигуры, не может быть изменен.
ms.openlocfilehash: 7f8800f0b260e808a46ec123d27784f3dd92e847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814153"
---
# <a name="locktextedit-cell-protection-section"></a><span data-ttu-id="209e5-103">Ячейка LockTextEdit (раздел Защита)</span><span class="sxs-lookup"><span data-stu-id="209e5-103">LockTextEdit Cell (Protection Section)</span></span>

<span data-ttu-id="209e5-104">Блокирует текст фигуры, не может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="209e5-104">Locks the text of a shape so that it cannot be edited.</span></span>
  
|<span data-ttu-id="209e5-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="209e5-105">**Value**</span></span>|<span data-ttu-id="209e5-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="209e5-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="209e5-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="209e5-107">TRUE</span></span>  <br/> |<span data-ttu-id="209e5-108">Невозможно изменить текст.</span><span class="sxs-lookup"><span data-stu-id="209e5-108">Text cannot be edited.</span></span>  <br/> |
| <span data-ttu-id="209e5-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="209e5-109">FALSE</span></span>  <br/> | <span data-ttu-id="209e5-110">Текст можно редактировать.</span><span class="sxs-lookup"><span data-stu-id="209e5-110">Text can be edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="209e5-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="209e5-111">Remarks</span></span>

<span data-ttu-id="209e5-112">По-прежнему можно отформатировать текст с применением стилей в диалоговое окно " **текст** " (на вкладке **Главная** щелкните стрелку **шрифтов** ).</span><span class="sxs-lookup"><span data-stu-id="209e5-112">You can still format text by applying a style in the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="209e5-113">Чтобы получить ссылку на ячейку LockTextEdit по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="209e5-113">To get a reference to the LockTextEdit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="209e5-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="209e5-114">Cell name:</span></span>  <br/> | <span data-ttu-id="209e5-115">LockTextEdit</span><span class="sxs-lookup"><span data-stu-id="209e5-115">LockTextEdit</span></span>  <br/> |
   
<span data-ttu-id="209e5-116">Для получения ссылки на ячейки LockTextEdit по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="209e5-116">To get a reference to the LockTextEdit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="209e5-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="209e5-117">Section index:</span></span>  <br/> |<span data-ttu-id="209e5-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="209e5-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="209e5-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="209e5-119">Row index:</span></span>  <br/> |<span data-ttu-id="209e5-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="209e5-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="209e5-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="209e5-121">Cell index:</span></span>  <br/> |<span data-ttu-id="209e5-122">**visLockTextEdit**</span><span class="sxs-lookup"><span data-stu-id="209e5-122">**visLockTextEdit**</span></span> <br/> |
   

