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
ms.openlocfilehash: b1109b3201e1b1e4a78c3a0fe0f2eb4d0cd43c05
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438822"
---
# <a name="freeprows"></a><span data-ttu-id="425ce-103">FreeProws</span><span class="sxs-lookup"><span data-stu-id="425ce-103">FreeProws</span></span>

  
  
<span data-ttu-id="425ce-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="425ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="425ce-105">Уничтожает [структуру SRowSet](srowset.md) и освободит связанную память, включая память, выделенную для всех массивов и структур членов.</span><span class="sxs-lookup"><span data-stu-id="425ce-105">Destroys an [SRowSet](srowset.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="425ce-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="425ce-106">Header file:</span></span>  <br/> |<span data-ttu-id="425ce-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="425ce-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="425ce-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="425ce-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="425ce-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="425ce-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="425ce-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="425ce-110">Called by:</span></span>  <br/> |<span data-ttu-id="425ce-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="425ce-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a><span data-ttu-id="425ce-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="425ce-112">Parameters</span></span>

 <span data-ttu-id="425ce-113">_prows_</span><span class="sxs-lookup"><span data-stu-id="425ce-113">_prows_</span></span>
  
> <span data-ttu-id="425ce-114">[in] Указатель на **структуру SRowSet,** которая будет уничтожена.</span><span class="sxs-lookup"><span data-stu-id="425ce-114">[in] Pointer to the **SRowSet** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="425ce-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="425ce-115">Return value</span></span>

<span data-ttu-id="425ce-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="425ce-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="425ce-117">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="425ce-117">Notes to callers</span></span>

<span data-ttu-id="425ce-118">В рамках своей реализации **FreeProws** MAPI вызывает функцию [MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить каждую запись в **структуре SRowSet,** прежде чем освободить полную структуру.</span><span class="sxs-lookup"><span data-stu-id="425ce-118">As part of its implementation of **FreeProws**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **SRowSet** structure before freeing the complete structure.</span></span> <span data-ttu-id="425ce-119">Поэтому все такие записи должны следовать правилам распределения для структуры [SRowSet,](srowset.md) используя отдельный вызов [MAPIAllocateBuffer](mapiallocatebuffer.md) для каждого массива и структуры участников.</span><span class="sxs-lookup"><span data-stu-id="425ce-119">Therefore all such entries must have followed the allocation rules for the [SRowSet](srowset.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="425ce-120">Дополнительные сведения о деление памяти для структур **ADRLIST** и **SRowSet** см. в рубрике Управление памятью для [структур ADRLIST и SRowSet.](managing-memory-for-adrlist-and-srowset-structures.md)</span><span class="sxs-lookup"><span data-stu-id="425ce-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="425ce-121">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="425ce-121">MFCMAPI reference</span></span>

<span data-ttu-id="425ce-122">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="425ce-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="425ce-123">**Файл**</span><span class="sxs-lookup"><span data-stu-id="425ce-123">**File**</span></span>|<span data-ttu-id="425ce-124">**Функция**</span><span class="sxs-lookup"><span data-stu-id="425ce-124">**Function**</span></span>|<span data-ttu-id="425ce-125">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="425ce-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="425ce-126">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="425ce-126">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="425ce-127">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="425ce-127">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="425ce-128">MFCMAPI использует **метод FreeProws,** чтобы освободить структуру SRowSet, содержащую строки обрабатываемой таблицы.</span><span class="sxs-lookup"><span data-stu-id="425ce-128">MFCMAPI uses the **FreeProws** method to free an SRowSet structure containing rows of the table being processed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="425ce-129">См. также</span><span class="sxs-lookup"><span data-stu-id="425ce-129">See also</span></span>



[<span data-ttu-id="425ce-130">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="425ce-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

