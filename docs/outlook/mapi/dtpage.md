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
ms.openlocfilehash: 769ae984e4b6e8610ca7909ea2ac714d9d04d698
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589674"
---
# <a name="dtpage"></a><span data-ttu-id="324bc-103">DTPAGE</span><span class="sxs-lookup"><span data-stu-id="324bc-103">DTPAGE</span></span>

  
  
<span data-ttu-id="324bc-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="324bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="324bc-105">Описание диалогового окна, построенного из отображения таблицы с помощью функции [BuildDisplayTable](builddisplaytable.md) .</span><span class="sxs-lookup"><span data-stu-id="324bc-105">Describes the dialog box that is built from a display table by the [BuildDisplayTable](builddisplaytable.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="324bc-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="324bc-106">Header file:</span></span>  <br/> |<span data-ttu-id="324bc-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="324bc-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="324bc-108">Members</span><span class="sxs-lookup"><span data-stu-id="324bc-108">Members</span></span>

 <span data-ttu-id="324bc-109">**cctl**</span><span class="sxs-lookup"><span data-stu-id="324bc-109">**cctl**</span></span>
  
> <span data-ttu-id="324bc-110">Количество элементов управления, на который указывает член **lpctl** .</span><span class="sxs-lookup"><span data-stu-id="324bc-110">Count of controls pointed to by the **lpctl** member.</span></span> 
    
 <span data-ttu-id="324bc-111">**lpszResourceName**</span><span class="sxs-lookup"><span data-stu-id="324bc-111">**lpszResourceName**</span></span>
  
> <span data-ttu-id="324bc-112">Указатель на имя или целое число идентификатор ресурс диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="324bc-112">Pointer to the name or integer identifier for the dialog box resource.</span></span> 
    
 <span data-ttu-id="324bc-113">**lpszComponent**</span><span class="sxs-lookup"><span data-stu-id="324bc-113">**lpszComponent**</span></span>
  
> <span data-ttu-id="324bc-114">Указатель на строку, которая отображается в разделе **[Help File Mappings]** в MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="324bc-114">Pointer to the string that appears in the **[Help File Mappings]** section in MAPISVC.INF.</span></span> <span data-ttu-id="324bc-115">Поскольку **lpszComponent** объединение с элементом **ulItemID** , только один из этих элементов содержит допустимых данных.</span><span class="sxs-lookup"><span data-stu-id="324bc-115">Because **lpszComponent** is in a union with the **ulItemID** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="324bc-116">**ulItemID**</span><span class="sxs-lookup"><span data-stu-id="324bc-116">**ulItemID**</span></span>
  
> <span data-ttu-id="324bc-117">Целочисленный идентификатор ресурса со значением меньше или равно 65535, из которой могут читать имя файла справки.</span><span class="sxs-lookup"><span data-stu-id="324bc-117">Integer resource identifier with a value less than or equal to 65535 from which the Help file name can be read.</span></span> <span data-ttu-id="324bc-118">Поскольку **ulItemID** объединение с элементом **lpszComponent** , только один из этих элементов содержит допустимых данных.</span><span class="sxs-lookup"><span data-stu-id="324bc-118">Because **ulItemID** is in a union with the **lpszComponent** member, only one of these members has valid data.</span></span> 
    
 <span data-ttu-id="324bc-119">**lpctl**</span><span class="sxs-lookup"><span data-stu-id="324bc-119">**lpctl**</span></span>
  
> <span data-ttu-id="324bc-120">Указатель на массив структур [DTCTL](dtctl.md) , по одному для каждого элемента управления на странице.</span><span class="sxs-lookup"><span data-stu-id="324bc-120">Pointer to an array of [DTCTL](dtctl.md) structures, one for each control on the page.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="324bc-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="324bc-121">Remarks</span></span>

<span data-ttu-id="324bc-122">Чтобы определить файл справки для вкладки, установите член **lpszComponent** жестко строку или член **ulItemID** для целочисленный идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="324bc-122">To identify the Help file for the tabbed page, set either the **lpszComponent** member to a hard-coded string or the **ulItemID** member to an integer resource identifier.</span></span> 
  
<span data-ttu-id="324bc-123">Каждая запись в разделе **[Help File Mappings]** в файл Mapisvc.inf. INF состоит из строки компонента, не более 30 знаков, в левой части и путь к файлу справки в правом.</span><span class="sxs-lookup"><span data-stu-id="324bc-123">Each entry in the **[Help File Mappings]** section in MAPISVC.INF consists of a component string, no longer than 30 characters, on the left side and a Help file path on the right.</span></span> <span data-ttu-id="324bc-124">**UlItemID** и **lpszResourceName** находятся в параметре _hInstance_ **BuildDisplayTable**.</span><span class="sxs-lookup"><span data-stu-id="324bc-124">Both **ulItemID** and **lpszResourceName** are found in the  _hInstance_ parameter of **BuildDisplayTable**.</span></span> <span data-ttu-id="324bc-125">Для получения дополнительных сведений см [файл Mapisvc.inf. Раздел [сопоставлению файлов справки] INF](mapisvc-inf-help-file-mappings-section.md).</span><span class="sxs-lookup"><span data-stu-id="324bc-125">For more information, see [MAPISVC.INF [Help File Mappings] Section](mapisvc-inf-help-file-mappings-section.md).</span></span>
  
<span data-ttu-id="324bc-126">Несмотря на то, что **BuildDisplayTable** использует эту структуру для построения в таблице отображения из элемента управления ресурсами, структура **DTPAGE** никогда не отображается в самой таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="324bc-126">Although **BuildDisplayTable** uses this structure to build the display table from control resources, the **DTPAGE** structure never appears in the display table itself.</span></span> 
  
<span data-ttu-id="324bc-127">Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="324bc-127">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="324bc-128">Сведения о том, как реализовать отображения таблицу [Таблица отображения](display-table-implementation.md)см.</span><span class="sxs-lookup"><span data-stu-id="324bc-128">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="324bc-129">См. также</span><span class="sxs-lookup"><span data-stu-id="324bc-129">See also</span></span>



[<span data-ttu-id="324bc-130">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="324bc-130">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="324bc-131">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="324bc-131">DTBLPAGE</span></span>](dtblpage.md)
  
[<span data-ttu-id="324bc-132">DTCTL</span><span class="sxs-lookup"><span data-stu-id="324bc-132">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="324bc-133">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="324bc-133">MAPI Structures</span></span>](mapi-structures.md)

