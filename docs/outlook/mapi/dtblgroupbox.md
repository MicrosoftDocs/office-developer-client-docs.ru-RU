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
# <a name="dtblgroupbox"></a><span data-ttu-id="ff1b5-103">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="ff1b5-103">DTBLGROUPBOX</span></span>

  
  
<span data-ttu-id="ff1b5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff1b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff1b5-105">Описывает элемент управления "Группа", который будет использоваться в диалоговом окне, созданном из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="ff1b5-105">Describes a group box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ff1b5-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ff1b5-106">Header file:</span></span>  <br/> |<span data-ttu-id="ff1b5-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="ff1b5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ff1b5-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="ff1b5-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="ff1b5-109">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="ff1b5-109">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a><span data-ttu-id="ff1b5-110">Members</span><span class="sxs-lookup"><span data-stu-id="ff1b5-110">Members</span></span>

 <span data-ttu-id="ff1b5-111">**Улблпсзлабел**</span><span class="sxs-lookup"><span data-stu-id="ff1b5-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="ff1b5-112">Позиция в памяти строки символов, сопровождающей поле группы.</span><span class="sxs-lookup"><span data-stu-id="ff1b5-112">Position in memory of the character string that accompanies the group box.</span></span> <span data-ttu-id="ff1b5-113">Если отображается, метка отображается в верхней части поля слева.</span><span class="sxs-lookup"><span data-stu-id="ff1b5-113">If displayed, the label appears on the top, left-hand side of the box.</span></span>
    
 <span data-ttu-id="ff1b5-114">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="ff1b5-114">**ulFlags**</span></span>
  
> <span data-ttu-id="ff1b5-115">Битовая маска флагов, используемых для обозначения формата метки, на который указывает элемент **улблпсзлабел** .</span><span class="sxs-lookup"><span data-stu-id="ff1b5-115">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="ff1b5-116">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="ff1b5-116">The following flag can be set:</span></span> 
    
<span data-ttu-id="ff1b5-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ff1b5-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ff1b5-118">Метка имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="ff1b5-118">The label is in Unicode format.</span></span> <span data-ttu-id="ff1b5-119">Если флаг МАПИ_УНИКОДЕ не установлен, метка имеет формат ANSI.</span><span class="sxs-lookup"><span data-stu-id="ff1b5-119">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ff1b5-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="ff1b5-120">Remarks</span></span>

<span data-ttu-id="ff1b5-121">Структура **дтблграупбокс** описывает элемент управления "Группа", который используется для визуального связывания других элементов управления в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="ff1b5-121">A **DTBLGROUPBOX** structure describes a group box control that is used to visually associate other controls in the dialog box.</span></span> <span data-ttu-id="ff1b5-122">Метод выделения включает окружающие другие элементы управления полем.</span><span class="sxs-lookup"><span data-stu-id="ff1b5-122">The highlighting technique involves surrounding the other controls by a box.</span></span> 
  
<span data-ttu-id="ff1b5-123">Общие сведения о отображаемых таблицах приведены в разделе [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="ff1b5-123">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="ff1b5-124">Сведения о том, как реализовать таблицу отображения, можно найти [в статье реализация таблицы отображения](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="ff1b5-124">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ff1b5-125">См. также</span><span class="sxs-lookup"><span data-stu-id="ff1b5-125">See also</span></span>



[<span data-ttu-id="ff1b5-126">DTCTL</span><span class="sxs-lookup"><span data-stu-id="ff1b5-126">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="ff1b5-127">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="ff1b5-127">MAPI Structures</span></span>](mapi-structures.md)

