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
ms.openlocfilehash: aa3345740c534b5ff156f062e731c98bc6164eed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410688"
---
# <a name="dtbllabel"></a><span data-ttu-id="407ae-103">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="407ae-103">DTBLLABEL</span></span>

  
  
<span data-ttu-id="407ae-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="407ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="407ae-105">Описывает метку, которая будет использоваться в диалоговом окне, созданном из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="407ae-105">Describes a label that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="407ae-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="407ae-106">Header file:</span></span>  <br/> |<span data-ttu-id="407ae-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="407ae-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="407ae-108">Связанный макрос</span><span class="sxs-lookup"><span data-stu-id="407ae-108">Related macro</span></span>  <br/> |[<span data-ttu-id="407ae-109">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="407ae-109">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a><span data-ttu-id="407ae-110">Members</span><span class="sxs-lookup"><span data-stu-id="407ae-110">Members</span></span>

 <span data-ttu-id="407ae-111">**Улблпсзлабелнаме**</span><span class="sxs-lookup"><span data-stu-id="407ae-111">**ulbLpszLabelName**</span></span>
  
> <span data-ttu-id="407ae-112">Позиция в памяти метки строки символов.</span><span class="sxs-lookup"><span data-stu-id="407ae-112">Position in memory of the character string label.</span></span>
    
 <span data-ttu-id="407ae-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="407ae-113">**ulFlags**</span></span>
  
> <span data-ttu-id="407ae-114">Битовая маска флагов, используемых для обозначения формата метки, на который указывает элемент **улблпсзлабелнаме** .</span><span class="sxs-lookup"><span data-stu-id="407ae-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="407ae-115">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="407ae-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="407ae-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="407ae-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="407ae-117">Метка имеет формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="407ae-117">The label is in Unicode format.</span></span> <span data-ttu-id="407ae-118">Если флаг МАПИ_УНИКОДЕ не установлен, метка имеет формат ANSI.</span><span class="sxs-lookup"><span data-stu-id="407ae-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="407ae-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="407ae-119">Remarks</span></span>

<span data-ttu-id="407ae-120">Структура **дтбллабел** описывает текст элемента управления Label, который отображается с помощью другого типа элементов управления для добавления смысла к этому элементу управления.</span><span class="sxs-lookup"><span data-stu-id="407ae-120">A **DTBLLABEL** structure describes a label control text that is displayed with another type of control to add meaning to that control.</span></span> <span data-ttu-id="407ae-121">Например, большинство элементов управления для редактирования располагаются рядом с метками для информирования пользователя о типе вводимой информации.</span><span class="sxs-lookup"><span data-stu-id="407ae-121">For example, most edit controls are positioned next to labels to inform the user of the type of information to be entered.</span></span> <span data-ttu-id="407ae-122">Некоторые элементы управления, например поля групп и переключатели, содержат свои собственные метки.</span><span class="sxs-lookup"><span data-stu-id="407ae-122">Some controls, such as group boxes and radio buttons, hold their own labels.</span></span> 
  
<span data-ttu-id="407ae-123">Метка может содержать ускоритель Windows, обозначенный символом после амперсанда (&amp;).</span><span class="sxs-lookup"><span data-stu-id="407ae-123">The label can include a Windows accelerator, identified as the character following the ampersand (&amp;).</span></span> <span data-ttu-id="407ae-124">Нажатие клавиши вызова помещает фокус в первый неэлементный элемент управления, не являющийся элементом управления, который следует за этой меткой в таблице отображения.</span><span class="sxs-lookup"><span data-stu-id="407ae-124">Pressing the accelerator key puts the focus in the first nonlabel, nonbutton control following this label in the display table.</span></span>
  
<span data-ttu-id="407ae-125">Многострочные метки не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="407ae-125">There is no support for multiline labels.</span></span> <span data-ttu-id="407ae-126">Для отображения нескольких строк требуется несколько меток.</span><span class="sxs-lookup"><span data-stu-id="407ae-126">Showing multiple lines requires multiple labels.</span></span>
  
<span data-ttu-id="407ae-127">Невозможно использовать метку в качестве элемента управления редактирования "только для чтения".</span><span class="sxs-lookup"><span data-stu-id="407ae-127">It is not possible to use a label as a read-only edit control.</span></span> <span data-ttu-id="407ae-128">Различие заключается в том, что элемент управления редактирования можно выбирать и копировать, в то время как метка не может быть.</span><span class="sxs-lookup"><span data-stu-id="407ae-128">The difference is that an edit control can be selected and copied whereas a label cannot.</span></span> 
  
<span data-ttu-id="407ae-129">Общие сведения о отображаемых таблицах приведены в разделе [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="407ae-129">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="407ae-130">Сведения о том, как реализовать таблицу отображения, можно найти [в статье реализация таблицы отображения](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="407ae-130">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="407ae-131">См. также</span><span class="sxs-lookup"><span data-stu-id="407ae-131">See also</span></span>



[<span data-ttu-id="407ae-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="407ae-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="407ae-133">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="407ae-133">MAPI Structures</span></span>](mapi-structures.md)

