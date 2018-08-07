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
ms.openlocfilehash: 0de5bf5d5bb4d8c5606e97bdbc6e70493609a05f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808365"
---
# <a name="dtblmvlistbox"></a><span data-ttu-id="9c16e-103">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="9c16e-103">DTBLMVLISTBOX</span></span>

  
  
<span data-ttu-id="9c16e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9c16e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9c16e-105">Список, который будет отображаться в диалоговом окне, построенного из таблицы Отображаемое описание.</span><span class="sxs-lookup"><span data-stu-id="9c16e-105">Describes a multi-valued list that will be displayed in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9c16e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9c16e-106">Header file:</span></span>  <br/> |<span data-ttu-id="9c16e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9c16e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a><span data-ttu-id="9c16e-108">Members</span><span class="sxs-lookup"><span data-stu-id="9c16e-108">Members</span></span>

 <span data-ttu-id="9c16e-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="9c16e-109">**ulFlags**</span></span>
  
> <span data-ttu-id="9c16e-110">Зарезервировано; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="9c16e-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="9c16e-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="9c16e-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="9c16e-112">Свойство tag для многозначного свойства типа PT_MV_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="9c16e-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9c16e-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="9c16e-113">Remarks</span></span>

<span data-ttu-id="9c16e-114">Структура **DTBLMVLISTBOX** описывает стандартные список со списком только для чтения элементов.</span><span class="sxs-lookup"><span data-stu-id="9c16e-114">A **DTBLMVLISTBOX** structure describes a standard multi-valued list that has a read-only list of items.</span></span> <span data-ttu-id="9c16e-115">С помощью стандартных список, немедленно отображаются значения.</span><span class="sxs-lookup"><span data-stu-id="9c16e-115">By using a standard multi-valued list, the values are displayed immediately.</span></span> 
  
<span data-ttu-id="9c16e-116">Данные, который отображается, поступающие из свойства, обнаруженных в элементе **ulMVPropTag** .</span><span class="sxs-lookup"><span data-stu-id="9c16e-116">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="9c16e-117">Не является обязательным для чтения из интерфейса свойства, связанного с таблицей отображения.</span><span class="sxs-lookup"><span data-stu-id="9c16e-117">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="9c16e-118">Кроме того так как пользователи не смогут выбирать из этих типов списков, данные не записываются в интерфейсе свойство.</span><span class="sxs-lookup"><span data-stu-id="9c16e-118">Also, because users are not able to make selections from these types of lists, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="9c16e-119">Только те свойства, поддерживающий несколько значений string, поддерживаются для многозначного списка; другие типы многозначного свойства не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="9c16e-119">Only multi-valued string properties are supported for the multi-valued list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="9c16e-120">Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="9c16e-120">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="9c16e-121">Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.</span><span class="sxs-lookup"><span data-stu-id="9c16e-121">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9c16e-122">См. также</span><span class="sxs-lookup"><span data-stu-id="9c16e-122">See also</span></span>



[<span data-ttu-id="9c16e-123">DTCTL</span><span class="sxs-lookup"><span data-stu-id="9c16e-123">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="9c16e-124">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="9c16e-124">MAPI Structures</span></span>](mapi-structures.md)

