---
title: WrapCompressedRTFStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WrapCompressedRTFStream
api_type:
- COM
ms.assetid: 0949e066-aa28-4ede-ac88-b2dccd5098e8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a7095907a1fb437e225922d0bef08b4ad79a4b6f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594595"
---
# <a name="wrapcompressedrtfstream"></a><span data-ttu-id="48249-103">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="48249-103">WrapCompressedRTFStream</span></span>

  
  
<span data-ttu-id="48249-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48249-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48249-105">Создает текстовый поток в несжатую форматированный текст (RTF) в сжатом формате, используемые в свойстве **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="48249-105">Creates a text stream in uncompressed Rich Text Format (RTF) from the compressed format used in the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="48249-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="48249-106">Header file:</span></span>  <br/> |<span data-ttu-id="48249-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="48249-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="48249-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="48249-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="48249-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="48249-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="48249-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="48249-110">Called by:</span></span>  <br/> |<span data-ttu-id="48249-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="48249-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a><span data-ttu-id="48249-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="48249-112">Parameters</span></span>

 <span data-ttu-id="48249-113">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="48249-113">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="48249-114">[in] Указатель на поток, открытый в свойстве PR_RTF_COMPRESSED сообщения.</span><span class="sxs-lookup"><span data-stu-id="48249-114">[in] Pointer to a stream opened on the PR_RTF_COMPRESSED property of a message.</span></span> 
    
 <span data-ttu-id="48249-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="48249-115">_ulFlags_</span></span>
  
> <span data-ttu-id="48249-116">[in] Битовая маска флаги функции.</span><span class="sxs-lookup"><span data-stu-id="48249-116">[in] Bitmask of option flags for the function.</span></span> <span data-ttu-id="48249-117">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="48249-117">The following flags can be set:</span></span>
    
<span data-ttu-id="48249-118">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="48249-118">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="48249-119">Является ли клиентом для чтения или записи интерфейс упакованный поток, который возвращается.</span><span class="sxs-lookup"><span data-stu-id="48249-119">Whether the client intends to read or write the wrapped stream interface that is returned.</span></span> 
    
<span data-ttu-id="48249-120">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="48249-120">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="48249-121">Поток, на который указывает _lpCompressedRTFStream_ должны быть написаны несжатый формат RTF</span><span class="sxs-lookup"><span data-stu-id="48249-121">Uncompressed RTF should be written to the stream pointed to by  _lpCompressedRTFStream_</span></span>
    
 <span data-ttu-id="48249-122">_lpUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="48249-122">_lpUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="48249-123">[out] Указатель на место, где **WrapCompressedRTFStream** возвращает поток для несжатый формат RTF.</span><span class="sxs-lookup"><span data-stu-id="48249-123">[out] Pointer to the location where **WrapCompressedRTFStream** returns a stream for the uncompressed RTF.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="48249-124">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="48249-124">Return value</span></span>

<span data-ttu-id="48249-125">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="48249-125">S_OK</span></span> 
  
> <span data-ttu-id="48249-126">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="48249-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="48249-127">���������</span><span class="sxs-lookup"><span data-stu-id="48249-127">Remarks</span></span>

<span data-ttu-id="48249-128">Если флаг MAPI_MODIFY передается в параметре _ulFlags_ , параметр _lpCompressedRTFStream_ уже должен быть открыт для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="48249-128">If the MAPI_MODIFY flag is passed in the  _ulFlags_ parameter, the  _lpCompressedRTFStream_ parameter must already be open for reading and writing.</span></span> <span data-ttu-id="48249-129">Новый, несжатую текст RTF должны быть написаны в интерфейс потока, возвращаемого в _lpUncompressedRTFStream_.</span><span class="sxs-lookup"><span data-stu-id="48249-129">New, uncompressed RTF text should be written into the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="48249-130">Так как не удается добавить существующего потока, должен быть написан всего текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="48249-130">Because it is not possible to append the existing stream, the entire message text must be written.</span></span> 
  
<span data-ttu-id="48249-131">Ноль передается в параметре _ulFlags_ , _lpCompressedRTFStream_ может открыть, только для чтения.</span><span class="sxs-lookup"><span data-stu-id="48249-131">If zero is passed in the  _ulFlags_ parameter, then  _lpCompressedRTFStream_ may be opened read-only.</span></span> <span data-ttu-id="48249-132">Поток интерфейса, возвращаемых в _lpUncompressedRTFStream_могут читать только всего текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="48249-132">Only the entire message text can be read out of the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="48249-133">Начало потока в центре поиска невозможна.</span><span class="sxs-lookup"><span data-stu-id="48249-133">It is not possible to search starting the middle of the stream.</span></span> 
  
 <span data-ttu-id="48249-134">**WrapCompressedRTFStream** предполагается, что указатель сжатый поток — это значение в начале потока.</span><span class="sxs-lookup"><span data-stu-id="48249-134">**WrapCompressedRTFStream** assumes that the compressed stream's pointer is set to the beginning of the stream.</span></span> <span data-ttu-id="48249-135">Некоторые методы OLE **IStream** , возвращенные несжатую потока не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="48249-135">Certain OLE **IStream** methods are not supported by the returned uncompressed stream.</span></span> <span data-ttu-id="48249-136">К ним относятся **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat**и **IStream::UnlockRegion**.</span><span class="sxs-lookup"><span data-stu-id="48249-136">These include **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat**, and **IStream::UnlockRegion**.</span></span> <span data-ttu-id="48249-137">Чтобы скопировать всю потока, необходим цикл чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="48249-137">In order to copy to the entire stream, a read/write loop is needed.</span></span> 
  
<span data-ttu-id="48249-138">Так как клиент записывает новый формат RTF в формат без сжатия, его следует использовать **WrapCompressedRTFStream**вместо непосредственно записи потока.</span><span class="sxs-lookup"><span data-stu-id="48249-138">Because the client writes new RTF in uncompressed format, it should use **WrapCompressedRTFStream**, instead of directly writing to the stream.</span></span> <span data-ttu-id="48249-139">Принять во внимание RTF клиентов следует искать флаг STORE_UNCOMPRESSED_RTF в свойстве **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) и передайте в него **WrapCompressed RTFStream** если оно установлено.</span><span class="sxs-lookup"><span data-stu-id="48249-139">RTF-aware clients should search for the STORE_UNCOMPRESSED_RTF flag in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property and pass it to **WrapCompressed RTFStream** if it is set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="48249-140">См. также</span><span class="sxs-lookup"><span data-stu-id="48249-140">See also</span></span>



[<span data-ttu-id="48249-141">RTFSync</span><span class="sxs-lookup"><span data-stu-id="48249-141">RTFSync</span></span>](rtfsync.md)

