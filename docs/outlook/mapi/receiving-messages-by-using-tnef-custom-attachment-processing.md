---
title: Получение сообщений с использованием настраиваемой обработки вложений TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: '���� ���������� ���������: 7 ������� 2015 �.'
ms.openlocfilehash: 18fc0983554284355dcdfb301fd41a0161a860fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812121"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="2fa73-103">Получение сообщений с использованием настраиваемой обработки вложений TNEF</span><span class="sxs-lookup"><span data-stu-id="2fa73-103">Receiving Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="2fa73-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2fa73-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2fa73-105">Чтобы получать сообщения в формате TNEF с настроенной вложения обработки:</span><span class="sxs-lookup"><span data-stu-id="2fa73-105">To receive a TNEF message with customized attachment processing:</span></span>
  
1. <span data-ttu-id="2fa73-106">Импорт всех передаваемого свойств — те, которые поддерживает системы обмена сообщениями — из входящего сообщения в новое сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="2fa73-106">Import all the transmittable properties — those that the messaging system supports — from the incoming message into a new MAPI message.</span></span> <span data-ttu-id="2fa73-107">Этот компонент включает текст сообщения, который содержит поток данных TNEF.</span><span class="sxs-lookup"><span data-stu-id="2fa73-107">This includes the message text, which contains the TNEF data stream.</span></span>
    
2. <span data-ttu-id="2fa73-108">Определение и декодирования специальные вложения, содержащий поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="2fa73-108">Identify and decode the special attachment that contains the TNEF stream.</span></span>
    
3. <span data-ttu-id="2fa73-109">Извлеките все вложения из входящего сообщения в MAPI вложений в новое сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="2fa73-109">Extract all the attachments from the incoming message into MAPI attachments on the new MAPI message.</span></span> <span data-ttu-id="2fa73-110">Восстановленную имена файлов, или других идентификационные маркеров на вложения, должны размещаться в свойство **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) нового вложения таким образом, метод [ITnef::ExtractProps](itnef-extractprops.md) позднее можно связать правильный вложения с тегами вложения, закодированный в качестве текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="2fa73-110">The recovered filenames, or other identifying markers on the attachments, should be placed into the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property of the new attachments so that the [ITnef::ExtractProps](itnef-extractprops.md) method can later associate the correct attachment with the attachment tags encoded in the message text.</span></span> 
    
4. <span data-ttu-id="2fa73-111">Создание интерфейса OLE **IStream** обтекания декодированное поток TNEF и использовать этот объект, а также новые сообщения MAPI в вызове функции [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="2fa73-111">Create an OLE **IStream** interface to wrap around the decoded TNEF stream and use that object along with the new MAPI message in a call to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="2fa73-112">Вызовите метод **ITnef::ExtractProps** для восстановления из потока данных TNEF nontransmittable свойств в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="2fa73-112">Call the **ITnef::ExtractProps** method to recover the nontransmittable properties on the message from the TNEF data stream.</span></span> 
    
6. <span data-ttu-id="2fa73-113">Вызовите метод [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) с набором флаги MAPI_CREATE и MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="2fa73-113">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method with the MAPI_CREATE and MAPI_MODIFY flags set.</span></span> <span data-ttu-id="2fa73-114">Этот вызов Удаляет теги вложения из текста сообщения и преобразует их в сведения о должности вложения в сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="2fa73-114">This call removes the attachment tags from the message text and converts them into attachment position information in the MAPI message.</span></span> 
    
7. <span data-ttu-id="2fa73-115">Доставить сообщение через диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="2fa73-115">Deliver the message through the MAPI spooler.</span></span>
    

