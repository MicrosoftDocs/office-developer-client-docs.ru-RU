---
title: DTBLMVDDLBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVDDLBOX
api_type:
- COM
ms.assetid: 0e6283dc-9a08-460f-9400-03f0ceb4081c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 33b4fd87f33c26db15e1a6a28f077c393168db91
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325762"
---
# <a name="dtblmvddlbox"></a><span data-ttu-id="5f0c9-103">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="5f0c9-103">DTBLMVDDLBOX</span></span>

  
  
<span data-ttu-id="5f0c9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f0c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f0c9-105">Описывает раскрывающийся список, который будет использоваться в диалоговом окне, созданном из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="5f0c9-105">Describes a drop-down list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5f0c9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5f0c9-106">Header file:</span></span>  <br/> |<span data-ttu-id="5f0c9-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="5f0c9-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a><span data-ttu-id="5f0c9-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="5f0c9-108">Members</span></span>

 <span data-ttu-id="5f0c9-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="5f0c9-109">**ulFlags**</span></span>
  
> <span data-ttu-id="5f0c9-110">Резервирования должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="5f0c9-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="5f0c9-111">**Улмвпроптаг**</span><span class="sxs-lookup"><span data-stu-id="5f0c9-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="5f0c9-112">Тег свойства с многозначным свойством типа ПТ_МВ_ТСТРИНГ.</span><span class="sxs-lookup"><span data-stu-id="5f0c9-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span> <span data-ttu-id="5f0c9-113">Различные значения этого свойства отображаются в раскрывающемся списке как отдельные записи.</span><span class="sxs-lookup"><span data-stu-id="5f0c9-113">The different values of this property are displayed as distinct entries in the drop-down list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5f0c9-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="5f0c9-114">Remarks</span></span>

<span data-ttu-id="5f0c9-115">Структура **дтблмвддлбокс** описывает раскрывающийся список, поддерживающий несколько значений, список элементов, предназначенный только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5f0c9-115">A **DTBLMVDDLBOX** structure describes a multi-valued drop-down list a read-only list of items.</span></span> <span data-ttu-id="5f0c9-116">При использовании раскрывающегося списка с несколькими значениями значения отображаются, когда пользователь нажимает полосу прокрутки.</span><span class="sxs-lookup"><span data-stu-id="5f0c9-116">By using a multi-valued drop-down list, values are displayed when a user clicks on a scroll bar.</span></span> 
  
<span data-ttu-id="5f0c9-117">Отображаемые данные берутся из свойства, указанного в элементе **улмвпроптаг** .</span><span class="sxs-lookup"><span data-stu-id="5f0c9-117">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="5f0c9-118">Нет необходимости считывать сведения из интерфейса свойства, связанного с таблицей отображения.</span><span class="sxs-lookup"><span data-stu-id="5f0c9-118">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="5f0c9-119">Кроме того, так как пользователи не могут выбирать из этих типов списков, данные не записываются в интерфейс свойств.</span><span class="sxs-lookup"><span data-stu-id="5f0c9-119">Also, because users are not able to make selections from these types of list boxes, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="5f0c9-120">В раскрывающемся списке с несколькими значениями поддерживаются только многозначные строковые свойства; другие многозначные типы свойств не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="5f0c9-120">Only multi-valued string properties are supported for the multi-valued drop-down list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="5f0c9-121">Общие сведения о отображаемых таблицах приведены в разделе [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="5f0c9-121">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="5f0c9-122">Сведения о том, как реализовать таблицу отображения, можно найти [в статье реализация таблицы отображения](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="5f0c9-122">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5f0c9-123">См. также</span><span class="sxs-lookup"><span data-stu-id="5f0c9-123">See also</span></span>



[<span data-ttu-id="5f0c9-124">DTCTL</span><span class="sxs-lookup"><span data-stu-id="5f0c9-124">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="5f0c9-125">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="5f0c9-125">MAPI Structures</span></span>](mapi-structures.md)

