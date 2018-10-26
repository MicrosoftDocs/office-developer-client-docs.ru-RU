---
title: FreeProws
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeProws
api_type:
- HeaderDef
ms.assetid: 0f8f9fc4-4940-4c0a-92cc-2a6409b9a13f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0686cee9bf6fa47332f75f99e1d2a2d35cb7e7fb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578026"
---
# <a name="freeprows"></a><span data-ttu-id="23902-103">FreeProws</span><span class="sxs-lookup"><span data-stu-id="23902-103">FreeProws</span></span>

  
  
<span data-ttu-id="23902-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23902-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23902-105">Удаляет структуру [SRowSet](srowset.md) и освобождает связанные памяти, включая объем памяти, выделенный для всех элементов массивов и структур.</span><span class="sxs-lookup"><span data-stu-id="23902-105">Destroys an [SRowSet](srowset.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23902-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="23902-106">Header file:</span></span>  <br/> |<span data-ttu-id="23902-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="23902-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="23902-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="23902-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="23902-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="23902-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="23902-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="23902-110">Called by:</span></span>  <br/> |<span data-ttu-id="23902-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="23902-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a><span data-ttu-id="23902-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="23902-112">Parameters</span></span>

 <span data-ttu-id="23902-113">_prows_</span><span class="sxs-lookup"><span data-stu-id="23902-113">_prows_</span></span>
  
> <span data-ttu-id="23902-114">[in] Указатель на структуру **SRowSet** удалена.</span><span class="sxs-lookup"><span data-stu-id="23902-114">[in] Pointer to the **SRowSet** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="23902-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="23902-115">Return value</span></span>

<span data-ttu-id="23902-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="23902-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="23902-117">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="23902-117">Notes to callers</span></span>

<span data-ttu-id="23902-118">Как часть его реализация **FreeProws**MAPI вызывает функцию [MAPIFreeBuffer](mapifreebuffer.md) для освобождения каждой записи в структуре **SRowSet** перед очисткой полной структурой.</span><span class="sxs-lookup"><span data-stu-id="23902-118">As part of its implementation of **FreeProws**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **SRowSet** structure before freeing the complete structure.</span></span> <span data-ttu-id="23902-119">Таким образом все записи следует правила распределения для структуры [SRowSet](srowset.md) , с помощью отдельного вызова [MAPIAllocateBuffer](mapiallocatebuffer.md) для каждого элемента массива и структуры.</span><span class="sxs-lookup"><span data-stu-id="23902-119">Therefore all such entries must have followed the allocation rules for the [SRowSet](srowset.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="23902-120">Дополнительные сведения о выделении памяти для структуры **ADRLIST** и **SRowSet** можно [Памяти ADRLIST и SRowSet структур](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="23902-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="23902-121">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="23902-121">MFCMAPI reference</span></span>

<span data-ttu-id="23902-122">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="23902-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="23902-123">**Файл**</span><span class="sxs-lookup"><span data-stu-id="23902-123">**File**</span></span>|<span data-ttu-id="23902-124">**Функция**</span><span class="sxs-lookup"><span data-stu-id="23902-124">**Function**</span></span>|<span data-ttu-id="23902-125">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="23902-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="23902-126">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="23902-126">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="23902-127">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="23902-127">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="23902-128">Mfcmapi (en) использует метод **FreeProws** , чтобы освободить место на структуру SRowSet, содержащую строки в таблице, обрабатываемых.</span><span class="sxs-lookup"><span data-stu-id="23902-128">MFCMAPI uses the **FreeProws** method to free an SRowSet structure containing rows of the table being processed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="23902-129">См. также</span><span class="sxs-lookup"><span data-stu-id="23902-129">See also</span></span>



[<span data-ttu-id="23902-130">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="23902-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

