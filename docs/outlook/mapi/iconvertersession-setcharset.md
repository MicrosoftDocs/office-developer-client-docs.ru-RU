---
title: IConverterSessionSetCharSet
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
ms.assetid: 25af3683-3a65-2d39-6f6e-76c8d36f866d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 14b2904e57852c564395f4b27c9d5270afd1454a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336661"
---
# <a name="iconvertersessionsetcharset"></a><span data-ttu-id="da23e-103">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="da23e-103">IConverterSession::SetCharSet</span></span>

  
  
<span data-ttu-id="da23e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da23e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da23e-105">Указывает необязательный набор символов, который преобразователь MAPI в MIME использует при преобразовании сообщения MAPI в поток MIME.</span><span class="sxs-lookup"><span data-stu-id="da23e-105">Specifies an optional character set that the MAPI to MIME converter use when converting a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a><span data-ttu-id="da23e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="da23e-106">Parameters</span></span>

 <span data-ttu-id="da23e-107">_fApply_</span><span class="sxs-lookup"><span data-stu-id="da23e-107">_fApply_</span></span>
  
> <span data-ttu-id="da23e-108">[in] Указывает, следует ли использовать определенный набор символов для преобразования.</span><span class="sxs-lookup"><span data-stu-id="da23e-108">[in] Indicates whether to use a specific character set for the conversion.</span></span> <span data-ttu-id="da23e-109">Установите для этого **параметра true,** чтобы применить набор символов при последующих преобразованиях.</span><span class="sxs-lookup"><span data-stu-id="da23e-109">Set this parameter to **true** to apply the character set in subsequent conversions.</span></span> <span data-ttu-id="da23e-110">Установите для этого параметра **значение false,** если вы больше не хотите применять какой-либо определенный набор символов и возвращаться к значениям по умолчанию для последующих сообщений.</span><span class="sxs-lookup"><span data-stu-id="da23e-110">Set this parameter to **false** if you no longer want to apply any specific character set and return to the defaults for subsequent messages.</span></span> 
    
 <span data-ttu-id="da23e-111">_hcharset_</span><span class="sxs-lookup"><span data-stu-id="da23e-111">_hcharset_</span></span>
  
> <span data-ttu-id="da23e-112">[in] Handle to a character set as defined in mimeole.h of Почта Windows.</span><span class="sxs-lookup"><span data-stu-id="da23e-112">[in] A handle to a character set as defined in mimeole.h of Windows Mail.</span></span> <span data-ttu-id="da23e-113">Укажите **null,** чтобы указать, что не нужно применять какой-либо определенный набор символов.</span><span class="sxs-lookup"><span data-stu-id="da23e-113">Specify **null** to specify that you do not want to apply any specific character set.</span></span> <span data-ttu-id="da23e-114">Для **значений,** не нуловых, используйте функцию, например [MimeOleGetCodePageCharset,](https://msdn.microsoft.com/library/ms714746%28VS.85%29.aspx) чтобы получить handle для набора символов.</span><span class="sxs-lookup"><span data-stu-id="da23e-114">For non- **null** values, use a function such as [MimeOleGetCodePageCharset](https://msdn.microsoft.com/library/ms714746%28VS.85%29.aspx) to obtain a handle to the character set.</span></span> 
    
 <span data-ttu-id="da23e-115">_csetapplytype_</span><span class="sxs-lookup"><span data-stu-id="da23e-115">_csetapplytype_</span></span>
  
> <span data-ttu-id="da23e-116">[in] Указывает, как применить набор символов для преобразования сообщения, как определено в mimeole.h Почта Windows.</span><span class="sxs-lookup"><span data-stu-id="da23e-116">[in] Indicates how to apply a character set to convert a message, as defined in mimeole.h of Windows Mail.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="da23e-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da23e-117">Return value</span></span>

<span data-ttu-id="da23e-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="da23e-118">S_OK</span></span>
  
> <span data-ttu-id="da23e-119">Вызов функции успешно.</span><span class="sxs-lookup"><span data-stu-id="da23e-119">The function call is successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="da23e-120">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="da23e-120">MFCMAPI reference</span></span>

<span data-ttu-id="da23e-121">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="da23e-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="da23e-122">**Файл**</span><span class="sxs-lookup"><span data-stu-id="da23e-122">**File**</span></span>|<span data-ttu-id="da23e-123">**Функция**</span><span class="sxs-lookup"><span data-stu-id="da23e-123">**Function**</span></span>|<span data-ttu-id="da23e-124">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="da23e-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="da23e-125">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="da23e-125">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="da23e-126">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="da23e-126">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="da23e-127">MFCMAPI использует MimeToMAPI для преобразования EML-файла в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="da23e-127">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="da23e-128">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="da23e-128">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="da23e-129">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="da23e-129">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="da23e-130">MFCMAPI использует MAPIToMIMEStm для преобразования сообщения MAPI в EML-файл.</span><span class="sxs-lookup"><span data-stu-id="da23e-130">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="da23e-131">См. также</span><span class="sxs-lookup"><span data-stu-id="da23e-131">See also</span></span>



[<span data-ttu-id="da23e-132">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="da23e-132">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="da23e-133">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="da23e-133">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="da23e-134">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="da23e-134">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="da23e-135">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="da23e-135">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
  
[<span data-ttu-id="da23e-136">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="da23e-136">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="da23e-137">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="da23e-137">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="da23e-138">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="da23e-138">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)

