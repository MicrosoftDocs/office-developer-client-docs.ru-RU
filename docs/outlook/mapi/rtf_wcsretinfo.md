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
# <a name="rtf_wcsretinfo"></a><span data-ttu-id="22d70-103">RTF_WCSRETINFO</span><span class="sxs-lookup"><span data-stu-id="22d70-103">RTF_WCSRETINFO</span></span>

<span data-ttu-id="22d70-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22d70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22d70-105">Эта структура предоставляет сведения о потоке в собственном формате, возвращенном из распаковки текста сообщения, инкапсулированного в формате RTF.</span><span class="sxs-lookup"><span data-stu-id="22d70-105">This structure provides information about a stream in native format returned from decompressing the body of a message that is encapsulated in compressed Rich Text Format (RTF).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="22d70-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="22d70-106">Quick info</span></span>

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a><span data-ttu-id="22d70-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="22d70-107">Members</span></span>

<span data-ttu-id="22d70-108">_size_</span><span class="sxs-lookup"><span data-stu-id="22d70-108">_size_</span></span>
  
> <span data-ttu-id="22d70-109">Размер структуры **RTF_WCSRETINFO** в байтах.</span><span class="sxs-lookup"><span data-stu-id="22d70-109">The size of the **RTF_WCSRETINFO** structure in number of bytes.</span></span> 
    
<span data-ttu-id="22d70-110">_улстреамфлагс_</span><span class="sxs-lookup"><span data-stu-id="22d70-110">_ulStreamFlags_</span></span>
  
> <span data-ttu-id="22d70-111">Это значение указывает формат основного текста.</span><span class="sxs-lookup"><span data-stu-id="22d70-111">This is a value that indicates the format of the native body.</span></span> <span data-ttu-id="22d70-112">Это значение является допустимым только в том случае, если флаг **MAPI_NATIVE_BODY** передается в параметре _ulFlags_ структуры [RTF_WCSINFO](rtf_wcsinfo.md) , которая передается функции [врапкомпресседртфстреамекс](wrapcompressedrtfstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="22d70-112">This value is only valid if the **MAPI_NATIVE_BODY** flag is passed in the  _ulFlags_ parameter of the [RTF_WCSINFO](rtf_wcsinfo.md) structure that is passed to the [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) function.</span></span> <span data-ttu-id="22d70-113">Это может быть одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="22d70-113">This can be one of the following values:</span></span> 
    
|||
|:-----|:-----|
|<span data-ttu-id="22d70-114">MAPI_NATIVE_BODY_TYPE_RTF</span><span class="sxs-lookup"><span data-stu-id="22d70-114">MAPI_NATIVE_BODY_TYPE_RTF</span></span>  <br/> |<span data-ttu-id="22d70-115">Это значение используется только в том случае, если _ulFlags_ включает флаг **MAPI_NATIVE_BODY** , а текст имеет формат RTF.</span><span class="sxs-lookup"><span data-stu-id="22d70-115">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is RTF.</span></span>  <br/> |
|<span data-ttu-id="22d70-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span><span class="sxs-lookup"><span data-stu-id="22d70-116">MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT</span></span>  <br/> |<span data-ttu-id="22d70-117">Это значение используется только в том случае, если _ulFlags_ включает флаг **MAPI_NATIVE_BODY** , а текст имеет обычный текстовый формат.</span><span class="sxs-lookup"><span data-stu-id="22d70-117">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is plain text format.</span></span>  <br/> |
|<span data-ttu-id="22d70-118">MAPI_NATIVE_BODY_TYPE_HTML</span><span class="sxs-lookup"><span data-stu-id="22d70-118">MAPI_NATIVE_BODY_TYPE_HTML</span></span>  <br/> |<span data-ttu-id="22d70-119">Это значение используется только в том случае, если _ulFlags_ включает флаг **MAPI_NATIVE_BODY** , а текст имеет формат HTML.</span><span class="sxs-lookup"><span data-stu-id="22d70-119">This value is only used if  _ulFlags_ includes the **MAPI_NATIVE_BODY** flag, and the body is Hypertext Markup Language (HTML) format.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="22d70-120">См. также</span><span class="sxs-lookup"><span data-stu-id="22d70-120">See also</span></span>

- [<span data-ttu-id="22d70-121">WrapCompressedRTFStreamEx</span><span class="sxs-lookup"><span data-stu-id="22d70-121">WrapCompressedRTFStreamEx</span></span>](wrapcompressedrtfstreamex.md)

