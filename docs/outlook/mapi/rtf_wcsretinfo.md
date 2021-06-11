---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cfa18c215fc98610b836db31e2a07581291910be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426172"
---
# <a name="rtf_wcsretinfo"></a><span data-ttu-id="f452a-103">RTF_WCSRETINFO</span><span class="sxs-lookup"><span data-stu-id="f452a-103">RTF_WCSRETINFO</span></span>

<span data-ttu-id="f452a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f452a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f452a-105">Эта структура предоставляет сведения о потоке в родном формате, возвращаемом из декомпрессии тела сообщения, инкапсулированного в сжатом формате богатого текста (RTF).</span><span class="sxs-lookup"><span data-stu-id="f452a-105">This structure provides information about a stream in native format returned from decompressing the body of a message that is encapsulated in compressed Rich Text Format (RTF).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f452a-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="f452a-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a><span data-ttu-id="f452a-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="f452a-107">Members</span></span>

<span data-ttu-id="f452a-108">_size_</span><span class="sxs-lookup"><span data-stu-id="f452a-108">_size_</span></span>
  
> <span data-ttu-id="f452a-109">Размер структуры **RTF_WCSRETINFO** в количестве bytes.</span><span class="sxs-lookup"><span data-stu-id="f452a-109">The size of the **RTF_WCSRETINFO** structure in number of bytes.</span></span> 
    
<span data-ttu-id="f452a-110">_ulStreamFlags_</span><span class="sxs-lookup"><span data-stu-id="f452a-110">_ulStreamFlags_</span></span>
  
> <span data-ttu-id="f452a-111">Это значение указывает формат родного тела.</span><span class="sxs-lookup"><span data-stu-id="f452a-111">This is a value that indicates the format of the native body.</span></span> <span data-ttu-id="f452a-112">Это значение допустимо, **MAPI_NATIVE_BODY** флаг передается в _параметре ulFlags_ структуры RTF_WCSINFO, которая передается функции [WrapCompressedRTFStreamEx.](wrapcompressedrtfstreamex.md) [](rtf_wcsinfo.md)</span><span class="sxs-lookup"><span data-stu-id="f452a-112">This value is only valid if the **MAPI_NATIVE_BODY** flag is passed in the  _ulFlags_ parameter of the [RTF_WCSINFO](rtf_wcsinfo.md) structure that is passed to the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="f452a-113">Это может быть одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="f452a-113">This can be one of the following values:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="f452a-114">MAPI_NATIVE_BODY_TYPE_RTF</span><span class="sxs-lookup"><span data-stu-id="f452a-114">MAPI_NATIVE_BODY_TYPE_RTF</span></span>  <br/> |<span data-ttu-id="f452a-115">Это значение используется только в том случае,  если _ulFlags_ включает флаг MAPI_NATIVE_BODY, а тело — RTF.</span><span class="sxs-lookup"><span data-stu-id="f452a-115">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is RTF.</span></span>  <br/> |
|<span data-ttu-id="f452a-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span><span class="sxs-lookup"><span data-stu-id="f452a-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span></span>  <br/> |<span data-ttu-id="f452a-117">Это значение используется только в том случае, если _ulFlags_ включает флаг MAPI_NATIVE_BODY, а тело — обычный текстовый формат. </span><span class="sxs-lookup"><span data-stu-id="f452a-117">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is plain text format.</span></span>  <br/> |
|<span data-ttu-id="f452a-118">MAPI_NATIVE_BODY_TYPE_HTML</span><span class="sxs-lookup"><span data-stu-id="f452a-118">MAPI_NATIVE_BODY_TYPE_HTML</span></span>  <br/> |<span data-ttu-id="f452a-119">Это значение используется только в том случае,  если _ulFlags_ включает флаг MAPI_NATIVE_BODY, а тело — формат Hypertext Markup Language (HTML).</span><span class="sxs-lookup"><span data-stu-id="f452a-119">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is Hypertext Markup Language (HTML) format.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f452a-120">См. также</span><span class="sxs-lookup"><span data-stu-id="f452a-120">See also</span></span>

- [<span data-ttu-id="f452a-121">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="f452a-121">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

