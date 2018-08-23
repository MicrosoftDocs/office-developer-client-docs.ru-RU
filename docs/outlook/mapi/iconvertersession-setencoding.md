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
ms.openlocfilehash: 3edcb422eb0e3dd415d49c5e014c8b69095e7ec1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577207"
---
# <a name="iconvertersessionsetencoding"></a><span data-ttu-id="eee33-103">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="eee33-103">IConverterSession::SetEncoding</span></span>

<span data-ttu-id="eee33-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eee33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eee33-105">Инициализирует кодировку для использования при преобразовании.</span><span class="sxs-lookup"><span data-stu-id="eee33-105">Initializes the encoding to be used during conversion.</span></span>
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a><span data-ttu-id="eee33-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="eee33-106">Parameters</span></span>

<span data-ttu-id="eee33-107">_et_</span><span class="sxs-lookup"><span data-stu-id="eee33-107">_et_</span></span>
  
> <span data-ttu-id="eee33-108">Значение [ENCODINGTYPE](http://msdn.microsoft.com/en-us/library/aa374936%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="eee33-108">An [ENCODINGTYPE](http://msdn.microsoft.com/en-us/library/aa374936%28VS.85%29.aspx) value.</span></span> <span data-ttu-id="eee33-109">Поддерживаются только следующие значения:</span><span class="sxs-lookup"><span data-stu-id="eee33-109">Only the following values are supported:</span></span> 
    
   - <span data-ttu-id="eee33-110">IET_BASE64</span><span class="sxs-lookup"><span data-stu-id="eee33-110">IET_BASE64</span></span>
   - <span data-ttu-id="eee33-111">IET_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="eee33-111">IET_UUENCODE</span></span>
   - <span data-ttu-id="eee33-112">IET_QP</span><span class="sxs-lookup"><span data-stu-id="eee33-112">IET_QP</span></span>
   - <span data-ttu-id="eee33-113">IET_7BIT</span><span class="sxs-lookup"><span data-stu-id="eee33-113">IET_7BIT</span></span>
   - <span data-ttu-id="eee33-114">IET_8BIT</span><span class="sxs-lookup"><span data-stu-id="eee33-114">IET_8BIT</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eee33-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="eee33-115">Return value</span></span>

<span data-ttu-id="eee33-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="eee33-116">E_INVALIDARG</span></span>
  
> <span data-ttu-id="eee33-117">Недопустимый тип кодировки передается.</span><span class="sxs-lookup"><span data-stu-id="eee33-117">The encoding type passed was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eee33-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="eee33-118">Remarks</span></span>

<span data-ttu-id="eee33-119">Вызовите **SetEncoding** перед использованием [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) для выполнения преобразования.</span><span class="sxs-lookup"><span data-stu-id="eee33-119">Call **SetEncoding** before using [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to perform conversion.</span></span> 
  
<span data-ttu-id="eee33-120">Используйте **SetEncoding** , чтобы установить кодировку только внешний сообщения из почтового элемента.</span><span class="sxs-lookup"><span data-stu-id="eee33-120">Use **SetEncoding** to set the encoding for only the outermost message body of a mail item.</span></span> <span data-ttu-id="eee33-121">Microsoft Outlook 2010 и Microsoft Outlook 2013 выберите кодировку для отдельных вложений.</span><span class="sxs-lookup"><span data-stu-id="eee33-121">Microsoft Outlook 2010 and Microsoft Outlook 2013 choose the encoding for any individual attachments.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="eee33-122">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="eee33-122">MFCMAPI reference</span></span>

<span data-ttu-id="eee33-123">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="eee33-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="eee33-124">**����**</span><span class="sxs-lookup"><span data-stu-id="eee33-124">**File**</span></span>|<span data-ttu-id="eee33-125">**�������**</span><span class="sxs-lookup"><span data-stu-id="eee33-125">**Function**</span></span>|<span data-ttu-id="eee33-126">**�����������**</span><span class="sxs-lookup"><span data-stu-id="eee33-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="eee33-127">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="eee33-127">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="eee33-128">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="eee33-128">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="eee33-129">Mfcmapi (en) используется MimeToMAPI для преобразования EML-файла в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="eee33-129">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="eee33-130">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="eee33-130">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="eee33-131">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="eee33-131">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="eee33-132">Mfcmapi (en) используется MAPIToMIMEStm для преобразования MAPI сообщения EML-файла.</span><span class="sxs-lookup"><span data-stu-id="eee33-132">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eee33-133">См. также</span><span class="sxs-lookup"><span data-stu-id="eee33-133">See also</span></span>

- [<span data-ttu-id="eee33-134">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eee33-134">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="eee33-135">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="eee33-135">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="eee33-136">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="eee33-136">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="eee33-137">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="eee33-137">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="eee33-138">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="eee33-138">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="eee33-139">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="eee33-139">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
- [<span data-ttu-id="eee33-140">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="eee33-140">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="eee33-141">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="eee33-141">MAPI Constants</span></span>](mapi-constants.md)

