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
# <a name="rtfwcsinfo"></a><span data-ttu-id="d7903-103">RTF_WCSINFO</span><span class="sxs-lookup"><span data-stu-id="d7903-103">RTF_WCSINFO</span></span>

  
  
<span data-ttu-id="d7903-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7903-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7903-105">Эта структура позволяет указать информацию для распаковки текста сообщения в формате RTF и (при необходимости) вернуть поток текста в исходном формате.</span><span class="sxs-lookup"><span data-stu-id="d7903-105">This structure enables you to specify information to decompress the body of a message in compressed Rich Text Format (RTF) and, optionally, return the body stream in its native format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d7903-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="d7903-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a><span data-ttu-id="d7903-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="d7903-107">Members</span></span>

 <span data-ttu-id="d7903-108">_размер_</span><span class="sxs-lookup"><span data-stu-id="d7903-108">_size_</span></span>
  
> <span data-ttu-id="d7903-109">Размер структуры **ртф_вксинфо** в байтах.</span><span class="sxs-lookup"><span data-stu-id="d7903-109">The size of the **RTF_WCSINFO** structure in number of bytes.</span></span> 
    
 <span data-ttu-id="d7903-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d7903-110">_ulFlags_</span></span>
  
> <span data-ttu-id="d7903-111">Это битовая маска флагов параметров для функции [врапкомпресседртфстреамекс](wrapcompressedrtfstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="d7903-111">This is the bitmask of option flags for the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="d7903-112">Флаги поддерживаемых параметров:</span><span class="sxs-lookup"><span data-stu-id="d7903-112">The supported option flags are:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="d7903-113">МАПИ_МОДИФИ</span><span class="sxs-lookup"><span data-stu-id="d7903-113">MAPI_MODIFY</span></span>  <br/> |<span data-ttu-id="d7903-114">Это указывает на то, что клиент намеревается записывать возвращаемый интерфейс упакованных потоков.</span><span class="sxs-lookup"><span data-stu-id="d7903-114">This indicates whether the client intends to write the wrapped stream interface that is returned.</span></span>  <br/> |
|<span data-ttu-id="d7903-115">СТОРЕ_УНКОМПРЕССЕД_РТФ</span><span class="sxs-lookup"><span data-stu-id="d7903-115">STORE_UNCOMPRESSED_RTF</span></span>  <br/> |<span data-ttu-id="d7903-116">Указывает, следует ли записывать Распакованный формат RTF в поток, на который указывает указатель _лпкомпресседртфстреам_ функции [врапкомпресседртфстреамекс](wrapcompressedrtfstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="d7903-116">This indicates whether the decompressed RTF is supposed to be written to the stream that is pointed to by the  _lpCompressedRTFStream_ pointer of the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span>  <br/> |
|<span data-ttu-id="d7903-117">МАПИ_НАТИВЕ_БОДИ</span><span class="sxs-lookup"><span data-stu-id="d7903-117">MAPI_NATIVE_BODY</span></span>  <br/> |<span data-ttu-id="d7903-118">Это указывает, будет ли Распакованный поток также преобразован в основной текст перед возвратом потока.</span><span class="sxs-lookup"><span data-stu-id="d7903-118">This indicates whether the decompressed stream is also converted to the native body before returning the stream.</span></span> <span data-ttu-id="d7903-119">Этот флаг не может использоваться вместе с флагом **мапи_модифи** .</span><span class="sxs-lookup"><span data-stu-id="d7903-119">This flag cannot be combined with the **MAPI_MODIFY** flag.</span></span>  <br/> |
   
 <span data-ttu-id="d7903-120">_Улинкодепаже_</span><span class="sxs-lookup"><span data-stu-id="d7903-120">_ulInCodePage_</span></span>
  
> <span data-ttu-id="d7903-121">Это значение кодовой страницы сообщения.</span><span class="sxs-lookup"><span data-stu-id="d7903-121">This is the code page value of the message.</span></span> <span data-ttu-id="d7903-122">Как правило, это значение получается из [канонИческое свойство PidTagInternetCodepage](pidtaginternetcodepage-canonical-property.md) сообщения.</span><span class="sxs-lookup"><span data-stu-id="d7903-122">Typically, this value is obtained from the [PidTagInternetCodepage Canonical Property](pidtaginternetcodepage-canonical-property.md) on the message.</span></span> <span data-ttu-id="d7903-123">Это значение используется только в том случае, если в _ulFlags_передается флаг **мапи_нативе_боди** .</span><span class="sxs-lookup"><span data-stu-id="d7903-123">This value is only used when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_.</span></span> <span data-ttu-id="d7903-124">В противном случае это значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="d7903-124">Otherwise, this value is ignored.</span></span>
    
 <span data-ttu-id="d7903-125">_Улауткодепаже_</span><span class="sxs-lookup"><span data-stu-id="d7903-125">_ulOutCodePage_</span></span>
  
> <span data-ttu-id="d7903-126">Это значение кодовой страницы возвращенного распакованного потока, который требуется выполнить.</span><span class="sxs-lookup"><span data-stu-id="d7903-126">This is the code page value of the returned decompressed stream that you want.</span></span> <span data-ttu-id="d7903-127">Если для этого свойства задано значение, отличное от нуля, функция [врапкомпресседртфстреамекс](wrapcompressedrtfstreamex.md) преобразует поток в указанную кодовую страницу.</span><span class="sxs-lookup"><span data-stu-id="d7903-127">If this is set to a non-zero value, the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function converts the stream to the specified code page.</span></span> <span data-ttu-id="d7903-128">Если для этого свойства задано нулевое значение, MAPI определяет, какую кодовую страницу использовать.</span><span class="sxs-lookup"><span data-stu-id="d7903-128">If this is set to a zero value, MAPI decides which code page to use.</span></span> <span data-ttu-id="d7903-129">Это значение используется только в том случае, если флаг **мапи_нативе_боди** передается в _ulFlags_, а формат основного текста не является RTF.</span><span class="sxs-lookup"><span data-stu-id="d7903-129">This value is used only when the **MAPI_NATIVE_BODY** flag is passed in  _ulFlags_, and the body format is not RTF.</span></span> <span data-ttu-id="d7903-130">В противном случае это значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="d7903-130">Otherwise, this value is ignored.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d7903-131">См. также</span><span class="sxs-lookup"><span data-stu-id="d7903-131">See also</span></span>



[<span data-ttu-id="d7903-132">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="d7903-132">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

