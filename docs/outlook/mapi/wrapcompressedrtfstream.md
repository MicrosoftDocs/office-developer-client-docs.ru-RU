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
# <a name="wrapcompressedrtfstream"></a><span data-ttu-id="9548b-103">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="9548b-103">WrapCompressedRTFStream</span></span>

  
  
<span data-ttu-id="9548b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9548b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9548b-105">Создает текстовый поток в формате несжатого текста RTF из сжатого формата, используемого в свойстве **пр_ртф_компрессед** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="9548b-105">Creates a text stream in uncompressed Rich Text Format (RTF) from the compressed format used in the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9548b-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9548b-106">Header file:</span></span>  <br/> |<span data-ttu-id="9548b-107">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="9548b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9548b-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="9548b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9548b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9548b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9548b-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="9548b-110">Called by:</span></span>  <br/> |<span data-ttu-id="9548b-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="9548b-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a><span data-ttu-id="9548b-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="9548b-112">Parameters</span></span>

 <span data-ttu-id="9548b-113">_Лпкомпресседртфстреам_</span><span class="sxs-lookup"><span data-stu-id="9548b-113">_lpCompressedRTFStream_</span></span>
  
> <span data-ttu-id="9548b-114">возврата Указатель на поток, Открытый в свойстве ПР_РТФ_КОМПРЕССЕД сообщения.</span><span class="sxs-lookup"><span data-stu-id="9548b-114">[in] Pointer to a stream opened on the PR_RTF_COMPRESSED property of a message.</span></span> 
    
 <span data-ttu-id="9548b-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9548b-115">_ulFlags_</span></span>
  
> <span data-ttu-id="9548b-116">возврата Битовая маска флагов Option для функции.</span><span class="sxs-lookup"><span data-stu-id="9548b-116">[in] Bitmask of option flags for the function.</span></span> <span data-ttu-id="9548b-117">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="9548b-117">The following flags can be set:</span></span>
    
<span data-ttu-id="9548b-118">МАПИ_МОДИФИ</span><span class="sxs-lookup"><span data-stu-id="9548b-118">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="9548b-119">Будет ли клиент намеревается считывать или записывать возвращаемый интерфейс упакованных потоков.</span><span class="sxs-lookup"><span data-stu-id="9548b-119">Whether the client intends to read or write the wrapped stream interface that is returned.</span></span> 
    
<span data-ttu-id="9548b-120">СТОРЕ_УНКОМПРЕССЕД_РТФ</span><span class="sxs-lookup"><span data-stu-id="9548b-120">STORE_UNCOMPRESSED_RTF</span></span> 
  
> <span data-ttu-id="9548b-121">Несжатый формат RTF должен быть записан в поток, на который указывает _лпкомпресседртфстреам_</span><span class="sxs-lookup"><span data-stu-id="9548b-121">Uncompressed RTF should be written to the stream pointed to by  _lpCompressedRTFStream_</span></span>
    
 <span data-ttu-id="9548b-122">_Лпункомпресседртфстреам_</span><span class="sxs-lookup"><span data-stu-id="9548b-122">_lpUncompressedRTFStream_</span></span>
  
> <span data-ttu-id="9548b-123">вышли Указатель на расположение, в котором **врапкомпресседртфстреам** возвращает поток для несжатого RTF.</span><span class="sxs-lookup"><span data-stu-id="9548b-123">[out] Pointer to the location where **WrapCompressedRTFStream** returns a stream for the uncompressed RTF.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9548b-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9548b-124">Return value</span></span>

<span data-ttu-id="9548b-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="9548b-125">S_OK</span></span> 
  
> <span data-ttu-id="9548b-126">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="9548b-126">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9548b-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="9548b-127">Remarks</span></span>

