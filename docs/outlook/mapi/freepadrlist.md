---
title: FreePadrlist
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FreePadrlist
api_type:
- COM
ms.assetid: ca8fbac6-b6f1-46ab-90a1-fc16f0d5824c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 39a184f00ccf54d4fa4477bbdf3086f3e44bddb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576549"
---
# <a name="freepadrlist"></a><span data-ttu-id="a45ab-103">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="a45ab-103">FreePadrlist</span></span>

  
  
<span data-ttu-id="a45ab-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a45ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a45ab-105">Удаляет структуру [ADRLIST](adrlist.md) и освобождает связанные памяти, включая объем памяти, выделенный для всех элементов массивов и структур.</span><span class="sxs-lookup"><span data-stu-id="a45ab-105">Destroys an [ADRLIST](adrlist.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a45ab-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a45ab-106">Header file:</span></span>  <br/> |<span data-ttu-id="a45ab-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a45ab-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a45ab-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="a45ab-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a45ab-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a45ab-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a45ab-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="a45ab-110">Called by:</span></span>  <br/> |<span data-ttu-id="a45ab-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="a45ab-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a><span data-ttu-id="a45ab-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a45ab-112">Parameters</span></span>

 <span data-ttu-id="a45ab-113">_padrlist_</span><span class="sxs-lookup"><span data-stu-id="a45ab-113">_padrlist_</span></span>
  
> <span data-ttu-id="a45ab-114">[in] Указатель на структуру **ADRLIST** удалена.</span><span class="sxs-lookup"><span data-stu-id="a45ab-114">[in] Pointer to the **ADRLIST** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a45ab-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a45ab-115">Return value</span></span>

<span data-ttu-id="a45ab-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="a45ab-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="a45ab-117">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="a45ab-117">Notes to callers</span></span>

<span data-ttu-id="a45ab-118">Как часть его реализация **FreePadrlist**MAPI вызывает функцию [MAPIFreeBuffer](mapifreebuffer.md) для освобождения каждой записи в структуре **ADRLIST** перед очисткой полной структурой.</span><span class="sxs-lookup"><span data-stu-id="a45ab-118">As part of its implementation of **FreePadrlist**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **ADRLIST** structure before freeing the complete structure.</span></span> <span data-ttu-id="a45ab-119">Таким образом все записи следует правила распределения для структуры [ADRLIST](adrlist.md) , с помощью отдельного вызова [MAPIAllocateBuffer](mapiallocatebuffer.md) для каждого элемента массива и структуры.</span><span class="sxs-lookup"><span data-stu-id="a45ab-119">Therefore all such entries must have followed the allocation rules for the [ADRLIST](adrlist.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="a45ab-120">Дополнительные сведения о выделении памяти для структуры **ADRLIST** и **SRowSet** можно [Памяти ADRLIST и SRowSet структур](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="a45ab-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a45ab-121">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a45ab-121">MFCMAPI reference</span></span>

<span data-ttu-id="a45ab-122">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a45ab-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a45ab-123">**Файл**</span><span class="sxs-lookup"><span data-stu-id="a45ab-123">**File**</span></span>|<span data-ttu-id="a45ab-124">**Функция**</span><span class="sxs-lookup"><span data-stu-id="a45ab-124">**Function**</span></span>|<span data-ttu-id="a45ab-125">**�����������**</span><span class="sxs-lookup"><span data-stu-id="a45ab-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a45ab-126">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="a45ab-126">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="a45ab-127">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="a45ab-127">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="a45ab-128">Mfcmapi (en) использует метод **FreePadrlist** , чтобы освободить место на структуру ADRLIST, построенный для добавления указывает адрес к сообщению.</span><span class="sxs-lookup"><span data-stu-id="a45ab-128">MFCMAPI uses the **FreePadrlist** method to free an ADRLIST structure that was built to add a one-off address to a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a45ab-129">См. также</span><span class="sxs-lookup"><span data-stu-id="a45ab-129">See also</span></span>



[<span data-ttu-id="a45ab-130">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="a45ab-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

