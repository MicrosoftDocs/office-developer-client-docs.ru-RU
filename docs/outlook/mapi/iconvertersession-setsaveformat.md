---
title: IConverterSessionSetSaveFormat
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
ms.assetid: e5308a94-5191-2109-a881-b4f4a7ff1c61
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b528d6ef45c02b27f8e07d151793fc338f9af7b1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394358"
---
# <a name="iconvertersessionsetsaveformat"></a><span data-ttu-id="d73b7-103">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="d73b7-103">IConverterSession::SetSaveFormat</span></span>

<span data-ttu-id="d73b7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d73b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d73b7-105">Задает формат, в котором преобразователь вернет MIME-поток в [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span><span class="sxs-lookup"><span data-stu-id="d73b7-105">Sets the format in which the converter will return a MIME stream in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetSaveFormat ( 
     MIMESAVETYPE mstSaveFormat 
);
```

## <a name="parameters"></a><span data-ttu-id="d73b7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d73b7-106">Parameters</span></span>

<span data-ttu-id="d73b7-107">_mstSaveFormat_</span><span class="sxs-lookup"><span data-stu-id="d73b7-107">_mstSaveFormat_</span></span>
  
> <span data-ttu-id="d73b7-108">[in] Сохранение форматирования для потока MIME.</span><span class="sxs-lookup"><span data-stu-id="d73b7-108">[in] The save format to be used for a MIME stream.</span></span> <span data-ttu-id="d73b7-109">Для получения дополнительных сведений см тип перечисления [MIMESAVETYPE](https://msdn.microsoft.com/library/ms715128%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d73b7-109">For more information, see the enum type [MIMESAVETYPE](https://msdn.microsoft.com/library/ms715128%28VS.85%29.aspx).</span></span>
    
  - <span data-ttu-id="d73b7-110">**SAVE_RFC1521**: использование MIME, который используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d73b7-110">**SAVE_RFC1521**: Use MIME, which is the default.</span></span>      
  - <span data-ttu-id="d73b7-111">**SAVE_RFC822**: используйте uuencode.</span><span class="sxs-lookup"><span data-stu-id="d73b7-111">**SAVE_RFC822**: Use uuencode.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="d73b7-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d73b7-112">Return values</span></span>

<span data-ttu-id="d73b7-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="d73b7-113">S_OK</span></span>
  
> <span data-ttu-id="d73b7-114">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="d73b7-114">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="d73b7-115">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d73b7-115">MFCMAPI reference</span></span>

<span data-ttu-id="d73b7-116">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="d73b7-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d73b7-117">**Файл**</span><span class="sxs-lookup"><span data-stu-id="d73b7-117">**File**</span></span>|<span data-ttu-id="d73b7-118">**Функция**</span><span class="sxs-lookup"><span data-stu-id="d73b7-118">**Function**</span></span>|<span data-ttu-id="d73b7-119">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="d73b7-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d73b7-120">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="d73b7-120">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="d73b7-121">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="d73b7-121">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="d73b7-122">Mfcmapi (en) используется MimeToMAPI для преобразования EML-файла в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="d73b7-122">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="d73b7-123">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="d73b7-123">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="d73b7-124">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="d73b7-124">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="d73b7-125">Mfcmapi (en) используется MAPIToMIMEStm для преобразования MAPI сообщения EML-файла.</span><span class="sxs-lookup"><span data-stu-id="d73b7-125">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d73b7-126">См. также</span><span class="sxs-lookup"><span data-stu-id="d73b7-126">See also</span></span>

- [<span data-ttu-id="d73b7-127">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d73b7-127">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="d73b7-128">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="d73b7-128">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="d73b7-129">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="d73b7-129">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="d73b7-130">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="d73b7-130">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="d73b7-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="d73b7-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="d73b7-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="d73b7-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
- [<span data-ttu-id="d73b7-133">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="d73b7-133">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="d73b7-134">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="d73b7-134">MAPI Constants</span></span>](mapi-constants.md)

