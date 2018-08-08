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
ms.openlocfilehash: a13d4e54900989c692add85add6853a1b511f448
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808797"
---
# <a name="iconvertersessionsetencoding"></a><span data-ttu-id="d4aee-103">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="d4aee-103">IConverterSession::SetEncoding</span></span>

<span data-ttu-id="d4aee-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d4aee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d4aee-105">Инициализирует кодировку для использования при преобразовании.</span><span class="sxs-lookup"><span data-stu-id="d4aee-105">Initializes the encoding to be used during conversion.</span></span>
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a><span data-ttu-id="d4aee-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4aee-106">Parameters</span></span>

<span data-ttu-id="d4aee-107">_et_</span><span class="sxs-lookup"><span data-stu-id="d4aee-107">_et_</span></span>
  
> <span data-ttu-id="d4aee-108">Значение [ENCODINGTYPE](http://msdn.microsoft.com/en-us/library/aa374936%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d4aee-108">An [ENCODINGTYPE](http://msdn.microsoft.com/en-us/library/aa374936%28VS.85%29.aspx) value.</span></span> <span data-ttu-id="d4aee-109">Поддерживаются только следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d4aee-109">Only the following values are supported:</span></span> 
    
   - <span data-ttu-id="d4aee-110">IET_BASE64</span><span class="sxs-lookup"><span data-stu-id="d4aee-110">IET_BASE64</span></span>
   - <span data-ttu-id="d4aee-111">IET_UUENCODE</span><span class="sxs-lookup"><span data-stu-id="d4aee-111">IET_UUENCODE</span></span>
   - <span data-ttu-id="d4aee-112">IET_QP</span><span class="sxs-lookup"><span data-stu-id="d4aee-112">IET_QP</span></span>
   - <span data-ttu-id="d4aee-113">IET_7BIT</span><span class="sxs-lookup"><span data-stu-id="d4aee-113">IET_7BIT</span></span>
   - <span data-ttu-id="d4aee-114">IET_8BIT</span><span class="sxs-lookup"><span data-stu-id="d4aee-114">IET_8BIT</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d4aee-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="d4aee-115">Return value</span></span>

<span data-ttu-id="d4aee-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d4aee-116">E_INVALIDARG</span></span>
  
> <span data-ttu-id="d4aee-117">Недопустимый тип кодировки передается.</span><span class="sxs-lookup"><span data-stu-id="d4aee-117">The encoding type passed was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d4aee-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="d4aee-118">Remarks</span></span>

<span data-ttu-id="d4aee-119">Вызовите **SetEncoding** перед использованием [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) для выполнения преобразования.</span><span class="sxs-lookup"><span data-stu-id="d4aee-119">Call **SetEncoding** before using [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to perform conversion.</span></span> 
  
<span data-ttu-id="d4aee-120">Используйте **SetEncoding** , чтобы установить кодировку только внешний сообщения из почтового элемента.</span><span class="sxs-lookup"><span data-stu-id="d4aee-120">Use **SetEncoding** to set the encoding for only the outermost message body of a mail item.</span></span> <span data-ttu-id="d4aee-121">Microsoft Outlook 2010 и Microsoft Outlook 2013 выберите кодировку для отдельных вложений.</span><span class="sxs-lookup"><span data-stu-id="d4aee-121">Microsoft Outlook 2010 and Microsoft Outlook 2013 choose the encoding for any individual attachments.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d4aee-122">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="d4aee-122">MFCMAPI reference</span></span>

<span data-ttu-id="d4aee-123">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="d4aee-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d4aee-124">**����**</span><span class="sxs-lookup"><span data-stu-id="d4aee-124">**File**</span></span>|<span data-ttu-id="d4aee-125">**�������**</span><span class="sxs-lookup"><span data-stu-id="d4aee-125">**Function**</span></span>|<span data-ttu-id="d4aee-126">**�����������**</span><span class="sxs-lookup"><span data-stu-id="d4aee-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d4aee-127">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="d4aee-127">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="d4aee-128">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="d4aee-128">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="d4aee-129">Mfcmapi (en) используется MimeToMAPI для преобразования EML-файла в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="d4aee-129">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="d4aee-130">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="d4aee-130">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="d4aee-131">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="d4aee-131">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="d4aee-132">Mfcmapi (en) используется MAPIToMIMEStm для преобразования MAPI сообщения EML-файла.</span><span class="sxs-lookup"><span data-stu-id="d4aee-132">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d4aee-133">См. также</span><span class="sxs-lookup"><span data-stu-id="d4aee-133">See also</span></span>

- [<span data-ttu-id="d4aee-134">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d4aee-134">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="d4aee-135">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="d4aee-135">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="d4aee-136">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="d4aee-136">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="d4aee-137">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="d4aee-137">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="d4aee-138">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="d4aee-138">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="d4aee-139">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="d4aee-139">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
- [<span data-ttu-id="d4aee-140">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="d4aee-140">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="d4aee-141">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="d4aee-141">MAPI Constants</span></span>](mapi-constants.md)

