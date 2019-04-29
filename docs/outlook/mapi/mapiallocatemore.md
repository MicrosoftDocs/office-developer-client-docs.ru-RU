---
title: MAPIAllocateMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateMore
api_type:
- HeaderDef
ms.assetid: 3e48f76a-bc97-4cbc-9082-c07dd674b73e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 01980b2da735838eeffa9afa5a0d139b69e76d0c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435392"
---
# <a name="mapiallocatemore"></a><span data-ttu-id="8d96f-103">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="8d96f-103">MAPIAllocateMore</span></span>

  
  
<span data-ttu-id="8d96f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d96f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d96f-105">Выделяет буфер памяти, связанный с другим буфером, выделенным ранее с помощью функции [мапиаллокатебуффер](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="8d96f-105">Allocates a memory buffer that is linked to another buffer previously allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8d96f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8d96f-106">Header file:</span></span>  <br/> |<span data-ttu-id="8d96f-107">Мапикс. h</span><span class="sxs-lookup"><span data-stu-id="8d96f-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="8d96f-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="8d96f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8d96f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8d96f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8d96f-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="8d96f-110">Called by:</span></span>  <br/> |<span data-ttu-id="8d96f-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="8d96f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="8d96f-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d96f-112">Parameters</span></span>

 <span data-ttu-id="8d96f-113">_Кбсизе_</span><span class="sxs-lookup"><span data-stu-id="8d96f-113">_cbSize_</span></span>
  
> <span data-ttu-id="8d96f-114">возврата Размер нового выделяемого буфера (в байтах).</span><span class="sxs-lookup"><span data-stu-id="8d96f-114">[in] Size, in bytes, of the new buffer to be allocated.</span></span> 
    
 <span data-ttu-id="8d96f-115">_Лпобжект_</span><span class="sxs-lookup"><span data-stu-id="8d96f-115">_lpObject_</span></span>
  
> <span data-ttu-id="8d96f-116">возврата Указатель на существующий буфер MAPI, выделенный с помощью **мапиаллокатебуффер**.</span><span class="sxs-lookup"><span data-stu-id="8d96f-116">[in] Pointer to an existing MAPI buffer allocated using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="8d96f-117">_Лппбуффер_</span><span class="sxs-lookup"><span data-stu-id="8d96f-117">_lppBuffer_</span></span>
  
> <span data-ttu-id="8d96f-118">вышли Указатель на возвращаемый, вновь выделенный буфер.</span><span class="sxs-lookup"><span data-stu-id="8d96f-118">[out] Pointer to the returned, newly allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8d96f-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d96f-119">Return value</span></span>

<span data-ttu-id="8d96f-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d96f-120">S_OK</span></span> 
  
> <span data-ttu-id="8d96f-121">Вызов выполнен успешно и возвращен указатель на запрошенный объем памяти.</span><span class="sxs-lookup"><span data-stu-id="8d96f-121">The call succeeded and has returned a pointer to the requested memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8d96f-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="8d96f-122">Remarks</span></span>

<span data-ttu-id="8d96f-123">Во время обработки вызовов **мапиаллокатеморе** вызывающая реализация получает блок памяти из операционной системы.</span><span class="sxs-lookup"><span data-stu-id="8d96f-123">During **MAPIAllocateMore** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="8d96f-124">Буфер памяти выделяется на байтовый адрес с четным номером.</span><span class="sxs-lookup"><span data-stu-id="8d96f-124">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="8d96f-125">На платформах, где доступ к долговременному целому числу эффективнее, операционная система выделяет буфер на адресе, размер которого в байтах равен четырем.</span><span class="sxs-lookup"><span data-stu-id="8d96f-125">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="8d96f-126">Единственный способ освободить буфер, выделенный с помощью **мапиаллокатеморе** , — передать указатель буфера, указанный в параметре _лпобжект_ , в функцию [мапифрибуффер](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="8d96f-126">The only way to release a buffer allocated with **MAPIAllocateMore** is to pass the buffer pointer specified in the  _lpObject_ parameter to the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="8d96f-127">Связь между буферами памяти, выделенными с помощью [мапиаллокатебуффер](mapiallocatebuffer.md) и **Мапиаллокатеморе** , позволяет **мапифрибуффер** освобождать оба буфера с помощью одного вызова.</span><span class="sxs-lookup"><span data-stu-id="8d96f-127">The link between the memory buffers allocated with [MAPIAllocateBuffer](mapiallocatebuffer.md) and **MAPIAllocateMore** enables **MAPIFreeBuffer** to release both buffers with a single call.</span></span> 
  

