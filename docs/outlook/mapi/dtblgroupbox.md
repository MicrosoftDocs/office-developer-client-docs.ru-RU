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
ms.openlocfilehash: ef38893c9ad44556cc9220809b5e407f86fd2642
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576318"
---
# <a name="dtblgroupbox"></a><span data-ttu-id="51cef-103">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="51cef-103">DTBLGROUPBOX</span></span>

  
  
<span data-ttu-id="51cef-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51cef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51cef-105">Описывает элемент управления поля группы, которая будет использоваться в диалоговое окно, построенная на основе таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="51cef-105">Describes a group box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51cef-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="51cef-106">Header file:</span></span>  <br/> |<span data-ttu-id="51cef-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="51cef-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="51cef-108">Связанные макрос:</span><span class="sxs-lookup"><span data-stu-id="51cef-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="51cef-109">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="51cef-109">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a><span data-ttu-id="51cef-110">Members</span><span class="sxs-lookup"><span data-stu-id="51cef-110">Members</span></span>

 <span data-ttu-id="51cef-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="51cef-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="51cef-112">Положение в памяти, который описывается в поле Группа строки.</span><span class="sxs-lookup"><span data-stu-id="51cef-112">Position in memory of the character string that accompanies the group box.</span></span> <span data-ttu-id="51cef-113">Если отображается, метка отображается в верхней, левой части поле.</span><span class="sxs-lookup"><span data-stu-id="51cef-113">If displayed, the label appears on the top, left-hand side of the box.</span></span>
    
 <span data-ttu-id="51cef-114">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="51cef-114">**ulFlags**</span></span>
  
> <span data-ttu-id="51cef-115">Битовая маска флагов используется для назначения формат подписи, на который указывает член **ulbLpszLabel** .</span><span class="sxs-lookup"><span data-stu-id="51cef-115">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="51cef-116">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="51cef-116">The following flag can be set:</span></span> 
    
<span data-ttu-id="51cef-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="51cef-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="51cef-118">Метка имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="51cef-118">The label is in Unicode format.</span></span> <span data-ttu-id="51cef-119">Если флаг MAPI_UNICODE не установлен, в формате ANSI имеет название.</span><span class="sxs-lookup"><span data-stu-id="51cef-119">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="51cef-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="51cef-120">Remarks</span></span>

<span data-ttu-id="51cef-121">Структура **DTBLGROUPBOX** описывает элемент управления поля группы, который используется для визуально сопоставить другие элементы управления в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="51cef-121">A **DTBLGROUPBOX** structure describes a group box control that is used to visually associate other controls in the dialog box.</span></span> <span data-ttu-id="51cef-122">Метод выделения состоит из соседних другие элементы управления полем.</span><span class="sxs-lookup"><span data-stu-id="51cef-122">The highlighting technique involves surrounding the other controls by a box.</span></span> 
  
<span data-ttu-id="51cef-123">Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="51cef-123">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="51cef-124">Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.</span><span class="sxs-lookup"><span data-stu-id="51cef-124">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="51cef-125">См. также</span><span class="sxs-lookup"><span data-stu-id="51cef-125">See also</span></span>



[<span data-ttu-id="51cef-126">DTCTL</span><span class="sxs-lookup"><span data-stu-id="51cef-126">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="51cef-127">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="51cef-127">MAPI Structures</span></span>](mapi-structures.md)