<span data-ttu-id="9548b-128">Если в параметре _ulFlags_ передается флаг мапи_модифи, параметр _лпкомпресседртфстреам_ должен быть уже открыт для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="9548b-128">If the MAPI_MODIFY flag is passed in the  _ulFlags_ parameter, the  _lpCompressedRTFStream_ parameter must already be open for reading and writing.</span></span> <span data-ttu-id="9548b-129">Новый, несжатый текст в формате RTF должен быть записан в интерфейс потока, возвращенный в _лпункомпресседртфстреам_.</span><span class="sxs-lookup"><span data-stu-id="9548b-129">New, uncompressed RTF text should be written into the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="9548b-130">Так как невозможно добавить существующий поток, необходимо записать весь текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="9548b-130">Because it is not possible to append the existing stream, the entire message text must be written.</span></span> 
  
<span data-ttu-id="9548b-131">Если в параметре _ulFlags_ передается нулевое значение, то _лпкомпресседртфстреам_ может быть открыт только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9548b-131">If zero is passed in the  _ulFlags_ parameter, then  _lpCompressedRTFStream_ may be opened read-only.</span></span> <span data-ttu-id="9548b-132">Только весь текст сообщения можно прочитать из интерфейса потока, возвращаемого в _лпункомпресседртфстреам_.</span><span class="sxs-lookup"><span data-stu-id="9548b-132">Only the entire message text can be read out of the stream interface returned in  _lpUncompressedRTFStream_.</span></span> <span data-ttu-id="9548b-133">Невозможно выполнить поиск, начав середину потока.</span><span class="sxs-lookup"><span data-stu-id="9548b-133">It is not possible to search starting the middle of the stream.</span></span> 
  
 <span data-ttu-id="9548b-134">В **врапкомпресседртфстреам** предполагается, что указатель сжатого потока установлен на начало потока.</span><span class="sxs-lookup"><span data-stu-id="9548b-134">**WrapCompressedRTFStream** assumes that the compressed stream's pointer is set to the beginning of the stream.</span></span> <span data-ttu-id="9548b-135">Некоторые методы OLE **IStream** не поддерживаются возвращенным несжатым потоком.</span><span class="sxs-lookup"><span data-stu-id="9548b-135">Certain OLE **IStream** methods are not supported by the returned uncompressed stream.</span></span> <span data-ttu-id="9548b-136">Сюда входят **: IStream:: Clone**, **IStream:: локкрегион**, **IStream:: revert**, **IStream:: Seek**, **IStream:: SetSize**, **IStream:: stat**и **IStream:: унлоккрегион**.</span><span class="sxs-lookup"><span data-stu-id="9548b-136">These include **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat**, and **IStream::UnlockRegion**.</span></span> <span data-ttu-id="9548b-137">Для копирования во весь поток необходим цикл чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="9548b-137">In order to copy to the entire stream, a read/write loop is needed.</span></span> 
  
<span data-ttu-id="9548b-138">Так как клиент записывает новый формат RTF в несжатом формате, он должен использовать **врапкомпресседртфстреам**вместо прямого записи в потоке.</span><span class="sxs-lookup"><span data-stu-id="9548b-138">Because the client writes new RTF in uncompressed format, it should use **WrapCompressedRTFStream**, instead of directly writing to the stream.</span></span> <span data-ttu-id="9548b-139">Клиенты, поддерживающие RTF, должны выполнить поиск флага СТОРЕ_УНКОМПРЕССЕД_РТФ в свойстве **пр_сторе_суппорт_маск** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) и передать его в **врапкомпрессед ртфстреам** , если он задан.</span><span class="sxs-lookup"><span data-stu-id="9548b-139">RTF-aware clients should search for the STORE_UNCOMPRESSED_RTF flag in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property and pass it to **WrapCompressed RTFStream** if it is set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9548b-140">См. также</span><span class="sxs-lookup"><span data-stu-id="9548b-140">See also</span></span>



[<span data-ttu-id="9548b-141">RTFSync</span><span class="sxs-lookup"><span data-stu-id="9548b-141">RTFSync</span></span>](rtfsync.md)

