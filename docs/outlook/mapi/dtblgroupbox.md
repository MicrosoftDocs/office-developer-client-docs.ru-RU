---
title: DTBLGROUPBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLGROUPBOX
api_type:
- COM
ms.assetid: 5e444b62-d6b6-4cfc-8601-d34aa004c1e6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 324cfe9d7c412b3bb0e3150b8eec51aaeb6a0e93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438395"
---
# <a name="dtblgroupbox"></a><span data-ttu-id="be7b9-103">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="be7b9-103">DTBLGROUPBOX</span></span>

  
  
<span data-ttu-id="be7b9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be7b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be7b9-105">Описывает управление групповым полем, которое будет использоваться в диалоговом окне, построенного из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="be7b9-105">Describes a group box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="be7b9-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="be7b9-106">Header file:</span></span>  <br/> |<span data-ttu-id="be7b9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="be7b9-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="be7b9-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="be7b9-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="be7b9-109">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="be7b9-109">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a><span data-ttu-id="be7b9-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="be7b9-110">Members</span></span>

 <span data-ttu-id="be7b9-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="be7b9-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="be7b9-112">Положение в памяти строки символов, сопровождаемой групповой окне.</span><span class="sxs-lookup"><span data-stu-id="be7b9-112">Position in memory of the character string that accompanies the group box.</span></span> <span data-ttu-id="be7b9-113">Если отображается, метка отображается в верхней левой части окна.</span><span class="sxs-lookup"><span data-stu-id="be7b9-113">If displayed, the label appears on the top, left-hand side of the box.</span></span>
    
 <span data-ttu-id="be7b9-114">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="be7b9-114">**ulFlags**</span></span>
  
> <span data-ttu-id="be7b9-115">Bitmask флагов, используемых для обозначения формата метки, указанной членом **ulbLpszLabel.**</span><span class="sxs-lookup"><span data-stu-id="be7b9-115">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="be7b9-116">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="be7b9-116">The following flag can be set:</span></span> 
    
<span data-ttu-id="be7b9-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="be7b9-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="be7b9-118">Метка находится в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="be7b9-118">The label is in Unicode format.</span></span> <span data-ttu-id="be7b9-119">Если флаг MAPI_UNICODE не установлен, метка находится в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="be7b9-119">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="be7b9-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="be7b9-120">Remarks</span></span>

<span data-ttu-id="be7b9-121">Структура **DTBLGROUPBOX** описывает элемент управления групповой коробкой, который используется для визуального связываения других элементов управления в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="be7b9-121">A **DTBLGROUPBOX** structure describes a group box control that is used to visually associate other controls in the dialog box.</span></span> <span data-ttu-id="be7b9-122">Метод выделения включает в себя окружение других элементов управления полем.</span><span class="sxs-lookup"><span data-stu-id="be7b9-122">The highlighting technique involves surrounding the other controls by a box.</span></span> 
  
<span data-ttu-id="be7b9-123">Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="be7b9-123">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="be7b9-124">Сведения о реализации таблицы отображения см. в таблице [Implementing a Display Table.](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="be7b9-124">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="be7b9-125">См. также</span><span class="sxs-lookup"><span data-stu-id="be7b9-125">See also</span></span>



[<span data-ttu-id="be7b9-126">DTCTL</span><span class="sxs-lookup"><span data-stu-id="be7b9-126">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="be7b9-127">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="be7b9-127">MAPI Structures</span></span>](mapi-structures.md)

