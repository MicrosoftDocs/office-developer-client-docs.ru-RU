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
# <a name="dtbllabel"></a><span data-ttu-id="e2afe-103">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="e2afe-103">DTBLLABEL</span></span>

  
  
<span data-ttu-id="e2afe-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2afe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2afe-105">Описывает метку, которая будет использоваться в диалоговом окне, построенной из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="e2afe-105">Describes a label that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e2afe-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e2afe-106">Header file:</span></span>  <br/> |<span data-ttu-id="e2afe-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e2afe-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e2afe-108">Связанный макрос</span><span class="sxs-lookup"><span data-stu-id="e2afe-108">Related macro</span></span>  <br/> |[<span data-ttu-id="e2afe-109">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="e2afe-109">SizedDtblLabel</span></span>](sizeddtbllabel.md) <br/> |
   
```cpp
typedef struct _DTBLLABEL
{
  ULONG ulbLpszLabelName;
  ULONG ulFlags;
} DTBLLABEL, FAR *LPDTBLLABEL;

```

## <a name="members"></a><span data-ttu-id="e2afe-110">"Участники"</span><span class="sxs-lookup"><span data-stu-id="e2afe-110">Members</span></span>

 <span data-ttu-id="e2afe-111">**ulbLpszLabelName**</span><span class="sxs-lookup"><span data-stu-id="e2afe-111">**ulbLpszLabelName**</span></span>
  
> <span data-ttu-id="e2afe-112">Положение в памяти метки строки символов.</span><span class="sxs-lookup"><span data-stu-id="e2afe-112">Position in memory of the character string label.</span></span>
    
 <span data-ttu-id="e2afe-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="e2afe-113">**ulFlags**</span></span>
  
> <span data-ttu-id="e2afe-114">Bitmask флагов, используемых для обозначения формата метки, указанной членом **ulbLpszLabelName.**</span><span class="sxs-lookup"><span data-stu-id="e2afe-114">Bitmask of flags used to designate the format of the label pointed to by the **ulbLpszLabelName** member.</span></span> <span data-ttu-id="e2afe-115">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="e2afe-115">The following flag can be set:</span></span> 
    
<span data-ttu-id="e2afe-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e2afe-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e2afe-117">Метка находится в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="e2afe-117">The label is in Unicode format.</span></span> <span data-ttu-id="e2afe-118">Если флаг MAPI_UNICODE не установлен, метка находится в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="e2afe-118">If the MAPI_UNICODE flag is not set, the label is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e2afe-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="e2afe-119">Remarks</span></span>

<span data-ttu-id="e2afe-120">Структура **DTBLLABEL** описывает текст управления меткой, отображаемый с другим типом управления, чтобы добавить значение к этому контролю.</span><span class="sxs-lookup"><span data-stu-id="e2afe-120">A **DTBLLABEL** structure describes a label control text that is displayed with another type of control to add meaning to that control.</span></span> <span data-ttu-id="e2afe-121">Например, большинство элементов управления редактированием находятся рядом с метами, чтобы информировать пользователя о типе вступаемой информации.</span><span class="sxs-lookup"><span data-stu-id="e2afe-121">For example, most edit controls are positioned next to labels to inform the user of the type of information to be entered.</span></span> <span data-ttu-id="e2afe-122">Некоторые элементы управления, такие как групповые ящики и кнопки радиосвязи, удерживают собственные метки.</span><span class="sxs-lookup"><span data-stu-id="e2afe-122">Some controls, such as group boxes and radio buttons, hold their own labels.</span></span> 
  
<span data-ttu-id="e2afe-123">Метка может включать ускоритель Windows, идентифицированный в качестве символа, следующего за ampersand ( &amp; ).</span><span class="sxs-lookup"><span data-stu-id="e2afe-123">The label can include a Windows accelerator, identified as the character following the ampersand (&amp;).</span></span> <span data-ttu-id="e2afe-124">При нажатии клавиши акселератора фокусируется в первом элементе управления nonlabel, nonbutton после этого метки в таблице отображения.</span><span class="sxs-lookup"><span data-stu-id="e2afe-124">Pressing the accelerator key puts the focus in the first nonlabel, nonbutton control following this label in the display table.</span></span>
  
<span data-ttu-id="e2afe-125">Поддержка многолинейных меток не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e2afe-125">There is no support for multiline labels.</span></span> <span data-ttu-id="e2afe-126">Отображение нескольких строк требует нескольких меток.</span><span class="sxs-lookup"><span data-stu-id="e2afe-126">Showing multiple lines requires multiple labels.</span></span>
  
<span data-ttu-id="e2afe-127">Невозможно использовать метку для редактирования только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e2afe-127">It is not possible to use a label as a read-only edit control.</span></span> <span data-ttu-id="e2afe-128">Разница заключается в том, что управление редактированием можно выбрать и скопировать, а метка — нет.</span><span class="sxs-lookup"><span data-stu-id="e2afe-128">The difference is that an edit control can be selected and copied whereas a label cannot.</span></span> 
  
<span data-ttu-id="e2afe-129">Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="e2afe-129">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="e2afe-130">Сведения о реализации таблицы отображения см. в таблице [Implementing a Display Table.](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="e2afe-130">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e2afe-131">См. также</span><span class="sxs-lookup"><span data-stu-id="e2afe-131">See also</span></span>



[<span data-ttu-id="e2afe-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="e2afe-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="e2afe-133">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="e2afe-133">MAPI Structures</span></span>](mapi-structures.md)

