---
title: Иконвертерсессион IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession
api_type:
- COM
ms.assetid: 24f7a14a-aa6f-4045-054b-4a7aefef25e4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2db55d6318cf02dd131d07b34841922e61605147
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432319"
---
# <a name="iconvertersession--iunknown"></a><span data-ttu-id="46a39-103">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="46a39-103">IConverterSession : IUnknown</span></span>

  
  
<span data-ttu-id="46a39-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46a39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46a39-105">Позволяет выполнять преобразование между объектами MIME и сообщениями MAPI.</span><span class="sxs-lookup"><span data-stu-id="46a39-105">Allows conversions between MIME objects and MAPI messages.</span></span> <span data-ttu-id="46a39-106">Это может быть удобно при переносе сообщений через Интернет.</span><span class="sxs-lookup"><span data-stu-id="46a39-106">This can be useful in transporting messages across the Internet.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="46a39-107">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="46a39-107">Provided by:</span></span>  <br/> |<span data-ttu-id="46a39-108">Клсид_иконвертерсессион</span><span class="sxs-lookup"><span data-stu-id="46a39-108">CLSID_IConverterSession</span></span>  <br/> |
|<span data-ttu-id="46a39-109">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="46a39-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="46a39-110">Иид_иконвертерсессион</span><span class="sxs-lookup"><span data-stu-id="46a39-110">IID_IConverterSession</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="46a39-111">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="46a39-111">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46a39-112">**[Сетадрбук](iconvertersession-setadrbook.md)**</span><span class="sxs-lookup"><span data-stu-id="46a39-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span></span> <br/> |<span data-ttu-id="46a39-113">Задает необязательную адресную книгу MAPI, используемую преобразователем MAPI to MIME для разрешения неоднозначных адресов при преобразовании сообщения MAPI в поток MIME.</span><span class="sxs-lookup"><span data-stu-id="46a39-113">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
|<span data-ttu-id="46a39-114">**[Сетенкодинг](iconvertersession-setencoding.md)**</span><span class="sxs-lookup"><span data-stu-id="46a39-114">**[SetEncoding](iconvertersession-setencoding.md)**</span></span> <br/> |<span data-ttu-id="46a39-115">Инициализирует кодировку, используемую при преобразовании.</span><span class="sxs-lookup"><span data-stu-id="46a39-115">Initializes the encoding to use during conversion.</span></span>  <br/> |
| <span data-ttu-id="46a39-116">*Элемент PlaceHolder*</span><span class="sxs-lookup"><span data-stu-id="46a39-116">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="46a39-117">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="46a39-117">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="46a39-118">**[Миметомапи](iconvertersession-mimetomapi.md)**</span><span class="sxs-lookup"><span data-stu-id="46a39-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span></span> <br/> |<span data-ttu-id="46a39-119">Преобразует поток MIME в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="46a39-119">Converts a MIME stream to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="46a39-120">**[Мапитомиместм](iconvertersession-mapitomimestm.md)**</span><span class="sxs-lookup"><span data-stu-id="46a39-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span></span> <br/> |<span data-ttu-id="46a39-121">Преобразует сообщение MAPI в поток MIME.</span><span class="sxs-lookup"><span data-stu-id="46a39-121">Converts a MAPI message to a MIME stream.</span></span>  <br/> |
| <span data-ttu-id="46a39-122">*Элемент PlaceHolder*</span><span class="sxs-lookup"><span data-stu-id="46a39-122">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="46a39-123">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="46a39-123">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="46a39-124">*Элемент PlaceHolder*</span><span class="sxs-lookup"><span data-stu-id="46a39-124">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="46a39-125">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="46a39-125">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="46a39-126">*Элемент PlaceHolder*</span><span class="sxs-lookup"><span data-stu-id="46a39-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="46a39-127">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="46a39-127">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="46a39-128">**[Сеттекствраппинг](iconvertersession-settextwrapping.md)**</span><span class="sxs-lookup"><span data-stu-id="46a39-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span></span> <br/> |<span data-ttu-id="46a39-129">Задает ширину обтекания текста для потока MIME, возвращаемого преобразователем в **мапитомиместм**.</span><span class="sxs-lookup"><span data-stu-id="46a39-129">Sets the text wrapping width for a MIME stream that the converter returns in **MAPIToMIMEStm**.</span></span>  <br/> |
|<span data-ttu-id="46a39-130">**[Сетсавеформат](iconvertersession-setsaveformat.md)**</span><span class="sxs-lookup"><span data-stu-id="46a39-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span></span> <br/> |<span data-ttu-id="46a39-131">Задает формат, который преобразователь возвращает поток MIME в **мапитомиместм**.</span><span class="sxs-lookup"><span data-stu-id="46a39-131">Sets the format that the converter returns a MIME stream in **MAPIToMIMEStm**.</span></span>  <br/> |
| <span data-ttu-id="46a39-132">*Элемент PlaceHolder*</span><span class="sxs-lookup"><span data-stu-id="46a39-132">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="46a39-133">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="46a39-133">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="46a39-134">**[Сетчарсет](iconvertersession-setcharset.md)**</span><span class="sxs-lookup"><span data-stu-id="46a39-134">**[SetCharSet](iconvertersession-setcharset.md)**</span></span> <br/> |<span data-ttu-id="46a39-135">Задает необязательный набор символов, используемый преобразователем MAPI для преобразования MIME при преобразовании сообщения MAPI в поток MIME.</span><span class="sxs-lookup"><span data-stu-id="46a39-135">Specifies an optional character set that the MAPI to MIME converter uses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46a39-136">Примечания</span><span class="sxs-lookup"><span data-stu-id="46a39-136">Remarks</span></span>

<span data-ttu-id="46a39-137">ВыЗовите **сетенкодинг** , прежде чем использовать **мапитомиместм** для выполнения преобразования.</span><span class="sxs-lookup"><span data-stu-id="46a39-137">Call **SetEncoding** before using **MAPIToMIMEStm** to perform conversion.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="46a39-138">См. также</span><span class="sxs-lookup"><span data-stu-id="46a39-138">See also</span></span>



[<span data-ttu-id="46a39-139">Сведения об API преобразования MAPI-MIME</span><span class="sxs-lookup"><span data-stu-id="46a39-139">About the MAPI-MIME Conversion API</span></span>](about-the-mapi-mime-conversion-api.md)
  
[<span data-ttu-id="46a39-140">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="46a39-140">MAPI Constants</span></span>](mapi-constants.md)

