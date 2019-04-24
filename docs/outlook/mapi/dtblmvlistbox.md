---
title: DTBLMVLISTBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVLISTBOX
api_type:
- COM
ms.assetid: 1c22f842-d0e7-44f0-a7d5-c9c2aa6b8820
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ae8f3ab28837bf0579549ead46c28477f815f35c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338278"
---
# <a name="dtblmvlistbox"></a><span data-ttu-id="2439a-103">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="2439a-103">DTBLMVLISTBOX</span></span>

  
  
<span data-ttu-id="2439a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2439a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2439a-105">Описывает Многозначный список, который будет отображаться в диалоговом окне, созданном из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="2439a-105">Describes a multi-valued list that will be displayed in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2439a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="2439a-106">Header file:</span></span>  <br/> |<span data-ttu-id="2439a-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="2439a-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a><span data-ttu-id="2439a-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="2439a-108">Members</span></span>

 <span data-ttu-id="2439a-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="2439a-109">**ulFlags**</span></span>
  
> <span data-ttu-id="2439a-110">Резервирования должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="2439a-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="2439a-111">**Улмвпроптаг**</span><span class="sxs-lookup"><span data-stu-id="2439a-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="2439a-112">Тег свойства с многозначным свойством типа ПТ_МВ_ТСТРИНГ.</span><span class="sxs-lookup"><span data-stu-id="2439a-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2439a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2439a-113">Remarks</span></span>

<span data-ttu-id="2439a-114">Структура **дтблмвлистбокс** описывает стандартный Многозначный список, содержащий список элементов, предназначенный только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2439a-114">A **DTBLMVLISTBOX** structure describes a standard multi-valued list that has a read-only list of items.</span></span> <span data-ttu-id="2439a-115">При использовании стандартного многозначного списка значения отображаются сразу.</span><span class="sxs-lookup"><span data-stu-id="2439a-115">By using a standard multi-valued list, the values are displayed immediately.</span></span> 
  
<span data-ttu-id="2439a-116">Отображаемые данные берутся из свойства, указанного в элементе **улмвпроптаг** .</span><span class="sxs-lookup"><span data-stu-id="2439a-116">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="2439a-117">Нет необходимости считывать сведения из интерфейса свойства, связанного с таблицей отображения.</span><span class="sxs-lookup"><span data-stu-id="2439a-117">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="2439a-118">Кроме того, так как пользователи не могут выбирать элементы из этих типов списков, данные не записываются в интерфейс свойств.</span><span class="sxs-lookup"><span data-stu-id="2439a-118">Also, because users are not able to make selections from these types of lists, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="2439a-119">В списке с несколькими значениями поддерживаются только многозначные строковые свойства; другие многозначные типы свойств не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="2439a-119">Only multi-valued string properties are supported for the multi-valued list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="2439a-120">Общие сведения о отображаемых таблицах приведены в разделе [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="2439a-120">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="2439a-121">Сведения о том, как реализовать таблицу отображения, можно найти [в статье реализация таблицы отображения](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="2439a-121">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2439a-122">См. также</span><span class="sxs-lookup"><span data-stu-id="2439a-122">See also</span></span>



[<span data-ttu-id="2439a-123">DTCTL</span><span class="sxs-lookup"><span data-stu-id="2439a-123">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="2439a-124">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="2439a-124">MAPI Structures</span></span>](mapi-structures.md)

