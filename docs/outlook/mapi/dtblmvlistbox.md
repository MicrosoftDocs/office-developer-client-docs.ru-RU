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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439704"
---
# <a name="dtblmvlistbox"></a><span data-ttu-id="360f4-103">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="360f4-103">DTBLMVLISTBOX</span></span>

  
  
<span data-ttu-id="360f4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="360f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="360f4-105">Описывает Многозначный список, который будет отображаться в диалоговом окне, созданном из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="360f4-105">Describes a multi-valued list that will be displayed in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="360f4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="360f4-106">Header file:</span></span>  <br/> |<span data-ttu-id="360f4-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="360f4-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a><span data-ttu-id="360f4-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="360f4-108">Members</span></span>

 <span data-ttu-id="360f4-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="360f4-109">**ulFlags**</span></span>
  
> <span data-ttu-id="360f4-110">Резервирования должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="360f4-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="360f4-111">**Улмвпроптаг**</span><span class="sxs-lookup"><span data-stu-id="360f4-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="360f4-112">Тег свойства с многозначным свойством типа ПТ_МВ_ТСТРИНГ.</span><span class="sxs-lookup"><span data-stu-id="360f4-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="360f4-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="360f4-113">Remarks</span></span>

<span data-ttu-id="360f4-114">Структура **дтблмвлистбокс** описывает стандартный Многозначный список, содержащий список элементов, предназначенный только для чтения.</span><span class="sxs-lookup"><span data-stu-id="360f4-114">A **DTBLMVLISTBOX** structure describes a standard multi-valued list that has a read-only list of items.</span></span> <span data-ttu-id="360f4-115">При использовании стандартного многозначного списка значения отображаются сразу.</span><span class="sxs-lookup"><span data-stu-id="360f4-115">By using a standard multi-valued list, the values are displayed immediately.</span></span> 
  
<span data-ttu-id="360f4-116">Отображаемые данные берутся из свойства, указанного в элементе **улмвпроптаг** .</span><span class="sxs-lookup"><span data-stu-id="360f4-116">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="360f4-117">Нет необходимости считывать сведения из интерфейса свойства, связанного с таблицей отображения.</span><span class="sxs-lookup"><span data-stu-id="360f4-117">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="360f4-118">Кроме того, так как пользователи не могут выбирать элементы из этих типов списков, данные не записываются в интерфейс свойств.</span><span class="sxs-lookup"><span data-stu-id="360f4-118">Also, because users are not able to make selections from these types of lists, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="360f4-119">В списке с несколькими значениями поддерживаются только многозначные строковые свойства; другие многозначные типы свойств не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="360f4-119">Only multi-valued string properties are supported for the multi-valued list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="360f4-120">Общие сведения о отображаемых таблицах приведены в разделе [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="360f4-120">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="360f4-121">Сведения о том, как реализовать таблицу отображения, можно найти [в статье реализация таблицы отображения](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="360f4-121">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="360f4-122">См. также</span><span class="sxs-lookup"><span data-stu-id="360f4-122">See also</span></span>



[<span data-ttu-id="360f4-123">DTCTL</span><span class="sxs-lookup"><span data-stu-id="360f4-123">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="360f4-124">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="360f4-124">MAPI Structures</span></span>](mapi-structures.md)

