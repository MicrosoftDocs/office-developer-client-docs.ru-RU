---
title: RTF_WCSINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c94501e-0ec7-e836-33a7-adcf5a61b375
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2dd9f002401f8de52a9ad187b7e5850d47caf8a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587385"
---
# <a name="rtfwcsinfo"></a><span data-ttu-id="fde28-103">RTF_WCSINFO</span><span class="sxs-lookup"><span data-stu-id="fde28-103">RTF_WCSINFO</span></span>

  
  
<span data-ttu-id="fde28-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fde28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fde28-105">Эта структура позволяет указать сведения, которые распаковка к тексту сообщения в сжатом форматированный текст (RTF) и при необходимости вернуться в потоке текста в его собственном формате.</span><span class="sxs-lookup"><span data-stu-id="fde28-105">This structure enables you to specify information to decompress the body of a message in compressed Rich Text Format (RTF) and, optionally, return the body stream in its native format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fde28-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="fde28-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a><span data-ttu-id="fde28-107">Members</span><span class="sxs-lookup"><span data-stu-id="fde28-107">Members</span></span>

 <span data-ttu-id="fde28-108">_size_.</span><span class="sxs-lookup"><span data-stu-id="fde28-108">_size_</span></span>
  
> <span data-ttu-id="fde28-109">Размер структуры **RTF_WCSINFO** в байтах.</span><span class="sxs-lookup"><span data-stu-id="fde28-109">The size of the **RTF_WCSINFO** structure in number of bytes.</span></span> 
    
 <span data-ttu-id="fde28-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fde28-110">_ulFlags_</span></span>
  
> <span data-ttu-id="fde28-111">Это битовая маска флаги функции [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="fde28-111">This is the bitmask of option flags for the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="fde28-112">Поддерживаемые варианты флаги являются:</span><span class="sxs-lookup"><span data-stu-id="fde28-112">The supported option flags are:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="fde28-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="fde28-113">MAPI_MODIFY</span></span>  <br/> |<span data-ttu-id="fde28-114">Указывает, планирует интерфейса упакованный поток, который возвращается клиенту.</span><span class="sxs-lookup"><span data-stu-id="fde28-114">This indicates whether the client intends to write the wrapped stream interface that is returned.</span></span>  <br/> |
|<span data-ttu-id="fde28-115">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="fde28-115">STORE_UNCOMPRESSED_RTF</span></span>  <br/> |<span data-ttu-id="fde28-116">Указывает, должен ли распакованных RTF для записи в поток, который указывает _lpCompressedRTFStream_ указатель функции [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="fde28-116">This indicates whether the decompressed RTF is supposed to be written to the stream that is pointed to by the  _lpCompressedRTFStream_ pointer of the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span>  <br/> |
|<span data-ttu-id="fde28-117">MAPI_NATIVE_BODY</span><span class="sxs-lookup"><span data-stu-id="fde28-117">MAPI_NATIVE_BODY</span></span>  <br/> |<span data-ttu-id="fde28-118">Это указывает, будет ли распакованных потока также преобразованы в собственный текст перед возвращением потока.</span><span class="sxs-lookup"><span data-stu-id="fde28-118">This indicates whether the decompressed stream is also converted to the native body before returning the stream.</span></span> <span data-ttu-id="fde28-119">Этот флаг нельзя использовать вместе с флагом **MAPI_MODIFY** .</span><span class="sxs-lookup"><span data-stu-id="fde28-119">This flag cannot be combined with the **MAPI_MODIFY** flag.</span></span>  <br/> |
   
 <span data-ttu-id="fde28-120">_ulInCodePage_</span><span class="sxs-lookup"><span data-stu-id="fde28-120">_ulInCodePage_</span></span>
  
> <span data-ttu-id="fde28-121">Это значение кодовой страницы сообщения.</span><span class="sxs-lookup"><span data-stu-id="fde28-121">This is the code page value of the message.</span></span> <span data-ttu-id="fde28-122">Как правило это значение будет получен из [Каноническое свойство PidTagInternetCodepage](pidtaginternetcodepage-canonical-property.md) в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="fde28-122">Typically, this value is obtained from the [PidTagInternetCodepage Canonical Property](pidtaginternetcodepage-canonical-property.md) on the message.</span></span> <span data-ttu-id="fde28-123">Это значение используется только в том случае, когда флаг **MAPI_NATIVE_BODY** передается в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="fde28-123">This value is only used when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_.</span></span> <span data-ttu-id="fde28-124">В противном случае это значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="fde28-124">Otherwise, this value is ignored.</span></span>
    
 <span data-ttu-id="fde28-125">_ulOutCodePage_</span><span class="sxs-lookup"><span data-stu-id="fde28-125">_ulOutCodePage_</span></span>
  
> <span data-ttu-id="fde28-126">Это значение кодовой страницы, возвращенные распакованных потока, который будет.</span><span class="sxs-lookup"><span data-stu-id="fde28-126">This is the code page value of the returned decompressed stream that you want.</span></span> <span data-ttu-id="fde28-127">Если это задано значение ненулевое значение, функция [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) преобразуется в потоке кодовой страницы.</span><span class="sxs-lookup"><span data-stu-id="fde28-127">If this is set to a non-zero value, the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function converts the stream to the specified code page.</span></span> <span data-ttu-id="fde28-128">Если это присвоено значение 0, MAPI решает использовать кодовую страницу.</span><span class="sxs-lookup"><span data-stu-id="fde28-128">If this is set to a zero value, MAPI decides which code page to use.</span></span> <span data-ttu-id="fde28-129">Это значение используется только в том случае, когда флаг **MAPI_NATIVE_BODY** передается в _ulFlags_и формат текста сообщения не является RTF.</span><span class="sxs-lookup"><span data-stu-id="fde28-129">This value is used only when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_, and the body format is not RTF.</span></span> <span data-ttu-id="fde28-130">В противном случае это значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="fde28-130">Otherwise, this value is ignored.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fde28-131">См. также</span><span class="sxs-lookup"><span data-stu-id="fde28-131">See also</span></span>



[<span data-ttu-id="fde28-132">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="fde28-132">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

