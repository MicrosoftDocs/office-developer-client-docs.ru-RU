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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328016"
---
# <a name="freeprows"></a><span data-ttu-id="c9b8c-103">FreeProws</span><span class="sxs-lookup"><span data-stu-id="c9b8c-103">FreeProws</span></span>

  
  
<span data-ttu-id="c9b8c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9b8c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9b8c-105">Уничтожает структуру [SRowSet](srowset.md) и освобождает связанную память, в том числе память, выделенную для всех массивов и структур элементов.</span><span class="sxs-lookup"><span data-stu-id="c9b8c-105">Destroys an [SRowSet](srowset.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9b8c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c9b8c-106">Header file:</span></span>  <br/> |<span data-ttu-id="c9b8c-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="c9b8c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c9b8c-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="c9b8c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c9b8c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c9b8c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c9b8c-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="c9b8c-110">Called by:</span></span>  <br/> |<span data-ttu-id="c9b8c-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="c9b8c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a><span data-ttu-id="c9b8c-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9b8c-112">Parameters</span></span>

 <span data-ttu-id="c9b8c-113">_провс_</span><span class="sxs-lookup"><span data-stu-id="c9b8c-113">_prows_</span></span>
  
> <span data-ttu-id="c9b8c-114">возврата Указатель на структуру **SRowSet** , которую необходимо уничтожить.</span><span class="sxs-lookup"><span data-stu-id="c9b8c-114">[in] Pointer to the **SRowSet** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c9b8c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9b8c-115">Return value</span></span>

<span data-ttu-id="c9b8c-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="c9b8c-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="c9b8c-117">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c9b8c-117">Notes to callers</span></span>

<span data-ttu-id="c9b8c-118">В рамках реализации **фрипровс**MAPI вызывает функцию [мапифрибуффер](mapifreebuffer.md) , чтобы освободить каждую запись в структуре **SRowSet** , прежде чем освобождать всю структуру.</span><span class="sxs-lookup"><span data-stu-id="c9b8c-118">As part of its implementation of **FreeProws**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **SRowSet** structure before freeing the complete structure.</span></span> <span data-ttu-id="c9b8c-119">Таким образом, все такие записи должны следовать правилам распределения для структуры [SRowSet](srowset.md) , используя отдельный вызов [мапиаллокатебуффер](mapiallocatebuffer.md) для каждого массива и структуры элементов.</span><span class="sxs-lookup"><span data-stu-id="c9b8c-119">Therefore all such entries must have followed the allocation rules for the [SRowSet](srowset.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="c9b8c-120">Дополнительные сведения о выделении памяти для структур **ADRLIST** и **SRowSet** можно найти в статье [Управление памятью для структур ADRLIST и SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="c9b8c-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c9b8c-121">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c9b8c-121">MFCMAPI reference</span></span>

<span data-ttu-id="c9b8c-122">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="c9b8c-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c9b8c-123">**Файл**</span><span class="sxs-lookup"><span data-stu-id="c9b8c-123">**File**</span></span>|<span data-ttu-id="c9b8c-124">**Функция**</span><span class="sxs-lookup"><span data-stu-id="c9b8c-124">**Function**</span></span>|<span data-ttu-id="c9b8c-125">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="c9b8c-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c9b8c-126">Контентстаблелистктрл. cpp</span><span class="sxs-lookup"><span data-stu-id="c9b8c-126">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="c9b8c-127">Двсреадфунклоадтабле</span><span class="sxs-lookup"><span data-stu-id="c9b8c-127">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="c9b8c-128">MFCMAPI использует метод **фрипровс** для освобождения структуры SRowSet, содержащей строки обрабатываемой таблицы.</span><span class="sxs-lookup"><span data-stu-id="c9b8c-128">MFCMAPI uses the **FreeProws** method to free an SRowSet structure containing rows of the table being processed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c9b8c-129">См. также</span><span class="sxs-lookup"><span data-stu-id="c9b8c-129">See also</span></span>



[<span data-ttu-id="c9b8c-130">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="c9b8c-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

