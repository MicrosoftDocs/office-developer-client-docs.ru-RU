---
title: DTBLLABEL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLABEL
api_type:
- COM
ms.assetid: 5837facf-acd3-48fe-9610-f88085d99aef
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 28f6471f74fb0fcc4f7e2f4114f0790e1564e17e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808364"
---
# <a name="dtbllabel"></a><span data-ttu-id="ba414-103">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="ba414-103">DTBLLABEL</span></span>

  
  
<span data-ttu-id="ba414-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ba414-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ba414-105">Описание метки, который будет использоваться в диалоговом окне, построенного из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="ba414-105">Describes a label that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ba414-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ba414-106">Header file:</span></span>  <br/> |<span data-ttu-id="ba414-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ba414-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ba414-108">Связанные макросов</span><span class="sxs-lookup"><span data-stu-id="ba414-108">Related macro</span></span>  <br/> |[<span data-ttu-id="ba414-109">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="ba414-109">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a><span data-ttu-id="ba414-110">Members</span><span class="sxs-lookup"><span data-stu-id="ba414-110">Members</span></span>

 <span data-ttu-id="ba414-111">**ulbLpszLabelName**</span><span class="sxs-lookup"><span data-stu-id="ba414-111">**ulbLpszLabelName**</span></span>
  
> <span data-ttu-id="ba414-112">Положение в памяти метки строка символов.</span><span class="sxs-lookup"><span data-stu-id="ba414-112">Position in memory of the character string label.</span></span>
    
 <span data-ttu-id="ba414-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="ba414-113">**ulFlags**</span></span>
  
> <span data-ttu-id="ba414-114">Битовая маска флагов используется для назначения формат подписи, на который указывает член **ulbLpszLabelName** .</span><span class="sxs-lookup"><span data-stu-id="ba414-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="ba414-115">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="ba414-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="ba414-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ba414-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ba414-117">Метка имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="ba414-117">The label is in Unicode format.</span></span> <span data-ttu-id="ba414-118">Если флаг MAPI_UNICODE не установлен, в формате ANSI имеет название.</span><span class="sxs-lookup"><span data-stu-id="ba414-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ba414-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="ba414-119">Remarks</span></span>

<span data-ttu-id="ba414-120">Структура **DTBLLABEL** описывает текст элемента управления метки, который будет отображаться с другой тип элемента управления для добавления значение для этого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ba414-120">A **DTBLLABEL** structure describes a label control text that is displayed with another type of control to add meaning to that control.</span></span> <span data-ttu-id="ba414-121">Например изменить элементы управления располагаются рядом с пунктом меток для оповещения пользователя тип данных, который должен быть введен.</span><span class="sxs-lookup"><span data-stu-id="ba414-121">For example, most edit controls are positioned next to labels to inform the user of the type of information to be entered.</span></span> <span data-ttu-id="ba414-122">Некоторые элементы управления, такие как группа полей и кнопок-переключателей, нажмите и удерживайте собственные метки.</span><span class="sxs-lookup"><span data-stu-id="ba414-122">Some controls, such as group boxes and radio buttons, hold their own labels.</span></span> 
  
<span data-ttu-id="ba414-123">Метка может включать ускорителя Windows, определенные как символ, следующий амперсанд (&amp;).</span><span class="sxs-lookup"><span data-stu-id="ba414-123">The label can include a Windows accelerator, identified as the character following the ampersand (&amp;).</span></span> <span data-ttu-id="ba414-124">Нажав сочетание клавиш перемещает фокус в первом nonlabel nonbutton управления версиями в этой метки в таблице отображения.</span><span class="sxs-lookup"><span data-stu-id="ba414-124">Pressing the accelerator key puts the focus in the first nonlabel, nonbutton control following this label in the display table.</span></span>
  
<span data-ttu-id="ba414-125">Multiline меток не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ba414-125">There is no support for multiline labels.</span></span> <span data-ttu-id="ba414-126">Отображение нескольких строк требует нескольких метки.</span><span class="sxs-lookup"><span data-stu-id="ba414-126">Showing multiple lines requires multiple labels.</span></span>
  
<span data-ttu-id="ba414-127">Не поддерживается для использования в качестве элемента управления только для чтения изменить метку.</span><span class="sxs-lookup"><span data-stu-id="ba414-127">It is not possible to use a label as a read-only edit control.</span></span> <span data-ttu-id="ba414-128">Разница —, что элемента управления можно выделить и скопировать в то время как метка не удается.</span><span class="sxs-lookup"><span data-stu-id="ba414-128">The difference is that an edit control can be selected and copied whereas a label cannot.</span></span> 
  
<span data-ttu-id="ba414-129">Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="ba414-129">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="ba414-130">Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.</span><span class="sxs-lookup"><span data-stu-id="ba414-130">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ba414-131">См. также</span><span class="sxs-lookup"><span data-stu-id="ba414-131">See also</span></span>



[<span data-ttu-id="ba414-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="ba414-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="ba414-133">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="ba414-133">MAPI Structures</span></span>](mapi-structures.md)

