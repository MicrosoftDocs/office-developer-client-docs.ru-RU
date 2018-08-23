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
# <a name="freeprows"></a><span data-ttu-id="b88f2-103">FreeProws</span><span class="sxs-lookup"><span data-stu-id="b88f2-103">FreeProws</span></span>

  
  
<span data-ttu-id="b88f2-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b88f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b88f2-105">Удаляет структуру [SRowSet](srowset.md) и освобождает связанные памяти, включая объем памяти, выделенный для всех элементов массивов и структур.</span><span class="sxs-lookup"><span data-stu-id="b88f2-105">Destroys an [SRowSet](srowset.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b88f2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b88f2-106">Header file:</span></span>  <br/> |<span data-ttu-id="b88f2-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b88f2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b88f2-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="b88f2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b88f2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b88f2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b88f2-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="b88f2-110">Called by:</span></span>  <br/> |<span data-ttu-id="b88f2-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="b88f2-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a><span data-ttu-id="b88f2-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b88f2-112">Parameters</span></span>

 <span data-ttu-id="b88f2-113">_prows_</span><span class="sxs-lookup"><span data-stu-id="b88f2-113">_prows_</span></span>
  
> <span data-ttu-id="b88f2-114">[in] Указатель на структуру **SRowSet** удалена.</span><span class="sxs-lookup"><span data-stu-id="b88f2-114">[in] Pointer to the **SRowSet** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b88f2-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b88f2-115">Return value</span></span>

<span data-ttu-id="b88f2-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="b88f2-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="b88f2-117">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="b88f2-117">Notes to callers</span></span>

<span data-ttu-id="b88f2-118">Как часть его реализация **FreeProws**MAPI вызывает функцию [MAPIFreeBuffer](mapifreebuffer.md) для освобождения каждой записи в структуре **SRowSet** перед очисткой полной структурой.</span><span class="sxs-lookup"><span data-stu-id="b88f2-118">As part of its implementation of **FreeProws**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **SRowSet** structure before freeing the complete structure.</span></span> <span data-ttu-id="b88f2-119">Таким образом все записи следует правила распределения для структуры [SRowSet](srowset.md) , с помощью отдельного вызова [MAPIAllocateBuffer](mapiallocatebuffer.md) для каждого элемента массива и структуры.</span><span class="sxs-lookup"><span data-stu-id="b88f2-119">Therefore all such entries must have followed the allocation rules for the [SRowSet](srowset.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="b88f2-120">Дополнительные сведения о выделении памяти для структуры **ADRLIST** и **SRowSet** можно [Памяти ADRLIST и SRowSet структур](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="b88f2-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b88f2-121">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="b88f2-121">MFCMAPI reference</span></span>

<span data-ttu-id="b88f2-122">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="b88f2-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b88f2-123">**����**</span><span class="sxs-lookup"><span data-stu-id="b88f2-123">**File**</span></span>|<span data-ttu-id="b88f2-124">**�������**</span><span class="sxs-lookup"><span data-stu-id="b88f2-124">**Function**</span></span>|<span data-ttu-id="b88f2-125">**�����������**</span><span class="sxs-lookup"><span data-stu-id="b88f2-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b88f2-126">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="b88f2-126">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="b88f2-127">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="b88f2-127">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="b88f2-128">Mfcmapi (en) использует метод **FreeProws** , чтобы освободить место на структуру SRowSet, содержащую строки в таблице, обрабатываемых.</span><span class="sxs-lookup"><span data-stu-id="b88f2-128">MFCMAPI uses the **FreeProws** method to free an SRowSet structure containing rows of the table being processed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b88f2-129">См. также</span><span class="sxs-lookup"><span data-stu-id="b88f2-129">See also</span></span>



[<span data-ttu-id="b88f2-130">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="b88f2-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

