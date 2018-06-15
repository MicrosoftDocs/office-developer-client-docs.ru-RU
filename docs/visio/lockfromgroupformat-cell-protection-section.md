---
title: Ячейка LockFromGroupFormat (раздел Защита)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 95633ab7a4127564fef65062bcf328d4364ebd86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19814145"
---
# <a name="lockfromgroupformat-cell-protection-section"></a><span data-ttu-id="2eb3b-102">Ячейка LockFromGroupFormat (раздел Защита)</span><span class="sxs-lookup"><span data-stu-id="2eb3b-102">LockFromGroupFormat Cell (Protection Section)</span></span>

<span data-ttu-id="2eb3b-103">Блоки изменений формата групповой фигуры распространения на вложенные фигуры, при этом позволяя пользователям напрямую форматирование указанных вложенных фигур.</span><span class="sxs-lookup"><span data-stu-id="2eb3b-103">Blocks format changes to a group shape from being propagated to its sub-shapes, while still allowing users to format selected sub-shapes directly.</span></span> 
  
<span data-ttu-id="2eb3b-104">Значение ячейки LockFromGroupFormat соответствует параметру **из группы форматирования** флажок в диалоговом окне " **Защита** ".</span><span class="sxs-lookup"><span data-stu-id="2eb3b-104">The value of the LockFromGroupFormat cell corresponds to the **From group formatting** check box setting in the **Protection** dialog box.</span></span> 
  
<span data-ttu-id="2eb3b-105">Для ссылки на ячейки LockFromGroupFormat по имени из другой формулы или из программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="2eb3b-105">To refer to the LockFromGroupFormat cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2eb3b-106">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="2eb3b-106">Cell name:</span></span>  <br/> |<span data-ttu-id="2eb3b-107">LockFromGroupFormat</span><span class="sxs-lookup"><span data-stu-id="2eb3b-107">LockFromGroupFormat</span></span>  <br/> |
   
<span data-ttu-id="2eb3b-108">Для ссылки на ячейки LockFromGroupFormat по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="2eb3b-108">To refer to the LockFromGroupFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2eb3b-109">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="2eb3b-109">Section index:</span></span>  <br/> |<span data-ttu-id="2eb3b-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2eb3b-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="2eb3b-111">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="2eb3b-111">Row index:</span></span>  <br/> |<span data-ttu-id="2eb3b-112">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="2eb3b-112">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="2eb3b-113">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="2eb3b-113">Cell index:</span></span>  <br/> |<span data-ttu-id="2eb3b-114">**visLockFromGroupFormat**</span><span class="sxs-lookup"><span data-stu-id="2eb3b-114">**visLockFromGroupFormat**</span></span> <br/> |
   
<span data-ttu-id="2eb3b-115">Значение по умолчанию для ячейки равно 0 (False).</span><span class="sxs-lookup"><span data-stu-id="2eb3b-115">The default value for the cell is 0 (False).</span></span>
  

