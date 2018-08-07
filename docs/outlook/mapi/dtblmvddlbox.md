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
ms.openlocfilehash: ede0a448a32565446e614fc2d14f2a72a9549dad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808367"
---
# <a name="dtblmvddlbox"></a><span data-ttu-id="27085-103">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="27085-103">DTBLMVDDLBOX</span></span>

  
  
<span data-ttu-id="27085-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="27085-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="27085-105">Описывает раскрывающегося списка, который будет использоваться в диалоговом окне, построенного из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="27085-105">Describes a drop-down list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="27085-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="27085-106">Header file:</span></span>  <br/> |<span data-ttu-id="27085-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27085-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a><span data-ttu-id="27085-108">Members</span><span class="sxs-lookup"><span data-stu-id="27085-108">Members</span></span>

 <span data-ttu-id="27085-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="27085-109">**ulFlags**</span></span>
  
> <span data-ttu-id="27085-110">Зарезервировано; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="27085-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="27085-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="27085-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="27085-112">Свойство tag для многозначного свойства типа PT_MV_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="27085-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span> <span data-ttu-id="27085-113">Различные значения этого свойства отображаются в виде отдельных записей в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="27085-113">The different values of this property are displayed as distinct entries in the drop-down list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="27085-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="27085-114">Remarks</span></span>

<span data-ttu-id="27085-115">Структура **DTBLMVDDLBOX** описывает многозначные раскрывающегося списка только для чтения список элементов.</span><span class="sxs-lookup"><span data-stu-id="27085-115">A **DTBLMVDDLBOX** structure describes a multi-valued drop-down list a read-only list of items.</span></span> <span data-ttu-id="27085-116">С помощью многозначные раскрывающегося списка, значения отображаются при щелчке полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="27085-116">By using a multi-valued drop-down list, values are displayed when a user clicks on a scroll bar.</span></span> 
  
<span data-ttu-id="27085-117">Данные, который отображается, поступающие из свойства, обнаруженных в элементе **ulMVPropTag** .</span><span class="sxs-lookup"><span data-stu-id="27085-117">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="27085-118">Не является обязательным для чтения из интерфейса свойства, связанного с таблицей отображения.</span><span class="sxs-lookup"><span data-stu-id="27085-118">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="27085-119">Кроме того так как пользователи не могут выбирать из этих типов списков, данные не записываются в интерфейсе свойство.</span><span class="sxs-lookup"><span data-stu-id="27085-119">Also, because users are not able to make selections from these types of list boxes, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="27085-120">Поддерживаются только те свойства, поддерживающий несколько значений string для многозначные раскрывающегося списка; другие типы многозначного свойства не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="27085-120">Only multi-valued string properties are supported for the multi-valued drop-down list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="27085-121">Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="27085-121">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="27085-122">Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.</span><span class="sxs-lookup"><span data-stu-id="27085-122">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="27085-123">См. также</span><span class="sxs-lookup"><span data-stu-id="27085-123">See also</span></span>



[<span data-ttu-id="27085-124">DTCTL</span><span class="sxs-lookup"><span data-stu-id="27085-124">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="27085-125">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="27085-125">MAPI Structures</span></span>](mapi-structures.md)

