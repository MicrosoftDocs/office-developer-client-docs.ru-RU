---
title: Иконвертерсессионсетсавеформат
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336640"
---
# <a name="iconvertersessionsetsaveformat"></a><span data-ttu-id="062d5-103">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="062d5-103">IConverterSession::SetSaveFormat</span></span>

<span data-ttu-id="062d5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="062d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="062d5-105">Задает формат, в котором преобразователь будет возвращать MIME поток в [иконвертерсессион:: мапитомиместм](iconvertersession-mapitomimestm.md).</span><span class="sxs-lookup"><span data-stu-id="062d5-105">Sets the format in which the converter will return a MIME stream in [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md).</span></span>
  
```cpp
HRESULT IConverterSession::SetSaveFormat ( 
     MIMESAVETYPE mstSaveFormat 
);
```

## <a name="parameters"></a><span data-ttu-id="062d5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="062d5-106">Parameters</span></span>

<span data-ttu-id="062d5-107">_Мстсавеформат_</span><span class="sxs-lookup"><span data-stu-id="062d5-107">_mstSaveFormat_</span></span>
  
> <span data-ttu-id="062d5-108">возврата Формат сохранения, используемый для потока MIME.</span><span class="sxs-lookup"><span data-stu-id="062d5-108">[in] The save format to be used for a MIME stream.</span></span> <span data-ttu-id="062d5-109">Дополнительные сведения см. в разделе enum Type [мимесаветипе](https://msdn.microsoft.com/library/ms715128%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="062d5-109">For more information, see the enum type [MIMESAVETYPE](https://msdn.microsoft.com/library/ms715128%28VS.85%29.aspx).</span></span>
    
  - <span data-ttu-id="062d5-110">**SAVE_RFC1521**: использовать MIME, который является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="062d5-110">**SAVE_RFC1521**: Use MIME, which is the default.</span></span>      
  - <span data-ttu-id="062d5-111">**SAVE_RFC822**: используйте кодировку UUEncode.</span><span class="sxs-lookup"><span data-stu-id="062d5-111">**SAVE_RFC822**: Use uuencode.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="062d5-112">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="062d5-112">Return values</span></span>

<span data-ttu-id="062d5-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="062d5-113">S_OK</span></span>
  
> <span data-ttu-id="062d5-114">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="062d5-114">The call was successful.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="062d5-115">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="062d5-115">MFCMAPI reference</span></span>

<span data-ttu-id="062d5-116">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="062d5-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="062d5-117">**Файл**</span><span class="sxs-lookup"><span data-stu-id="062d5-117">**File**</span></span>|<span data-ttu-id="062d5-118">**Функция**</span><span class="sxs-lookup"><span data-stu-id="062d5-118">**Function**</span></span>|<span data-ttu-id="062d5-119">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="062d5-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="062d5-120">Мапимиме. cpp</span><span class="sxs-lookup"><span data-stu-id="062d5-120">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="062d5-121">Импортемлтоимессаже</span><span class="sxs-lookup"><span data-stu-id="062d5-121">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="062d5-122">MFCMAPI использует Миметомапи для преобразования EML файла в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="062d5-122">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="062d5-123">Мапимиме. cpp</span><span class="sxs-lookup"><span data-stu-id="062d5-123">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="062d5-124">Експортимессажетоемл</span><span class="sxs-lookup"><span data-stu-id="062d5-124">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="062d5-125">MFCMAPI использует Мапитомиместм для преобразования сообщения MAPI в файл EML.</span><span class="sxs-lookup"><span data-stu-id="062d5-125">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="062d5-126">См. также</span><span class="sxs-lookup"><span data-stu-id="062d5-126">See also</span></span>

- [<span data-ttu-id="062d5-127">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="062d5-127">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
- [<span data-ttu-id="062d5-128">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="062d5-128">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
- [<span data-ttu-id="062d5-129">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="062d5-129">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
- [<span data-ttu-id="062d5-130">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="062d5-130">IConverterSession::SetAdrBook</span></span>](iconvertersession-setadrbook.md)
- [<span data-ttu-id="062d5-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="062d5-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
- [<span data-ttu-id="062d5-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="062d5-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
- [<span data-ttu-id="062d5-133">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="062d5-133">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)
- [<span data-ttu-id="062d5-134">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="062d5-134">MAPI Constants</span></span>](mapi-constants.md)

