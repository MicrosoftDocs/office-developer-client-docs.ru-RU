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
ms.openlocfilehash: 710e0e2fc334194e33c6d8ba1296e4c7b1938bc0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439802"
---
# <a name="wrapcompressedrtfstream"></a><span data-ttu-id="3f611-103">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="3f611-103">WrapCompressedRTFStream</span></span>

  
  
<span data-ttu-id="3f611-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f611-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f611-105">Создает текстовый поток в несжатом формате RTF из сжатого формата, используемого в свойстве **PR_RTF_COMPRESSED** [(PidTagRtfCompressed).](pidtagrtfcompressed-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="3f611-105">Creates a text stream in uncompressed Rich Text Format (RTF) from the compressed format used in the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3f611-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3f611-106">Header file:</span></span>  <br/> |<span data-ttu-id="3f611-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3f611-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3f611-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="3f611-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3f611-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3f611-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3f611-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="3f611-110">Called by:</span></span>  <br/> |<span data-ttu-id="3f611-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="3f611-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a><span data-ttu-id="3f611-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f611-112">Parameters</span></span>

 <span data-ttu-id="3f611-113">_lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="3f611-113">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="3f611-114">[in] Указатель на поток, открытый PR_RTF_COMPRESSED свойства сообщения.</span><span class="sxs-lookup"><span data-stu-id="3f611-114">[in] Pointer to a stream opened on the PR_RTF_COMPRESSED property of a message.</span></span> 
    
 <span data-ttu-id="3f611-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3f611-115">_ulFlags_</span></span>
  
> <span data-ttu-id="3f611-116">[in] Битоваяmas флажков параметра для функции.</span><span class="sxs-lookup"><span data-stu-id="3f611-116">[in] Bitmask of option flags for the function.</span></span> <span data-ttu-id="3f611-117">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="3f611-117">The following flags can be set:</span></span>
    
<span data-ttu-id="3f611-118">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="3f611-118">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="3f611-119">Будет ли клиент читать или записывать возвращаемого интерфейса потока с оболочкой.</span><span class="sxs-lookup"><span data-stu-id="3f611-119">Whether the client intends to read or write the wrapped stream interface that is returned.</span></span> 
    
<span data-ttu-id="3f611-120">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="3f611-120">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="3f611-121">Несмеченный RTF должен быть записан в поток, на который указывает  _lpCompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="3f611-121">Uncompressed RTF should be written to the stream pointed to by  _lpCompressedRTFStream_</span></span>
    
 <span data-ttu-id="3f611-122">_lpUncompressedRTFStream_</span><span class="sxs-lookup"><span data-stu-id="3f611-122">_lpUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="3f611-123">[out] Указатель на расположение, где **WrapCompressedRTFStream** возвращает поток для несхваченного RTF.</span><span class="sxs-lookup"><span data-stu-id="3f611-123">[out] Pointer to the location where **WrapCompressedRTFStream** returns a stream for the uncompressed RTF.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3f611-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f611-124">Return value</span></span>

<span data-ttu-id="3f611-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="3f611-125">S_OK</span></span> 
  
> <span data-ttu-id="3f611-126">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="3f611-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3f611-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="3f611-127">Remarks</span></span>

<span data-ttu-id="3f611-128">Если флаг MAPI_MODIFY передается в  _параметре ulFlags,_ параметр  _lpCompressedRTFStream_ должен быть уже открыт для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="3f611-128">If the MAPI_MODIFY flag is passed in the  _ulFlags_ parameter, the  _lpCompressedRTFStream_ parameter must already be open for reading and writing.</span></span> <span data-ttu-id="3f611-129">Новый несмеченный текст RTF должен быть записан в интерфейс потока, возвращенный _в lpUncompressedRTFStream._</span><span class="sxs-lookup"><span data-stu-id="3f611-129">New, uncompressed RTF text should be written into the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="3f611-130">Так как невозможно примедить существующий поток, необходимо написать весь текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="3f611-130">Because it is not possible to append the existing stream, the entire message text must be written.</span></span> 
  
<span data-ttu-id="3f611-131">Если в параметре  _ulFlags_ передается ноль,  _то lpCompressedRTFStream_ может быть открыт только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3f611-131">If zero is passed in the  _ulFlags_ parameter, then  _lpCompressedRTFStream_ may be opened read-only.</span></span> <span data-ttu-id="3f611-132">Из интерфейса потока, возвращаемого  _в lpUncompressedRTFStream,_ можно прочитать только весь текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="3f611-132">Only the entire message text can be read out of the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="3f611-133">Поиск в середине потока невозможен.</span><span class="sxs-lookup"><span data-stu-id="3f611-133">It is not possible to search starting the middle of the stream.</span></span> 
  
 <span data-ttu-id="3f611-134">**WrapCompressedRTFStream** предполагает, что указатель сжатого потока установлен в начале потока.</span><span class="sxs-lookup"><span data-stu-id="3f611-134">**WrapCompressedRTFStream** assumes that the compressed stream's pointer is set to the beginning of the stream.</span></span> <span data-ttu-id="3f611-135">Некоторые методы OLE **IStream** не поддерживаются возвращенным несмеченным потоком.</span><span class="sxs-lookup"><span data-stu-id="3f611-135">Certain OLE **IStream** methods are not supported by the returned uncompressed stream.</span></span> <span data-ttu-id="3f611-136">К ним относятся **IStream::Clone,** **IStream::LockRegion,** **IStream::Revert,** **IStream::Seek,** **IStream::SetSize,** **IStream::Stat** и **IStream::UnlockRegion.**</span><span class="sxs-lookup"><span data-stu-id="3f611-136">These include **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat**, and **IStream::UnlockRegion**.</span></span> <span data-ttu-id="3f611-137">Для копирования во весь поток необходим цикл чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="3f611-137">In order to copy to the entire stream, a read/write loop is needed.</span></span> 
  
<span data-ttu-id="3f611-138">Так как клиент записывает новый RTF в несмеченном формате, он должен использовать **WrapCompressedRTFStream** вместо прямой записи в поток.</span><span class="sxs-lookup"><span data-stu-id="3f611-138">Because the client writes new RTF in uncompressed format, it should use **WrapCompressedRTFStream**, instead of directly writing to the stream.</span></span> <span data-ttu-id="3f611-139">Клиенты с RTF должны искать флаг STORE_UNCOMPRESSED_RTF в свойстве **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)и передавать его в **wrapCompressed RTFStream,** если он установлен.</span><span class="sxs-lookup"><span data-stu-id="3f611-139">RTF-aware clients should search for the STORE_UNCOMPRESSED_RTF flag in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property and pass it to **WrapCompressed RTFStream** if it is set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3f611-140">См. также</span><span class="sxs-lookup"><span data-stu-id="3f611-140">See also</span></span>



[<span data-ttu-id="3f611-141">RTFSync</span><span class="sxs-lookup"><span data-stu-id="3f611-141">RTFSync</span></span>](rtfsync.md)

