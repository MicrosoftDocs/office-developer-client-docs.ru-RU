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
ms.openlocfilehash: 316e17e7804e754eed4ee4fef27211fb5173d4bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589646"
---
# <a name="iconvertersession--iunknown"></a><span data-ttu-id="42e1d-103">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="42e1d-103">IConverterSession : IUnknown</span></span>

  
  
<span data-ttu-id="42e1d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42e1d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42e1d-105">Обеспечивает преобразование между объектами MIME и сообщения MAPI.</span><span class="sxs-lookup"><span data-stu-id="42e1d-105">Allows conversions between MIME objects and MAPI messages.</span></span> <span data-ttu-id="42e1d-106">Это может быть полезно в обмен сообщениями через Интернет.</span><span class="sxs-lookup"><span data-stu-id="42e1d-106">This can be useful in transporting messages across the Internet.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="42e1d-107">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="42e1d-107">Provided by:</span></span>  <br/> |<span data-ttu-id="42e1d-108">CLSID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="42e1d-108">CLSID_IConverterSession</span></span>  <br/> |
|<span data-ttu-id="42e1d-109">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="42e1d-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="42e1d-110">IID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="42e1d-110">IID_IConverterSession</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="42e1d-111">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="42e1d-111">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="42e1d-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span><span class="sxs-lookup"><span data-stu-id="42e1d-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span></span> <br/> |<span data-ttu-id="42e1d-113">Задает необязательный MAPI адресной книге, MAPI для конвертера MIME для разрешения неоднозначных адреса при преобразовании сообщения MAPI в MIME-поток.</span><span class="sxs-lookup"><span data-stu-id="42e1d-113">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
|<span data-ttu-id="42e1d-114">**[SetEncoding](iconvertersession-setencoding.md)**</span><span class="sxs-lookup"><span data-stu-id="42e1d-114">**[SetEncoding](iconvertersession-setencoding.md)**</span></span> <br/> |<span data-ttu-id="42e1d-115">Инициализирует кодировку для использования при преобразовании.</span><span class="sxs-lookup"><span data-stu-id="42e1d-115">Initializes the encoding to use during conversion.</span></span>  <br/> |
| <span data-ttu-id="42e1d-116">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="42e1d-116">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="42e1d-117">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="42e1d-117">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="42e1d-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span><span class="sxs-lookup"><span data-stu-id="42e1d-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span></span> <br/> |<span data-ttu-id="42e1d-119">Преобразование MIME-поток сообщений MAPI.</span><span class="sxs-lookup"><span data-stu-id="42e1d-119">Converts a MIME stream to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="42e1d-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span><span class="sxs-lookup"><span data-stu-id="42e1d-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span></span> <br/> |<span data-ttu-id="42e1d-121">Преобразование сообщения MAPI в MIME-поток.</span><span class="sxs-lookup"><span data-stu-id="42e1d-121">Converts a MAPI message to a MIME stream.</span></span>  <br/> |
| <span data-ttu-id="42e1d-122">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="42e1d-122">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="42e1d-123">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="42e1d-123">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="42e1d-124">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="42e1d-124">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="42e1d-125">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="42e1d-125">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="42e1d-126">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="42e1d-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="42e1d-127">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="42e1d-127">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="42e1d-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span><span class="sxs-lookup"><span data-stu-id="42e1d-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span></span> <br/> |<span data-ttu-id="42e1d-129">Задает ширину потока MIME, который возвращает преобразователь в **MAPIToMIMEStm**обтекания.</span><span class="sxs-lookup"><span data-stu-id="42e1d-129">Sets the text wrapping width for a MIME stream that the converter returns in **MAPIToMIMEStm**.</span></span>  <br/> |
|<span data-ttu-id="42e1d-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span><span class="sxs-lookup"><span data-stu-id="42e1d-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span></span> <br/> |<span data-ttu-id="42e1d-131">Задает формат, что преобразователь возвращает MIME-поток в **MAPIToMIMEStm**.</span><span class="sxs-lookup"><span data-stu-id="42e1d-131">Sets the format that the converter returns a MIME stream in **MAPIToMIMEStm**.</span></span>  <br/> |
| <span data-ttu-id="42e1d-132">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="42e1d-132">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="42e1d-133">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="42e1d-133">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="42e1d-134">**[SetCharSet](iconvertersession-setcharset.md)**</span><span class="sxs-lookup"><span data-stu-id="42e1d-134">**[SetCharSet](iconvertersession-setcharset.md)**</span></span> <br/> |<span data-ttu-id="42e1d-135">Задает набора необязательный символ, что MAPI-MIME преобразователь использует при преобразовании сообщения MAPI в MIME-поток.</span><span class="sxs-lookup"><span data-stu-id="42e1d-135">Specifies an optional character set that the MAPI to MIME converter uses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42e1d-136">Замечания</span><span class="sxs-lookup"><span data-stu-id="42e1d-136">Remarks</span></span>

<span data-ttu-id="42e1d-137">Вызовите **SetEncoding** перед использованием **MAPIToMIMEStm** для выполнения преобразования.</span><span class="sxs-lookup"><span data-stu-id="42e1d-137">Call **SetEncoding** before using **MAPIToMIMEStm** to perform conversion.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="42e1d-138">См. также</span><span class="sxs-lookup"><span data-stu-id="42e1d-138">See also</span></span>



[<span data-ttu-id="42e1d-139">Сведения об API преобразования MAPI-MIME</span><span class="sxs-lookup"><span data-stu-id="42e1d-139">About the MAPI-MIME Conversion API</span></span>](about-the-mapi-mime-conversion-api.md)
  
[<span data-ttu-id="42e1d-140">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="42e1d-140">MAPI Constants</span></span>](mapi-constants.md)

