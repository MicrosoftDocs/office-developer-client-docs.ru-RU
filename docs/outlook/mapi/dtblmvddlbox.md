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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420747"
---
# <a name="dtblmvddlbox"></a><span data-ttu-id="233c6-103">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="233c6-103">DTBLMVDDLBOX</span></span>

  
  
<span data-ttu-id="233c6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="233c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="233c6-105">Описывает отбрасывной список, который будет использоваться в диалоговом окне, построенного из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="233c6-105">Describes a drop-down list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="233c6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="233c6-106">Header file:</span></span>  <br/> |<span data-ttu-id="233c6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="233c6-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a><span data-ttu-id="233c6-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="233c6-108">Members</span></span>

 <span data-ttu-id="233c6-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="233c6-109">**ulFlags**</span></span>
  
> <span data-ttu-id="233c6-110">Зарезервировано; должно быть нулевой.</span><span class="sxs-lookup"><span data-stu-id="233c6-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="233c6-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="233c6-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="233c6-112">Тег свойства для многомерного свойства типа PT_MV_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="233c6-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span> <span data-ttu-id="233c6-113">Различные значения этого свойства отображаются в качестве отдельных записей в выпадаемом списке.</span><span class="sxs-lookup"><span data-stu-id="233c6-113">The different values of this property are displayed as distinct entries in the drop-down list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="233c6-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="233c6-114">Remarks</span></span>

<span data-ttu-id="233c6-115">Структура **DTBLMVDDLBOX** описывает многоценный список элементов только для чтения.</span><span class="sxs-lookup"><span data-stu-id="233c6-115">A **DTBLMVDDLBOX** structure describes a multi-valued drop-down list a read-only list of items.</span></span> <span data-ttu-id="233c6-116">С помощью многомерного списка выпаданий значения отображаются, когда пользователь щелкает по панели прокрутки.</span><span class="sxs-lookup"><span data-stu-id="233c6-116">By using a multi-valued drop-down list, values are displayed when a user clicks on a scroll bar.</span></span> 
  
<span data-ttu-id="233c6-117">Отображаемая информация поступает из свойства, обнаруженного в **члене ulMVPropTag.**</span><span class="sxs-lookup"><span data-stu-id="233c6-117">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="233c6-118">Не нужно читать из интерфейса свойства, связанного с таблицей отображения.</span><span class="sxs-lookup"><span data-stu-id="233c6-118">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="233c6-119">Кроме того, поскольку пользователи не могут сделать выбор из этих типов полей списков, данные не записаны в интерфейс свойства.</span><span class="sxs-lookup"><span data-stu-id="233c6-119">Also, because users are not able to make selections from these types of list boxes, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="233c6-120">Поддерживаются только свойства строк с несколькими значениями для многомерного отсевного списка; другие типы свойств с несколькими значениями не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="233c6-120">Only multi-valued string properties are supported for the multi-valued drop-down list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="233c6-121">Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="233c6-121">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="233c6-122">Сведения о реализации таблицы отображения см. в таблице [Implementing a Display Table.](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="233c6-122">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="233c6-123">См. также</span><span class="sxs-lookup"><span data-stu-id="233c6-123">See also</span></span>



[<span data-ttu-id="233c6-124">DTCTL</span><span class="sxs-lookup"><span data-stu-id="233c6-124">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="233c6-125">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="233c6-125">MAPI Structures</span></span>](mapi-structures.md)

