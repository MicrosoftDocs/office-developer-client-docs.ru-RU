---
title: Иконвертерсессионсетадрбук
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
ms.openlocfilehash: 7645208e6a0256957deb3a71ba3e04ad125a6b61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326896"
---
# <a name="iconvertersessionsetadrbook"></a><span data-ttu-id="a88c1-103">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="a88c1-103">IConverterSession::SetAdrBook</span></span>

  
  
<span data-ttu-id="a88c1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a88c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a88c1-105">Задает необязательную адресную книгу MAPI, используемую преобразователем MAPI to MIME для разрешения неоднозначных адресов при преобразовании сообщения MAPI в поток MIME.</span><span class="sxs-lookup"><span data-stu-id="a88c1-105">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a><span data-ttu-id="a88c1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a88c1-106">Parameters</span></span>

 <span data-ttu-id="a88c1-107">_адресной_</span><span class="sxs-lookup"><span data-stu-id="a88c1-107">_pab_</span></span>
  
> <span data-ttu-id="a88c1-108">возврата Указатель на интерфейс [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) , который будет использоваться в преобразовании MAPI в MIME.</span><span class="sxs-lookup"><span data-stu-id="a88c1-108">[in] Pointer to an [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface to be used in the MAPI to MIME conversion.</span></span> <span data-ttu-id="a88c1-109">Если адресная книга больше не нужна, установите для этого параметра **значение NULL** . При этом интерфейс освобождается и сбрасывается без использования адресной книги.</span><span class="sxs-lookup"><span data-stu-id="a88c1-109">Set this parameter to **null** when you no longer need the Address Book; this releases the interface and resets the converter to not using any Address Book.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a88c1-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a88c1-110">Return value</span></span>

<span data-ttu-id="a88c1-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="a88c1-111">S_OK</span></span>
  
> <span data-ttu-id="a88c1-112">Вызов функции выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="a88c1-112">The function call is successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a88c1-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="a88c1-113">Remarks</span></span>

<span data-ttu-id="a88c1-114">Для преобразования сообщения MAPI в поток MIME обычно не требуется вход в профиль MAPI.</span><span class="sxs-lookup"><span data-stu-id="a88c1-114">Converting a MAPI message to MIME stream generally does not require logging on to a MAPI profile.</span></span> <span data-ttu-id="a88c1-115">Однако чтобы указать адресную книгу MAPI для преобразования, необходимо войти в профиль, чтобы получить адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="a88c1-115">However, specifying a MAPI Address Book for conversion requires logging on to a profile to obtain the Address Book.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a88c1-116">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a88c1-116">MFCMAPI reference</span></span>

<span data-ttu-id="a88c1-117">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a88c1-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a88c1-118">**Файл**</span><span class="sxs-lookup"><span data-stu-id="a88c1-118">**File**</span></span>|<span data-ttu-id="a88c1-119">**Функция**</span><span class="sxs-lookup"><span data-stu-id="a88c1-119">**Function**</span></span>|<span data-ttu-id="a88c1-120">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="a88c1-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a88c1-121">Мапимиме. cpp</span><span class="sxs-lookup"><span data-stu-id="a88c1-121">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="a88c1-122">Импортемлтоимессаже</span><span class="sxs-lookup"><span data-stu-id="a88c1-122">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="a88c1-123">MFCMAPI использует Миметомапи для преобразования EML файла в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="a88c1-123">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="a88c1-124">Мапимиме. cpp</span><span class="sxs-lookup"><span data-stu-id="a88c1-124">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="a88c1-125">Експортимессажетоемл</span><span class="sxs-lookup"><span data-stu-id="a88c1-125">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="a88c1-126">MFCMAPI использует Мапитомиместм для преобразования сообщения MAPI в файл EML.</span><span class="sxs-lookup"><span data-stu-id="a88c1-126">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a88c1-127">См. также</span><span class="sxs-lookup"><span data-stu-id="a88c1-127">See also</span></span>



[<span data-ttu-id="a88c1-128">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a88c1-128">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="a88c1-129">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="a88c1-129">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="a88c1-130">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="a88c1-130">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="a88c1-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="a88c1-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="a88c1-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="a88c1-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="a88c1-133">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="a88c1-133">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="a88c1-134">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="a88c1-134">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)

