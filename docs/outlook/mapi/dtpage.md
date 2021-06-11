---
title: DTPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTPAGE
api_type:
- COM
ms.assetid: 500f60ed-fdec-4d70-8cf5-664c46643956
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ad8aec8d015849965bea6ac011c8a45e75c69ca1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408224"
---
# <a name="dtpage"></a><span data-ttu-id="65c0b-103">DTPAGE</span><span class="sxs-lookup"><span data-stu-id="65c0b-103">DTPAGE</span></span>

  
  
<span data-ttu-id="65c0b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="65c0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="65c0b-105">Описывает диалоговое окно, построенное из таблицы отображения [функцией BuildDisplayTable.](builddisplaytable.md)</span><span class="sxs-lookup"><span data-stu-id="65c0b-105">Describes the dialog box that is built from a display table by the [BuildDisplayTable](builddisplaytable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="65c0b-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="65c0b-106">Header file:</span></span>  <br/> |<span data-ttu-id="65c0b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="65c0b-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct DTPAGE
{
  ULONG cctl;
  LPSTR lpszResourceName;
  union
  {
    LPSTR lpszComponent;
    ULONG ulItemID;
  }
  LPDTCTL lpctl;
} DTPAGE, FAR *LPDTPAGE;

```

## <a name="members"></a><span data-ttu-id="65c0b-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="65c0b-108">Members</span></span>

 <span data-ttu-id="65c0b-109">**cctl**</span><span class="sxs-lookup"><span data-stu-id="65c0b-109">**cctl**</span></span>
  
> <span data-ttu-id="65c0b-110">Количество элементов управления, на которые указывает **элемент lpctl.**</span><span class="sxs-lookup"><span data-stu-id="65c0b-110">Count of controls pointed to by the **lpctl** member.</span></span> 
    
 <span data-ttu-id="65c0b-111">**lpszResourceName**</span><span class="sxs-lookup"><span data-stu-id="65c0b-111">**lpszResourceName**</span></span>
  
> <span data-ttu-id="65c0b-112">Указатель на имя или идентификатор integer для ресурса диалоговых полей.</span><span class="sxs-lookup"><span data-stu-id="65c0b-112">Pointer to the name or integer identifier for the dialog box resource.</span></span> 
    
 <span data-ttu-id="65c0b-113">**lpszComponent**</span><span class="sxs-lookup"><span data-stu-id="65c0b-113">**lpszComponent**</span></span>
  
> <span data-ttu-id="65c0b-114">Указатель на строку, которая отображается в **разделе [Сопоставления** файлов справки] в MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="65c0b-114">Pointer to the string that appears in the **[Help File Mappings]** section in MAPISVC.INF.</span></span> <span data-ttu-id="65c0b-115">Так **как lpszComponent** находится в союзе с **членом ulItemID,** только один из этих членов имеет допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="65c0b-115">Because **lpszComponent** is in a union with the **ulItemID** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="65c0b-116">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="65c0b-116">**ulItemID**</span></span>
  
> <span data-ttu-id="65c0b-117">Идентификатор ресурса integer со значением меньше или равно 65535, из которого можно прочитать имя файла Справки.</span><span class="sxs-lookup"><span data-stu-id="65c0b-117">Integer resource identifier with a value less than or equal to 65535 from which the Help file name can be read.</span></span> <span data-ttu-id="65c0b-118">Так как **ulItemID** находится в союзе с **членом lpszComponent,** только один из этих членов имеет допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="65c0b-118">Because **ulItemID** is in a union with the **lpszComponent** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="65c0b-119">**lpctl**</span><span class="sxs-lookup"><span data-stu-id="65c0b-119">**lpctl**</span></span>
  
> <span data-ttu-id="65c0b-120">Указатель на массив структур [DTCTL,](dtctl.md) по одному для каждого управления на странице.</span><span class="sxs-lookup"><span data-stu-id="65c0b-120">Pointer to an array of [DTCTL](dtctl.md) structures, one for each control on the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="65c0b-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="65c0b-121">Remarks</span></span>

<span data-ttu-id="65c0b-122">Чтобы определить файл справки для страницы вкладки, установите либо член **lpszComponent** в строку с жесткой кодом, либо **член ulItemID** к идентификатору ресурсов в составе.</span><span class="sxs-lookup"><span data-stu-id="65c0b-122">To identify the Help file for the tabbed page, set either the **lpszComponent** member to a hard-coded string or the **ulItemID** member to an integer resource identifier.</span></span> 
  
<span data-ttu-id="65c0b-123">Каждая запись в **разделе [Сопоставления файлов справки]** в MAPISVC. INF состоит из строки компонентов, не более 30 символов, с левой стороны и пути файла справки справа.</span><span class="sxs-lookup"><span data-stu-id="65c0b-123">Each entry in the **[Help File Mappings]** section in MAPISVC.INF consists of a component string, no longer than 30 characters, on the left side and a Help file path on the right.</span></span> <span data-ttu-id="65c0b-124">Оба **параметра ulItemID** и **lpszResourceName** находятся в  _параметре hInstance_ **BuildDisplayTable**.</span><span class="sxs-lookup"><span data-stu-id="65c0b-124">Both **ulItemID** and **lpszResourceName** are found in the  _hInstance_ parameter of **BuildDisplayTable**.</span></span> <span data-ttu-id="65c0b-125">Дополнительные сведения см. [в mapISVC. Раздел INF [Справка сопоставления файлов]](mapisvc-inf-help-file-mappings-section.md).</span><span class="sxs-lookup"><span data-stu-id="65c0b-125">For more information, see [MAPISVC.INF [Help File Mappings] Section](mapisvc-inf-help-file-mappings-section.md).</span></span>
  
<span data-ttu-id="65c0b-126">Хотя **BuildDisplayTable** использует эту структуру для построения таблицы отображения из ресурсов управления, структура **DTPAGE** никогда не отображается в самой таблице отображения.</span><span class="sxs-lookup"><span data-stu-id="65c0b-126">Although **BuildDisplayTable** uses this structure to build the display table from control resources, the **DTPAGE** structure never appears in the display table itself.</span></span> 
  
<span data-ttu-id="65c0b-127">Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="65c0b-127">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="65c0b-128">Сведения о реализации таблицы отображения см. в таблице [Implementing a Display Table.](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="65c0b-128">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="65c0b-129">См. также</span><span class="sxs-lookup"><span data-stu-id="65c0b-129">See also</span></span>



[<span data-ttu-id="65c0b-130">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="65c0b-130">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="65c0b-131">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="65c0b-131">DTBLPAGE</span></span>](dtblpage.md)
  
[<span data-ttu-id="65c0b-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="65c0b-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="65c0b-133">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="65c0b-133">MAPI Structures</span></span>](mapi-structures.md)

