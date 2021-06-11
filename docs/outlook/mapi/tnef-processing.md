---
title: Обработка TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d324fb3-d917-4502-b3a4-179c479deb79
description: '���� ���������� ���������: 5 ���� 2012 �.'
ms.openlocfilehash: 066ad3dfb64161e326b92fef7774d5b3b9461d8a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339601"
---
# <a name="tnef-processing"></a><span data-ttu-id="014c8-103">Обработка TNEF</span><span class="sxs-lookup"><span data-stu-id="014c8-103">TNEF Processing</span></span>

  
  
<span data-ttu-id="014c8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="014c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="014c8-105">В следующей серии действий описывается, как транспорты используют методы TNEF для обработки исходяющих и входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="014c8-105">The following series of actions describe how transports use TNEF methods to process outgoing and incoming messages.</span></span>
  
 <span data-ttu-id="014c8-106">**Отправка сообщения с потоком TNEF**</span><span class="sxs-lookup"><span data-stu-id="014c8-106">**To send a message that includes a TNEF stream**</span></span>
  
1. <span data-ttu-id="014c8-107">Обработать свойства сообщений, поддерживаемые системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="014c8-107">Process the message properties that are supported by the messaging system.</span></span>
    
2. <span data-ttu-id="014c8-108">Пометить сообщение определенным способом реализации, чтобы поставщик транспорта, получаюющий транспорт, мог определить, что сообщение требует обработки TNEF.</span><span class="sxs-lookup"><span data-stu-id="014c8-108">Mark the message in an implementation specific way so that the receiving transport provider can determine that the message requires TNEF processing.</span></span> <span data-ttu-id="014c8-109">Например, поставщик транспорта TNEF, отправляющий в систему обмена сообщениями SMTP, может добавить настраиваемую область загона, например "X-CONTAINS-TNEF", чтобы указать, что сообщение содержит данные TNEF.</span><span class="sxs-lookup"><span data-stu-id="014c8-109">For example, a TNEF transport provider sending to an SMTP messaging system might add a custom header field like "X-CONTAINS-TNEF" to indicate that the message contains TNEF data.</span></span>
    
3. <span data-ttu-id="014c8-110">Получение объекта TNEF и его использование для инкапсулации свойств сообщений, не поддерживаемых системой обмена сообщениями, в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="014c8-110">Obtain a TNEF object and use it to encapsulate the message properties not supported by the messaging system into a TNEF stream.</span></span>
    
4. <span data-ttu-id="014c8-111">Кодировать поток TNEF с помощью модели вложений системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="014c8-111">Encode the TNEF stream using the messaging system's attachment model.</span></span> <span data-ttu-id="014c8-112">Например, если в модели вложений вложены uuencode и они приложены к тексту сообщения, то поставщик транспорта должен uuencode поток TNEF в другое вложение.</span><span class="sxs-lookup"><span data-stu-id="014c8-112">For example, if the underlying attachment model is to uuencode attachments and append them to the message text, then the transport provider must uuencode the TNEF stream into another attachment.</span></span> <span data-ttu-id="014c8-113">Поставщик транспорта также должен реализовать метод распознавания того, какое вложение содержит закодированный поток TNEF при приеме сообщения.</span><span class="sxs-lookup"><span data-stu-id="014c8-113">The transport provider must also implement a method for recognizing which attachment contains the encoded TNEF stream when it receives a message.</span></span> <span data-ttu-id="014c8-114">Стандартный способ пометить это вложение — дать ему имя файла вложения "WINMAIL. DAT".</span><span class="sxs-lookup"><span data-stu-id="014c8-114">The standard way to mark this attachment is to give it an attachment filename of "WINMAIL.DAT".</span></span> <span data-ttu-id="014c8-115">Если ваш поставщик транспорта выполнит это, с ним смогут работать другие транспортные поставщики с поддержкой TNEF, которые следуют этой конвенции.</span><span class="sxs-lookup"><span data-stu-id="014c8-115">If your transport provider does this, any other TNEF-enabled transport providers that follow this convention will be able to interoperate with it.</span></span>
    
5. <span data-ttu-id="014c8-116">Используйте [методы интерфейса ITnef : IUnknown](itnefiunknown.md) для вставки тегов, описывающих позиции вложений сообщений в текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="014c8-116">Use [ITnef : IUnknown](itnefiunknown.md) interface methods to insert tags describing the positions of message attachments in the message text.</span></span> 
    
6. <span data-ttu-id="014c8-117">Доступ к тексту сообщения с тегами с помощью [методов IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) и отправка его в систему обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="014c8-117">Access the tagged message text through [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) methods, and send it to the messaging system.</span></span> 
    
 <span data-ttu-id="014c8-118">**Извлечение инкапсулированных свойств**</span><span class="sxs-lookup"><span data-stu-id="014c8-118">**To retrieve encapsulated properties**</span></span>
  
1. <span data-ttu-id="014c8-119">Напишите свойства, поддерживаемые системой обмена сообщениями, в новое сообщение, включая помеченный текст сообщения, содержащий инкапсулированные свойства.</span><span class="sxs-lookup"><span data-stu-id="014c8-119">Write the properties supported by the messaging system into a new message, including the tagged message text that contains the encapsulated properties.</span></span>
    
2. <span data-ttu-id="014c8-120">Расшифровка потока TNEF из правильного вложения.</span><span class="sxs-lookup"><span data-stu-id="014c8-120">Decode the TNEF stream from the proper attachment.</span></span>
    
3. <span data-ttu-id="014c8-121">Декодировать любые другие вложения и записывать их в новые вложения MAPI в сообщении.</span><span class="sxs-lookup"><span data-stu-id="014c8-121">Decode any other attachments and write them to new MAPI attachments on a message.</span></span>
    
4. <span data-ttu-id="014c8-122">Откройте поток TNEF для декодирования с помощью [функции OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="014c8-122">Open the TNEF stream for decoding using the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="014c8-123">Используйте [метод ITnef::ExtractProps](itnef-extractprops.md) для расшифровки потока TNEF и записи инкапсулированных свойств в новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="014c8-123">Use the [ITnef::ExtractProps](itnef-extractprops.md) method to decode the TNEF stream and write the encapsulated properties into the new message.</span></span> <span data-ttu-id="014c8-124">Все закодированные свойства, которые являются дубликатами некодируемых свойств, будут перезаписывать некодированные свойства при декодировании закодированные свойства.</span><span class="sxs-lookup"><span data-stu-id="014c8-124">Any encoded properties that are duplicates of nonencoded properties will overwrite the nonencoded properties when the encoded properties are decoded.</span></span> 
    
6. <span data-ttu-id="014c8-125">Используйте [метод ITnef::OpenTaggedBody](itnef-opentaggedbody.md) для разбора текста сообщения, чтобы восстановить позиции вложений из тегов в тексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="014c8-125">Use the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to parse the message text to recover attachment positions from the tags in the message text.</span></span> 
    

