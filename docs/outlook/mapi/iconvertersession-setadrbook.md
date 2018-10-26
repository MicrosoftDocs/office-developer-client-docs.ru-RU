---
title: IConverterSessionSetAdrBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetAdrBook
api_type:
- COM
ms.assetid: d276ab19-17f4-01c7-4b44-b578e631b5fe
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ae00fd0711b8fcae01db6a89da7607d79d8757c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584361"
---
# <a name="iconvertersessionsetadrbook"></a><span data-ttu-id="f6a16-103">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="f6a16-103">IConverterSession::SetAdrBook</span></span>

  
  
<span data-ttu-id="f6a16-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6a16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6a16-105">Задает необязательный MAPI адресной книге, MAPI для конвертера MIME для разрешения неоднозначных адреса при преобразовании сообщения MAPI в MIME-поток.</span><span class="sxs-lookup"><span data-stu-id="f6a16-105">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a><span data-ttu-id="f6a16-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6a16-106">Parameters</span></span>

 <span data-ttu-id="f6a16-107">_адресной книги_</span><span class="sxs-lookup"><span data-stu-id="f6a16-107">_pab_</span></span>
  
> <span data-ttu-id="f6a16-108">[in] Указатель на [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) интерфейс для использования в MAPI для преобразования MIME.</span><span class="sxs-lookup"><span data-stu-id="f6a16-108">[in] Pointer to an [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface to be used in the MAPI to MIME conversion.</span></span> <span data-ttu-id="f6a16-109">Присвойте этому параметру значение **null** , если нет необходимости в адресной книге; Это освобождает интерфейс и сбрасывает преобразователь не, используя любой адресной книги.</span><span class="sxs-lookup"><span data-stu-id="f6a16-109">Set this parameter to **null** when you no longer need the Address Book; this releases the interface and resets the converter to not using any Address Book.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f6a16-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6a16-110">Return value</span></span>

<span data-ttu-id="f6a16-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="f6a16-111">S_OK</span></span>
  
> <span data-ttu-id="f6a16-112">Вызов функции выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="f6a16-112">The function call is successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f6a16-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="f6a16-113">Remarks</span></span>

<span data-ttu-id="f6a16-114">Преобразование MAPI сообщений MIME потоке обычно не требуется вход в профиль MAPI.</span><span class="sxs-lookup"><span data-stu-id="f6a16-114">Converting a MAPI message to MIME stream generally does not require logging on to a MAPI profile.</span></span> <span data-ttu-id="f6a16-115">Тем не менее определяющее адресную книгу MAPI для преобразования требуется вход в систему в профиль, чтобы получить адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="f6a16-115">However, specifying a MAPI Address Book for conversion requires logging on to a profile to obtain the Address Book.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f6a16-116">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f6a16-116">MFCMAPI reference</span></span>

<span data-ttu-id="f6a16-117">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="f6a16-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f6a16-118">**Файл**</span><span class="sxs-lookup"><span data-stu-id="f6a16-118">**File**</span></span>|<span data-ttu-id="f6a16-119">**Функция**</span><span class="sxs-lookup"><span data-stu-id="f6a16-119">**Function**</span></span>|<span data-ttu-id="f6a16-120">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="f6a16-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f6a16-121">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="f6a16-121">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="f6a16-122">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="f6a16-122">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="f6a16-123">Mfcmapi (en) используется MimeToMAPI для преобразования EML-файла в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="f6a16-123">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="f6a16-124">MapiMime.cpp</span><span class="sxs-lookup"><span data-stu-id="f6a16-124">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="f6a16-125">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="f6a16-125">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="f6a16-126">Mfcmapi (en) используется MAPIToMIMEStm для преобразования MAPI сообщения EML-файла.</span><span class="sxs-lookup"><span data-stu-id="f6a16-126">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f6a16-127">См. также</span><span class="sxs-lookup"><span data-stu-id="f6a16-127">See also</span></span>



[<span data-ttu-id="f6a16-128">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f6a16-128">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="f6a16-129">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="f6a16-129">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="f6a16-130">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="f6a16-130">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="f6a16-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="f6a16-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="f6a16-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="f6a16-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="f6a16-133">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="f6a16-133">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="f6a16-134">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="f6a16-134">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)

