---
title: LockFromGroupFormat Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 3daeb4704a33ba836cf82c9ab3517c6ca6be8db7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426060"
---
# <a name="lockfromgroupformat-cell-protection-section"></a><span data-ttu-id="01f03-102">LockFromGroupFormat Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="01f03-102">LockFromGroupFormat Cell (Protection Section)</span></span>

<span data-ttu-id="01f03-103">Блокирует изменение формата в групповую форму от распространения до его подформ, при этом позволяя пользователям напрямую форматировать выбранные подформы.</span><span class="sxs-lookup"><span data-stu-id="01f03-103">Blocks format changes to a group shape from being propagated to its sub-shapes, while still allowing users to format selected sub-shapes directly.</span></span> 
  
<span data-ttu-id="01f03-104">Значение ячейки LockFromGroupFormat соответствует параметру "От группового форматирования" в диалоговом окне **Protection.** </span><span class="sxs-lookup"><span data-stu-id="01f03-104">The value of the LockFromGroupFormat cell corresponds to the **From group formatting** check box setting in the **Protection** dialog box.</span></span> 
  
<span data-ttu-id="01f03-105">Чтобы сослаться на ячейку LockFromGroupFormat по имени из другой формулы или из программы, используя свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="01f03-105">To refer to the LockFromGroupFormat cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01f03-106">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="01f03-106">Cell name:</span></span>  <br/> |<span data-ttu-id="01f03-107">LockFromGroupFormat</span><span class="sxs-lookup"><span data-stu-id="01f03-107">LockFromGroupFormat</span></span>  <br/> |
   
<span data-ttu-id="01f03-108">Чтобы сослаться на ячейку LockFromGroupFormat по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="01f03-108">To refer to the LockFromGroupFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01f03-109">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="01f03-109">Section index:</span></span>  <br/> |<span data-ttu-id="01f03-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="01f03-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="01f03-111">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="01f03-111">Row index:</span></span>  <br/> |<span data-ttu-id="01f03-112">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="01f03-112">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="01f03-113">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="01f03-113">Cell index:</span></span>  <br/> |<span data-ttu-id="01f03-114">**visLockFromGroupFormat**</span><span class="sxs-lookup"><span data-stu-id="01f03-114">**visLockFromGroupFormat**</span></span> <br/> |
   
<span data-ttu-id="01f03-115">Значение по умолчанию для ячейки — 0 (False).</span><span class="sxs-lookup"><span data-stu-id="01f03-115">The default value for the cell is 0 (False).</span></span>
  

