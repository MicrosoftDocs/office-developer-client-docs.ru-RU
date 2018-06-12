---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 3a38a4604230c0aa3f5b0d104ae3b838f544b31d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812165"
---
# <a name="rtfwcsretinfo"></a><span data-ttu-id="1dc12-103">RTF_WCSRETINFO</span><span class="sxs-lookup"><span data-stu-id="1dc12-103">RTF_WCSRETINFO</span></span>

<span data-ttu-id="1dc12-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1dc12-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1dc12-105">Эта структура предоставляет сведения о потоке в собственном формате, возвращенные распаковки к тексту сообщения, инкапсулированную в сжатом форматированный текст (RTF).</span><span class="sxs-lookup"><span data-stu-id="1dc12-105">This structure provides information about a stream in native format returned from decompressing the body of a message that is encapsulated in compressed Rich Text Format (RTF).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1dc12-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="1dc12-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a><span data-ttu-id="1dc12-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="1dc12-107">Members</span></span>

<span data-ttu-id="1dc12-108">_size_</span><span class="sxs-lookup"><span data-stu-id="1dc12-108">_size_</span></span>
  
> <span data-ttu-id="1dc12-109">Размер структуры **RTF_WCSRETINFO** в байтах.</span><span class="sxs-lookup"><span data-stu-id="1dc12-109">The size of the **RTF_WCSRETINFO** structure in number of bytes.</span></span> 
    
<span data-ttu-id="1dc12-110">_ulStreamFlags_</span><span class="sxs-lookup"><span data-stu-id="1dc12-110">_ulStreamFlags_</span></span>
  
> <span data-ttu-id="1dc12-111">Это значение, указывающее формат собственного текста.</span><span class="sxs-lookup"><span data-stu-id="1dc12-111">This is a value that indicates the format of the native body.</span></span> <span data-ttu-id="1dc12-112">Это значение допустимо только в том случае, если флаг **MAPI_NATIVE_BODY** передается в параметре _ulFlags_ структуры [RTF_WCSINFO](rtf_wcsinfo.md) , которое передается в функцию [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="1dc12-112">This value is only valid if the **MAPI_NATIVE_BODY** flag is passed in the  _ulFlags_ parameter of the [RTF_WCSINFO](rtf_wcsinfo.md) structure that is passed to the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="1dc12-113">Это может быть одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="1dc12-113">This can be one of the following values:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="1dc12-114">MAPI_NATIVE_BODY_TYPE_RTF</span><span class="sxs-lookup"><span data-stu-id="1dc12-114">MAPI_NATIVE_BODY_TYPE_RTF</span></span>  <br/> |<span data-ttu-id="1dc12-115">Это значение используется только в том случае, если _ulFlags_ включает флаг **MAPI_NATIVE_BODY** , и текст RTF.</span><span class="sxs-lookup"><span data-stu-id="1dc12-115">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is RTF.</span></span>  <br/> |
|<span data-ttu-id="1dc12-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span><span class="sxs-lookup"><span data-stu-id="1dc12-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span></span>  <br/> |<span data-ttu-id="1dc12-117">Это значение используется только в том случае, если _ulFlags_ включает флаг **MAPI_NATIVE_BODY** , а текста имеет формат обычного текста.</span><span class="sxs-lookup"><span data-stu-id="1dc12-117">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is plain text format.</span></span>  <br/> |
|<span data-ttu-id="1dc12-118">MAPI_NATIVE_BODY_TYPE_HTML</span><span class="sxs-lookup"><span data-stu-id="1dc12-118">MAPI_NATIVE_BODY_TYPE_HTML</span></span>  <br/> |<span data-ttu-id="1dc12-119">Это значение используется только в том случае, если _ulFlags_ включает флаг **MAPI_NATIVE_BODY** , и текст формате (Hypertext Markup Language).</span><span class="sxs-lookup"><span data-stu-id="1dc12-119">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is Hypertext Markup Language (HTML) format.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1dc12-120">См. также</span><span class="sxs-lookup"><span data-stu-id="1dc12-120">See also</span></span>

- [<span data-ttu-id="1dc12-121">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="1dc12-121">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

