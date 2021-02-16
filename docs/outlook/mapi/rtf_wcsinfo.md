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
ms.openlocfilehash: 6bec29aa0e88e0224f9cd6049553f2df6379e23d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430534"
---
# <a name="rtf_wcsinfo"></a><span data-ttu-id="bc36b-103">RTF_WCSINFO</span><span class="sxs-lookup"><span data-stu-id="bc36b-103">RTF_WCSINFO</span></span>

  
  
<span data-ttu-id="bc36b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc36b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc36b-105">Эта структура позволяет указать сведения для расшифрования текста сообщения в сжатом формате RTF и при желании вернуть поток текста в основном формате.</span><span class="sxs-lookup"><span data-stu-id="bc36b-105">This structure enables you to specify information to decompress the body of a message in compressed Rich Text Format (RTF) and, optionally, return the body stream in its native format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="bc36b-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="bc36b-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a><span data-ttu-id="bc36b-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="bc36b-107">Members</span></span>

 <span data-ttu-id="bc36b-108">_size_</span><span class="sxs-lookup"><span data-stu-id="bc36b-108">_size_</span></span>
  
> <span data-ttu-id="bc36b-109">Размер структуры **RTF_WCSINFO** в количестве вбайтах.</span><span class="sxs-lookup"><span data-stu-id="bc36b-109">The size of the **RTF_WCSINFO** structure in number of bytes.</span></span> 
    
 <span data-ttu-id="bc36b-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bc36b-110">_ulFlags_</span></span>
  
> <span data-ttu-id="bc36b-111">Это битоваяmas флагов параметра для функции [WrapCompressedRTFStreamEx.](wrapcompressedrtfstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="bc36b-111">This is the bitmask of option flags for the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="bc36b-112">Поддерживаемые флажки вариантов:</span><span class="sxs-lookup"><span data-stu-id="bc36b-112">The supported option flags are:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="bc36b-113">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="bc36b-113">MAPI_MODIFY</span></span>  <br/> |<span data-ttu-id="bc36b-114">Это указывает, собирается ли клиент написать возвращаемого интерфейса потока с оболочкой.</span><span class="sxs-lookup"><span data-stu-id="bc36b-114">This indicates whether the client intends to write the wrapped stream interface that is returned.</span></span>  <br/> |
|<span data-ttu-id="bc36b-115">STORE_UNCOMPRESSED_RTF</span><span class="sxs-lookup"><span data-stu-id="bc36b-115">STORE_UNCOMPRESSED_RTF</span></span>  <br/> |<span data-ttu-id="bc36b-116">Это указывает, должен ли расшифрованный RTF быть записан в поток, на который указывает указатель _lpCompressedRTFStream_ функции [WrapCompressedRTFStreamEx.](wrapcompressedrtfstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="bc36b-116">This indicates whether the decompressed RTF is supposed to be written to the stream that is pointed to by the  _lpCompressedRTFStream_ pointer of the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span>  <br/> |
|<span data-ttu-id="bc36b-117">MAPI_NATIVE_BODY</span><span class="sxs-lookup"><span data-stu-id="bc36b-117">MAPI_NATIVE_BODY</span></span>  <br/> |<span data-ttu-id="bc36b-118">Это указывает, преобразуется ли также раскомпрессовавный поток в свой теле, прежде чем возвращать поток.</span><span class="sxs-lookup"><span data-stu-id="bc36b-118">This indicates whether the decompressed stream is also converted to the native body before returning the stream.</span></span> <span data-ttu-id="bc36b-119">Этот флаг нельзя объединить  с MAPI_MODIFY флагом.</span><span class="sxs-lookup"><span data-stu-id="bc36b-119">This flag cannot be combined with the **MAPI_MODIFY** flag.</span></span>  <br/> |
   
 <span data-ttu-id="bc36b-120">_ulInCodePage_</span><span class="sxs-lookup"><span data-stu-id="bc36b-120">_ulInCodePage_</span></span>
  
> <span data-ttu-id="bc36b-121">Это значение страницы кода сообщения.</span><span class="sxs-lookup"><span data-stu-id="bc36b-121">This is the code page value of the message.</span></span> <span data-ttu-id="bc36b-122">Как правило, это значение получается из канонического свойства [PidTagInternetCodepage](pidtaginternetcodepage-canonical-property.md) сообщения.</span><span class="sxs-lookup"><span data-stu-id="bc36b-122">Typically, this value is obtained from the [PidTagInternetCodepage Canonical Property](pidtaginternetcodepage-canonical-property.md) on the message.</span></span> <span data-ttu-id="bc36b-123">Это значение используется, только если **флаг MAPI_NATIVE_BODY** передается в _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="bc36b-123">This value is only used when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_.</span></span> <span data-ttu-id="bc36b-124">В противном случае это значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="bc36b-124">Otherwise, this value is ignored.</span></span>
    
 <span data-ttu-id="bc36b-125">_ulOutCodePage_</span><span class="sxs-lookup"><span data-stu-id="bc36b-125">_ulOutCodePage_</span></span>
  
> <span data-ttu-id="bc36b-126">Это значение кодовой страницы возвращаемого расшифрованного потока, который вы хотите получить.</span><span class="sxs-lookup"><span data-stu-id="bc36b-126">This is the code page value of the returned decompressed stream that you want.</span></span> <span data-ttu-id="bc36b-127">Если задано ненулевой значение, функция [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) преобразует поток в указанную кодовую страницу.</span><span class="sxs-lookup"><span data-stu-id="bc36b-127">If this is set to a non-zero value, the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function converts the stream to the specified code page.</span></span> <span data-ttu-id="bc36b-128">Если установлено нулевое значение, MAPI решает, какую кодовую страницу использовать.</span><span class="sxs-lookup"><span data-stu-id="bc36b-128">If this is set to a zero value, MAPI decides which code page to use.</span></span> <span data-ttu-id="bc36b-129">Это значение используется, только если флаг **MAPI_NATIVE_BODY** передается в  _ulFlags,_ а формат тела не является форматом RTF.</span><span class="sxs-lookup"><span data-stu-id="bc36b-129">This value is used only when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_, and the body format is not RTF.</span></span> <span data-ttu-id="bc36b-130">В противном случае это значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="bc36b-130">Otherwise, this value is ignored.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc36b-131">См. также</span><span class="sxs-lookup"><span data-stu-id="bc36b-131">See also</span></span>



[<span data-ttu-id="bc36b-132">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="bc36b-132">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

