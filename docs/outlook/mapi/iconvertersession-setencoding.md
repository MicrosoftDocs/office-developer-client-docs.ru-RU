---
title: IConverterSessionSetEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetCharSet
api_type:
- COM
ms.assetid: a9624d3f-a636-0267-5cbd-de0db42f9c22
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5a81e04d112e0adf201dcacf03673daac77a04ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341302"
---
# <a name="iconvertersessionsetencoding"></a><span data-ttu-id="7ea2d-103">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="7ea2d-103">IConverterSession::SetEncoding</span></span>

<span data-ttu-id="7ea2d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ea2d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ea2d-105">Инициализирует кодику, используемую во время преобразования.</span><span class="sxs-lookup"><span data-stu-id="7ea2d-105">Initializes the encoding to be used during conversion.</span></span>
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a><span data-ttu-id="7ea2d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ea2d-106">Parameters</span></span>

<span data-ttu-id="7ea2d-107">_et_</span><span class="sxs-lookup"><span data-stu-id="7ea2d-107">_et_</span></span>
  
> <span data-ttu-id="7ea2d-108">Значение [ENCODINGTYPE.](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7ea2d-108">An [ENCODINGTYPE](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx) value.</span></span> <span data-ttu-id="7ea2d-109">Поддерживаются только следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7ea2d-109">Only the following values are supported:</span></span> 
    
   - <span data-ttu-id="7ea2d-110">IET_BASE64</span><span class="sxs-lookup"><span data-stu-id="7ea2d-110">IET_BASE64</span></span>
   - <span data-ttu-id="7ea2d-111">IET_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="7ea2d-111">IET_UUENCODE</span></span>
   - <span data-ttu-id="7ea2d-112">IET_QP</span><span class="sxs-lookup"><span data-stu-id="7ea2d-112">IET_QP</span></span>
   - <span data-ttu-id="7ea2d-113">IET_7BIT</span><span class="sxs-lookup"><span data-stu-id="7ea2d-113">IET_7BIT</span></span>
   - <span data-ttu-id="7ea2d-114">IET_8BIT</span><span class="sxs-lookup"><span data-stu-id="7ea2d-114">IET_8BIT</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7ea2d-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ea2d-115">Return value</span></span>

<span data-ttu-id="7ea2d-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="7ea2d-116">E_INVALIDARG</span></span>
  
> <span data-ttu-id="7ea2d-117">Переданный тип кодии недействителен.</span><span class="sxs-lookup"><span data-stu-id="7ea2d-117">The encoding type passed was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7ea2d-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="7ea2d-118">Remarks</span></span>

<span data-ttu-id="7ea2d-119">Вызовите **SetEncoding** перед использованием [IConverterSession::MAPIToMIMEStm для](iconvertersession-mapitomimestm.md) выполнения преобразования.</span><span class="sxs-lookup"><span data-stu-id="7ea2d-119">Call **SetEncoding** before using [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to perform conversion.</span></span> 
  
<span data-ttu-id="7ea2d-120">Используйте **SetEncoding,** чтобы настроить кодику только для внешнего тела сообщения почтового элемента.</span><span class="sxs-lookup"><span data-stu-id="7ea2d-120">Use **SetEncoding** to set the encoding for only the outermost message body of a mail item.</span></span> <span data-ttu-id="7ea2d-121">Microsoft Outlook 2010, русская версия и Microsoft Outlook 2013 выберите кодику для всех отдельных вложений.</span><span class="sxs-lookup"><span data-stu-id="7ea2d-121">Microsoft Outlook 2010 and Microsoft Outlook 2013 choose the encoding for any individual attachments.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7ea2d-122">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7ea2d-122">MFCMAPI reference</span></span>

<span data-ttu-id="7ea2d-123">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="7ea2d-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7ea2d-124">**Файл**</span><span class="sxs-lookup"><span data-stu-id="7ea2d-124">**File**</span></span>|<span data-ttu-id="7ea2d-125">**Функция**</span><span class="sxs-lookup"><span data-stu-id="7ea2d-125">**Function**</span></span>|<span data-ttu-id="7ea2d-126">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="7ea2d-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7ea2d-127">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="7ea2d-127">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="7ea2d-128">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="7ea2d-128">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="7ea2d-129">MFCMAPI использует MimeToMAPI для преобразования EML-файла в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="7ea2d-129">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="7ea2d-130">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="7ea2d-130">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="7ea2d-131">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="7ea2d-131">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="7ea2d-132">MFCMAPI использует MAPIToMIMEStm для преобразования сообщения MAPI в EML-файл.</span><span class="sxs-lookup"><span data-stu-id="7ea2d-132">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7ea2d-133">См. также</span><span class="sxs-lookup"><span data-stu-id="7ea2d-133">See also</span></span>

- [<span data-ttu-id="7ea2d-134">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7ea2d-134">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="7ea2d-135">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="7ea2d-135">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="7ea2d-136">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="7ea2d-136">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="7ea2d-137">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="7ea2d-137">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="7ea2d-138">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="7ea2d-138">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="7ea2d-139">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="7ea2d-139">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
- [<span data-ttu-id="7ea2d-140">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="7ea2d-140">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="7ea2d-141">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="7ea2d-141">MAPI Constants</span></span>](mapi-constants.md)

