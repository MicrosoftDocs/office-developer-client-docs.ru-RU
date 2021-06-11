---
title: IConverterSession IUnknown
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
# <a name="iconvertersession--iunknown"></a><span data-ttu-id="cbb2f-103">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cbb2f-103">IConverterSession : IUnknown</span></span>

  
  
<span data-ttu-id="cbb2f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbb2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbb2f-105">Позволяет преобразования между объектами MIME и сообщениями MAPI.</span><span class="sxs-lookup"><span data-stu-id="cbb2f-105">Allows conversions between MIME objects and MAPI messages.</span></span> <span data-ttu-id="cbb2f-106">Это может быть полезно при транспортировке сообщений через Интернет.</span><span class="sxs-lookup"><span data-stu-id="cbb2f-106">This can be useful in transporting messages across the Internet.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cbb2f-107">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="cbb2f-107">Provided by:</span></span>  <br/> |<span data-ttu-id="cbb2f-108">CLSID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="cbb2f-108">CLSID_IConverterSession</span></span>  <br/> |
|<span data-ttu-id="cbb2f-109">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="cbb2f-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="cbb2f-110">IID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="cbb2f-110">IID_IConverterSession</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="cbb2f-111">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="cbb2f-111">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cbb2f-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span><span class="sxs-lookup"><span data-stu-id="cbb2f-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span></span> <br/> |<span data-ttu-id="cbb2f-113">Указывает необязательная адресная книга MAPI, которую конвертер MAPI для MIME использует для решения неоднозначных адресов при преобразовании сообщения MAPI в поток MIME.</span><span class="sxs-lookup"><span data-stu-id="cbb2f-113">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
|<span data-ttu-id="cbb2f-114">**[SetEncoding](iconvertersession-setencoding.md)**</span><span class="sxs-lookup"><span data-stu-id="cbb2f-114">**[SetEncoding](iconvertersession-setencoding.md)**</span></span> <br/> |<span data-ttu-id="cbb2f-115">Инициализирует кодацию, используемую во время преобразования.</span><span class="sxs-lookup"><span data-stu-id="cbb2f-115">Initializes the encoding to use during conversion.</span></span>  <br/> |
| <span data-ttu-id="cbb2f-116">*Член placeholder*</span><span class="sxs-lookup"><span data-stu-id="cbb2f-116">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="cbb2f-117">*Не поддерживается или не документируется.*</span><span class="sxs-lookup"><span data-stu-id="cbb2f-117">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="cbb2f-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span><span class="sxs-lookup"><span data-stu-id="cbb2f-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span></span> <br/> |<span data-ttu-id="cbb2f-119">Преобразует поток MIME в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="cbb2f-119">Converts a MIME stream to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="cbb2f-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span><span class="sxs-lookup"><span data-stu-id="cbb2f-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span></span> <br/> |<span data-ttu-id="cbb2f-121">Преобразует сообщение MAPI в поток MIME.</span><span class="sxs-lookup"><span data-stu-id="cbb2f-121">Converts a MAPI message to a MIME stream.</span></span>  <br/> |
| <span data-ttu-id="cbb2f-122">*Член placeholder*</span><span class="sxs-lookup"><span data-stu-id="cbb2f-122">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="cbb2f-123">*Не поддерживается или не документируется.*</span><span class="sxs-lookup"><span data-stu-id="cbb2f-123">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="cbb2f-124">*Член placeholder*</span><span class="sxs-lookup"><span data-stu-id="cbb2f-124">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="cbb2f-125">*Не поддерживается или не документируется.*</span><span class="sxs-lookup"><span data-stu-id="cbb2f-125">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="cbb2f-126">*Член placeholder*</span><span class="sxs-lookup"><span data-stu-id="cbb2f-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="cbb2f-127">*Не поддерживается или не документируется.*</span><span class="sxs-lookup"><span data-stu-id="cbb2f-127">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="cbb2f-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span><span class="sxs-lookup"><span data-stu-id="cbb2f-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span></span> <br/> |<span data-ttu-id="cbb2f-129">Задает ширину текстовой упаковки для потока MIME, который конвертер возвращает в **MAPIToMIMEStm.**</span><span class="sxs-lookup"><span data-stu-id="cbb2f-129">Sets the text wrapping width for a MIME stream that the converter returns in **MAPIToMIMEStm**.</span></span>  <br/> |
|<span data-ttu-id="cbb2f-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span><span class="sxs-lookup"><span data-stu-id="cbb2f-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span></span> <br/> |<span data-ttu-id="cbb2f-131">Задает формат, в который конвертер возвращает поток MIME в **MAPIToMIMEStm.**</span><span class="sxs-lookup"><span data-stu-id="cbb2f-131">Sets the format that the converter returns a MIME stream in **MAPIToMIMEStm**.</span></span>  <br/> |
| <span data-ttu-id="cbb2f-132">*Член placeholder*</span><span class="sxs-lookup"><span data-stu-id="cbb2f-132">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="cbb2f-133">*Не поддерживается или не документируется.*</span><span class="sxs-lookup"><span data-stu-id="cbb2f-133">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="cbb2f-134">**[SetCharSet](iconvertersession-setcharset.md)**</span><span class="sxs-lookup"><span data-stu-id="cbb2f-134">**[SetCharSet](iconvertersession-setcharset.md)**</span></span> <br/> |<span data-ttu-id="cbb2f-135">Указывает необязательный набор символов, который конвертер MAPI для MIME использует при преобразовании сообщения MAPI в поток MIME.</span><span class="sxs-lookup"><span data-stu-id="cbb2f-135">Specifies an optional character set that the MAPI to MIME converter uses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cbb2f-136">Примечания</span><span class="sxs-lookup"><span data-stu-id="cbb2f-136">Remarks</span></span>

<span data-ttu-id="cbb2f-137">Вызов **SetEncoding перед** использованием **MAPIToMIMEStm для** выполнения преобразования.</span><span class="sxs-lookup"><span data-stu-id="cbb2f-137">Call **SetEncoding** before using **MAPIToMIMEStm** to perform conversion.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cbb2f-138">См. также</span><span class="sxs-lookup"><span data-stu-id="cbb2f-138">See also</span></span>



[<span data-ttu-id="cbb2f-139">Сведения об API преобразования MAPI-MIME</span><span class="sxs-lookup"><span data-stu-id="cbb2f-139">About the MAPI-MIME Conversion API</span></span>](about-the-mapi-mime-conversion-api.md)
  
[<span data-ttu-id="cbb2f-140">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="cbb2f-140">MAPI Constants</span></span>](mapi-constants.md)

