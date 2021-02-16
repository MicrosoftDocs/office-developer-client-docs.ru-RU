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
# <a name="dtblgroupbox"></a><span data-ttu-id="ca203-103">DTBLGROUPBOX</span><span class="sxs-lookup"><span data-stu-id="ca203-103">DTBLGROUPBOX</span></span>

  
  
<span data-ttu-id="ca203-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca203-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca203-105">Описание группового окна, который будет использоваться в диалоговом окне, построенного из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="ca203-105">Describes a group box control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ca203-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ca203-106">Header file:</span></span>  <br/> |<span data-ttu-id="ca203-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ca203-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ca203-108">Связанный макрос:</span><span class="sxs-lookup"><span data-stu-id="ca203-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="ca203-109">SizedDtblGroupBox</span><span class="sxs-lookup"><span data-stu-id="ca203-109">SizedDtblGroupBox</span></span>](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a><span data-ttu-id="ca203-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="ca203-110">Members</span></span>

 <span data-ttu-id="ca203-111">**ulbLpszLabel**</span><span class="sxs-lookup"><span data-stu-id="ca203-111">**ulbLpszLabel**</span></span>
  
> <span data-ttu-id="ca203-112">Положение в памяти строки символа, которая сопровождает поле группы.</span><span class="sxs-lookup"><span data-stu-id="ca203-112">Position in memory of the character string that accompanies the group box.</span></span> <span data-ttu-id="ca203-113">Если она отображается, метка отображается в верхней левой части окна.</span><span class="sxs-lookup"><span data-stu-id="ca203-113">If displayed, the label appears on the top, left-hand side of the box.</span></span>
    
 <span data-ttu-id="ca203-114">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="ca203-114">**ulFlags**</span></span>
  
> <span data-ttu-id="ca203-115">Битовая метка флагов, используемая для обозначения формата метки, на который указывает элемент **ulbLpszLabel.**</span><span class="sxs-lookup"><span data-stu-id="ca203-115">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabel** member.</span></span> <span data-ttu-id="ca203-116">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="ca203-116">The following flag can be set:</span></span> 
    
<span data-ttu-id="ca203-117">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ca203-117">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ca203-118">Метка имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="ca203-118">The label is in Unicode format.</span></span> <span data-ttu-id="ca203-119">Если флаг MAPI_UNICODE не установлен, метка будет в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="ca203-119">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ca203-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="ca203-120">Remarks</span></span>

<span data-ttu-id="ca203-121">Структура **DTBLGROUPBOX** описывает элемент управления "Групповое поле", используемый для визуального связываия других элементов управления в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="ca203-121">A **DTBLGROUPBOX** structure describes a group box control that is used to visually associate other controls in the dialog box.</span></span> <span data-ttu-id="ca203-122">Метод выделения включает в себя окружение других элементов управления полем.</span><span class="sxs-lookup"><span data-stu-id="ca203-122">The highlighting technique involves surrounding the other controls by a box.</span></span> 
  
<span data-ttu-id="ca203-123">Обзор таблиц отображения см. в [таблице отображения.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="ca203-123">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="ca203-124">Сведения о реализации таблицы отображения см. в таблице ["Реализация таблицы отображения".](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="ca203-124">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ca203-125">См. также</span><span class="sxs-lookup"><span data-stu-id="ca203-125">See also</span></span>



[<span data-ttu-id="ca203-126">DTCTL</span><span class="sxs-lookup"><span data-stu-id="ca203-126">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="ca203-127">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="ca203-127">MAPI Structures</span></span>](mapi-structures.md)

