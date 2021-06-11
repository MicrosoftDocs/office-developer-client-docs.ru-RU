---
title: Получение сообщений с помощью пользовательской обработки вложений TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: '���� ���������� ���������: 7 ������� 2015 �.'
ms.openlocfilehash: 046b537d41b318fa857ef77f1906edcf2c3aa2bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429322"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="9e72a-103">Получение сообщений с помощью пользовательской обработки вложений TNEF</span><span class="sxs-lookup"><span data-stu-id="9e72a-103">Receiving Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="9e72a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e72a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e72a-105">Получение сообщения TNEF с настраиваемой обработкой вложений:</span><span class="sxs-lookup"><span data-stu-id="9e72a-105">To receive a TNEF message with customized attachment processing:</span></span>
  
1. <span data-ttu-id="9e72a-106">Импортировать все передаваемые свойства — те, которые поддерживает система обмена сообщениями — из входящих сообщений в новое сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e72a-106">Import all the transmittable properties — those that the messaging system supports — from the incoming message into a new MAPI message.</span></span> <span data-ttu-id="9e72a-107">Это включает текст сообщения, содержащий поток данных TNEF.</span><span class="sxs-lookup"><span data-stu-id="9e72a-107">This includes the message text, which contains the TNEF data stream.</span></span>
    
2. <span data-ttu-id="9e72a-108">Определите и расшифруйте специальное вложение, содержаное поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="9e72a-108">Identify and decode the special attachment that contains the TNEF stream.</span></span>
    
3. <span data-ttu-id="9e72a-109">Извлекать все вложения из входящих сообщений в вложения MAPI в новом сообщении MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e72a-109">Extract all the attachments from the incoming message into MAPI attachments on the new MAPI message.</span></span> <span data-ttu-id="9e72a-110">Восстановленные имена файлов или другие маркеры идентификации на вложениях должны быть помещены в **свойство PR_ATTACH_TRANSPORT_NAME** [(PidTagAttachTransportName)](pidtagattachtransportname-canonical-property.md)новых вложений, чтобы метод [ITnef::ExtractProps](itnef-extractprops.md) позже связывал правильное вложение с тегами вложений, закодированных в тексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="9e72a-110">The recovered filenames, or other identifying markers on the attachments, should be placed into the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property of the new attachments so that the [ITnef::ExtractProps](itnef-extractprops.md) method can later associate the correct attachment with the attachment tags encoded in the message text.</span></span> 
    
4. <span data-ttu-id="9e72a-111">Создайте интерфейс OLE **IStream** для обмотки расшифровки потока TNEF и используйте этот объект вместе с новым сообщением MAPI в вызове функции [OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="9e72a-111">Create an OLE **IStream** interface to wrap around the decoded TNEF stream and use that object along with the new MAPI message in a call to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="9e72a-112">Вызов метода **ITnef::ExtractProps** для восстановления нетрансмитируемых свойств сообщения из потока данных TNEF.</span><span class="sxs-lookup"><span data-stu-id="9e72a-112">Call the **ITnef::ExtractProps** method to recover the nontransmittable properties on the message from the TNEF data stream.</span></span> 
    
6. <span data-ttu-id="9e72a-113">Вызов метода [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) с набором MAPI_CREATE и MAPI_MODIFY флагов.</span><span class="sxs-lookup"><span data-stu-id="9e72a-113">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method with the MAPI_CREATE and MAPI_MODIFY flags set.</span></span> <span data-ttu-id="9e72a-114">Этот вызов удаляет теги вложений из текста сообщения и преобразует их в сведения о положении вложений в сообщении MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e72a-114">This call removes the attachment tags from the message text and converts them into attachment position information in the MAPI message.</span></span> 
    
7. <span data-ttu-id="9e72a-115">Доставка сообщения через шпалер MAPI.</span><span class="sxs-lookup"><span data-stu-id="9e72a-115">Deliver the message through the MAPI spooler.</span></span>
    

