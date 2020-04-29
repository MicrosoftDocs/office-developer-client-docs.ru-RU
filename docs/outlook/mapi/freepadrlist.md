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
ms.openlocfilehash: 95c2e52760bd7d65351b4dd2091b68a43cd2f97c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408644"
---
# <a name="freepadrlist"></a><span data-ttu-id="09dca-103">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="09dca-103">FreePadrlist</span></span>

  
  
<span data-ttu-id="09dca-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09dca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09dca-105">Уничтожает структуру [ADRLIST](adrlist.md) и освобождает связанную память, в том числе память, выделенную для всех массивов и структур элементов.</span><span class="sxs-lookup"><span data-stu-id="09dca-105">Destroys an [ADRLIST](adrlist.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="09dca-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="09dca-106">Header file:</span></span>  <br/> |<span data-ttu-id="09dca-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="09dca-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="09dca-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="09dca-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="09dca-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="09dca-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="09dca-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="09dca-110">Called by:</span></span>  <br/> |<span data-ttu-id="09dca-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="09dca-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a><span data-ttu-id="09dca-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="09dca-112">Parameters</span></span>

 <span data-ttu-id="09dca-113">_падрлист_</span><span class="sxs-lookup"><span data-stu-id="09dca-113">_padrlist_</span></span>
  
> <span data-ttu-id="09dca-114">возврата Указатель на структуру **ADRLIST** , которую необходимо уничтожить.</span><span class="sxs-lookup"><span data-stu-id="09dca-114">[in] Pointer to the **ADRLIST** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="09dca-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="09dca-115">Return value</span></span>

<span data-ttu-id="09dca-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="09dca-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="09dca-117">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="09dca-117">Notes to callers</span></span>

<span data-ttu-id="09dca-118">В рамках реализации **фрипадрлист**MAPI вызывает функцию [мапифрибуффер](mapifreebuffer.md) , чтобы освободить каждую запись в структуре **ADRLIST** , прежде чем освобождать всю структуру.</span><span class="sxs-lookup"><span data-stu-id="09dca-118">As part of its implementation of **FreePadrlist**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **ADRLIST** structure before freeing the complete structure.</span></span> <span data-ttu-id="09dca-119">Таким образом, все такие записи должны следовать правилам распределения для структуры [ADRLIST](adrlist.md) , используя отдельный вызов [мапиаллокатебуффер](mapiallocatebuffer.md) для каждого массива и структуры элементов.</span><span class="sxs-lookup"><span data-stu-id="09dca-119">Therefore all such entries must have followed the allocation rules for the [ADRLIST](adrlist.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="09dca-120">Дополнительные сведения о выделении памяти для структур **ADRLIST** и **SRowSet** можно найти в статье [Управление памятью для структур ADRLIST и SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="09dca-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="09dca-121">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="09dca-121">MFCMAPI reference</span></span>

<span data-ttu-id="09dca-122">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="09dca-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="09dca-123">**Файл**</span><span class="sxs-lookup"><span data-stu-id="09dca-123">**File**</span></span>|<span data-ttu-id="09dca-124">**Функция**</span><span class="sxs-lookup"><span data-stu-id="09dca-124">**Function**</span></span>|<span data-ttu-id="09dca-125">**�����������**</span><span class="sxs-lookup"><span data-stu-id="09dca-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="09dca-126">Мапиабфунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="09dca-126">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="09dca-127">аддонеоффаддресс</span><span class="sxs-lookup"><span data-stu-id="09dca-127">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="09dca-128">MFCMAPI использует метод **фрипадрлист** для освобождения структуры ADRLIST, созданной для добавления к сообщению одного адреса.</span><span class="sxs-lookup"><span data-stu-id="09dca-128">MFCMAPI uses the **FreePadrlist** method to free an ADRLIST structure that was built to add a one-off address to a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="09dca-129">См. также</span><span class="sxs-lookup"><span data-stu-id="09dca-129">See also</span></span>



[<span data-ttu-id="09dca-130">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="09dca-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

