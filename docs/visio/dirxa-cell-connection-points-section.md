---
title: Ячейка DirX / A (раздел "Точки соединения")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251721
localization_priority: Normal
ms.assetid: 00d87b92-0da7-37d6-e7b5-23f350db0a9b
description: Определяет значение x-компонент для вектор Обязательное выравнивание совпадающих точки подключения. DirX аудио- и ячейки также используется для сориентироваться вложенные ветвь динамических соединителя. В этой ячейке принимает число с плавающей запятой.
ms.openlocfilehash: 49feba7cefbccc4efcbd04e8940c1f801563539e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813623"
---
# <a name="dirx--a-cell-connection-points-section"></a><span data-ttu-id="4e9fe-105">Ячейка DirX / A (раздел "Точки соединения")</span><span class="sxs-lookup"><span data-stu-id="4e9fe-105">DirX / A Cell (Connection Points Section)</span></span>

<span data-ttu-id="4e9fe-106">Определяет значение *x* -компонент для вектор Обязательное выравнивание совпадающих точки подключения.</span><span class="sxs-lookup"><span data-stu-id="4e9fe-106">Determines the  *x*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="4e9fe-107">DirX аудио- и ячейки также используется для сориентироваться вложенные ветвь динамических соединителя.</span><span class="sxs-lookup"><span data-stu-id="4e9fe-107">The DirX / A cell is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="4e9fe-108">В этой ячейке принимает число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="4e9fe-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4e9fe-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="4e9fe-109">Remarks</span></span>

<span data-ttu-id="4e9fe-110">Чтобы получить ссылку на DirX / ячейки по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="4e9fe-110">To get a reference to the DirX / A cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4e9fe-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="4e9fe-111">Cell name:</span></span>  <br/> | <span data-ttu-id="4e9fe-112">Connections.DirX [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="4e9fe-112">Connections.DirX[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="4e9fe-113">Чтобы получить ссылку на DirX / ячейки по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="4e9fe-113">To get a reference to the DirX / A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4e9fe-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="4e9fe-114">Section index:</span></span>  <br/> |<span data-ttu-id="4e9fe-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="4e9fe-115">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="4e9fe-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="4e9fe-116">Row index:</span></span>  <br/> |<span data-ttu-id="4e9fe-117">**visRowConnectionPts** +  *i* где *i* = 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="4e9fe-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2</span></span>  <br/> |
| <span data-ttu-id="4e9fe-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="4e9fe-118">Cell index:</span></span>  <br/> |<span data-ttu-id="4e9fe-119">**visCnnctDirX** (не только строк)           **visCnnctA** (расширенные строк)</span><span class="sxs-lookup"><span data-stu-id="4e9fe-119">**visCnnctDirX** (non-extended rows)           **visCnnctA** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="4e9fe-120">Сведения о не расширены и расширенного строк, в разделе точек подключения строки.</span><span class="sxs-lookup"><span data-stu-id="4e9fe-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

