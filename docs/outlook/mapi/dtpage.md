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
# <a name="dtpage"></a><span data-ttu-id="1215d-103">DTPAGE</span><span class="sxs-lookup"><span data-stu-id="1215d-103">DTPAGE</span></span>

  
  
<span data-ttu-id="1215d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1215d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1215d-105">Описывает диалоговое окно, созданное из таблицы отображения с помощью функции [буилддисплайтабле](builddisplaytable.md) .</span><span class="sxs-lookup"><span data-stu-id="1215d-105">Describes the dialog box that is built from a display table by the [BuildDisplayTable](builddisplaytable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1215d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1215d-106">Header file:</span></span>  <br/> |<span data-ttu-id="1215d-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="1215d-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="1215d-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="1215d-108">Members</span></span>

 <span data-ttu-id="1215d-109">**кктл**</span><span class="sxs-lookup"><span data-stu-id="1215d-109">**cctl**</span></span>
  
> <span data-ttu-id="1215d-110">Количество элементов управления, на которые указывает элемент **лпктл** .</span><span class="sxs-lookup"><span data-stu-id="1215d-110">Count of controls pointed to by the **lpctl** member.</span></span> 
    
 <span data-ttu-id="1215d-111">**лпсзресаурценаме**</span><span class="sxs-lookup"><span data-stu-id="1215d-111">**lpszResourceName**</span></span>
  
> <span data-ttu-id="1215d-112">Указатель на имя или целочисленный идентификатор ресурса диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="1215d-112">Pointer to the name or integer identifier for the dialog box resource.</span></span> 
    
 <span data-ttu-id="1215d-113">**лпсзкомпонент**</span><span class="sxs-lookup"><span data-stu-id="1215d-113">**lpszComponent**</span></span>
  
> <span data-ttu-id="1215d-114">Указатель на строку, которая отображается в разделе **[Help File Mappings]** файла Mapisvc. INF.</span><span class="sxs-lookup"><span data-stu-id="1215d-114">Pointer to the string that appears in the **[Help File Mappings]** section in MAPISVC.INF.</span></span> <span data-ttu-id="1215d-115">Так как **лпсзкомпонент** находится в объединении с членом **улитемид** , только один из этих элементов содержит допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="1215d-115">Because **lpszComponent** is in a union with the **ulItemID** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="1215d-116">**улитемид**</span><span class="sxs-lookup"><span data-stu-id="1215d-116">**ulItemID**</span></span>
  
> <span data-ttu-id="1215d-117">Целочисленный идентификатор ресурса со значением, меньшим или равным 65535, из которого можно прочитать имя файла справки.</span><span class="sxs-lookup"><span data-stu-id="1215d-117">Integer resource identifier with a value less than or equal to 65535 from which the Help file name can be read.</span></span> <span data-ttu-id="1215d-118">Так как **улитемид** находится в объединении с членом **лпсзкомпонент** , только один из этих элементов содержит допустимые данные.</span><span class="sxs-lookup"><span data-stu-id="1215d-118">Because **ulItemID** is in a union with the **lpszComponent** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="1215d-119">**лпктл**</span><span class="sxs-lookup"><span data-stu-id="1215d-119">**lpctl**</span></span>
  
> <span data-ttu-id="1215d-120">Указатель на массив структур [дтктл](dtctl.md) , по одному для каждого элемента управления на странице.</span><span class="sxs-lookup"><span data-stu-id="1215d-120">Pointer to an array of [DTCTL](dtctl.md) structures, one for each control on the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1215d-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="1215d-121">Remarks</span></span>

<span data-ttu-id="1215d-122">Чтобы определить файл справки для страницы с вкладками, установите для элемента **лпсзкомпонент** жестко заданную строку или элемент **улитемид** в целочисленный идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="1215d-122">To identify the Help file for the tabbed page, set either the **lpszComponent** member to a hard-coded string or the **ulItemID** member to an integer resource identifier.</span></span> 
  
<span data-ttu-id="1215d-123">Каждая запись в разделе **[Help File Mappings]** в Mapisvc. INF состоит из строки компонента, не превышающей 30 символов, в левой части и пути к файлу справки справа.</span><span class="sxs-lookup"><span data-stu-id="1215d-123">Each entry in the **[Help File Mappings]** section in MAPISVC.INF consists of a component string, no longer than 30 characters, on the left side and a Help file path on the right.</span></span> <span data-ttu-id="1215d-124">В параметре _HINSTANCE_ объекта **буилддисплайтабле**найдены **улитемид** и **лпсзресаурценаме** .</span><span class="sxs-lookup"><span data-stu-id="1215d-124">Both **ulItemID** and **lpszResourceName** are found in the  _hInstance_ parameter of **BuildDisplayTable**.</span></span> <span data-ttu-id="1215d-125">Дополнительные сведения см. в разделе [Mapisvc. INF-раздел [сопоставления файлов справки]](mapisvc-inf-help-file-mappings-section.md).</span><span class="sxs-lookup"><span data-stu-id="1215d-125">For more information, see [MAPISVC.INF [Help File Mappings] Section](mapisvc-inf-help-file-mappings-section.md).</span></span>
  
<span data-ttu-id="1215d-126">Несмотря на то, что **буилддисплайтабле** использует эту структуру для создания таблицы отображения из ресурсов управления, структура **дтпаже** никогда не отображается в самой таблице.</span><span class="sxs-lookup"><span data-stu-id="1215d-126">Although **BuildDisplayTable** uses this structure to build the display table from control resources, the **DTPAGE** structure never appears in the display table itself.</span></span> 
  
<span data-ttu-id="1215d-127">Общие сведения о отображаемых таблицах приведены в разделе [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="1215d-127">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="1215d-128">Сведения о том, как реализовать таблицу отображения, можно найти [в статье реализация таблицы отображения](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="1215d-128">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1215d-129">См. также</span><span class="sxs-lookup"><span data-stu-id="1215d-129">See also</span></span>



[<span data-ttu-id="1215d-130">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="1215d-130">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="1215d-131">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="1215d-131">DTBLPAGE</span></span>](dtblpage.md)
  
[<span data-ttu-id="1215d-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="1215d-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="1215d-133">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="1215d-133">MAPI Structures</span></span>](mapi-structures.md)

