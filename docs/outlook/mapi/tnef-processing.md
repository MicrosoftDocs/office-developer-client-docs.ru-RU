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
# <a name="tnef-processing"></a><span data-ttu-id="3ce9c-103">Обработка TNEF</span><span class="sxs-lookup"><span data-stu-id="3ce9c-103">TNEF Processing</span></span>

  
  
<span data-ttu-id="3ce9c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ce9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ce9c-105">В приведенной ниже последовательности действий описано, как транспорты используют методы TNEF для обработки исходящих и входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-105">The following series of actions describe how transports use TNEF methods to process outgoing and incoming messages.</span></span>
  
 <span data-ttu-id="3ce9c-106">**Отправка сообщения, содержащего поток TNEF**</span><span class="sxs-lookup"><span data-stu-id="3ce9c-106">**To send a message that includes a TNEF stream**</span></span>
  
1. <span data-ttu-id="3ce9c-107">Обработка свойств сообщений, которые поддерживаются системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-107">Process the message properties that are supported by the messaging system.</span></span>
    
2. <span data-ttu-id="3ce9c-108">ПоМетка сообщения в определенном способе реализации, чтобы принимающий поставщик транспорта мог определить, что сообщение требует обработки TNEF.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-108">Mark the message in an implementation specific way so that the receiving transport provider can determine that the message requires TNEF processing.</span></span> <span data-ttu-id="3ce9c-109">Например, поставщик транспорта TNEF, отправляющий в систему обмена сообщениями SMTP, может добавить настраиваемое поле заголовка, например "X-CONTAINS-TNEF", чтобы указать, что сообщение содержит данные TNEF.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-109">For example, a TNEF transport provider sending to an SMTP messaging system might add a custom header field like "X-CONTAINS-TNEF" to indicate that the message contains TNEF data.</span></span>
    
3. <span data-ttu-id="3ce9c-110">Получите объект TNEF и используйте его для инкапсуляции свойств сообщений, не поддерживаемых системой обмена сообщениями, в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-110">Obtain a TNEF object and use it to encapsulate the message properties not supported by the messaging system into a TNEF stream.</span></span>
    
4. <span data-ttu-id="3ce9c-111">Кодирование потока TNEF с помощью модели вложений системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-111">Encode the TNEF stream using the messaging system's attachment model.</span></span> <span data-ttu-id="3ce9c-112">Например, если базовая модель вложений преобразуется в вложения uuencode и добавляет их в текст сообщения, то поставщик транспорта должен объединить поток TNEF в другое вложение.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-112">For example, if the underlying attachment model is to uuencode attachments and append them to the message text, then the transport provider must uuencode the TNEF stream into another attachment.</span></span> <span data-ttu-id="3ce9c-113">Поставщик транспорта также должен реализовать метод для распознавания вложения, которое содержит закодированный поток TNEF при получении сообщения.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-113">The transport provider must also implement a method for recognizing which attachment contains the encoded TNEF stream when it receives a message.</span></span> <span data-ttu-id="3ce9c-114">Стандартный способ пометить это вложение — присвоить файлу вложение имя WINMAIL. DAT ".</span><span class="sxs-lookup"><span data-stu-id="3ce9c-114">The standard way to mark this attachment is to give it an attachment filename of "WINMAIL.DAT".</span></span> <span data-ttu-id="3ce9c-115">Если ваш поставщик транспорта выполняет это, все другие поставщики транспорта с поддержкой TNEF, удовлетворяющие этому соглашению, смогут взаимодействовать с ним.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-115">If your transport provider does this, any other TNEF-enabled transport providers that follow this convention will be able to interoperate with it.</span></span>
    
5. <span data-ttu-id="3ce9c-116">Используйте [итнеф:](itnefiunknown.md) методы интерфейса IUnknown для вставки тегов, описывающих положения вложений в тексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-116">Use [ITnef : IUnknown](itnefiunknown.md) interface methods to insert tags describing the positions of message attachments in the message text.</span></span> 
    
6. <span data-ttu-id="3ce9c-117">Получите доступ к тексту сообщения с тегами с помощью методов [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) и отправьте его в систему обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-117">Access the tagged message text through [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) methods, and send it to the messaging system.</span></span> 
    
 <span data-ttu-id="3ce9c-118">**Извлечение инкапсулированных свойств**</span><span class="sxs-lookup"><span data-stu-id="3ce9c-118">**To retrieve encapsulated properties**</span></span>
  
1. <span data-ttu-id="3ce9c-119">ЗаПишите свойства, поддерживаемые системой обмена сообщениями, в новое сообщение, включая текст сообщения с тегами, который содержит инкапсулированные свойства.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-119">Write the properties supported by the messaging system into a new message, including the tagged message text that contains the encapsulated properties.</span></span>
    
2. <span data-ttu-id="3ce9c-120">ДеКодирование потока TNEF из надлежащего вложения.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-120">Decode the TNEF stream from the proper attachment.</span></span>
    
3. <span data-ttu-id="3ce9c-121">ДеКодирование любых других вложений и запись их в новые вложения MAPI сообщения.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-121">Decode any other attachments and write them to new MAPI attachments on a message.</span></span>
    
4. <span data-ttu-id="3ce9c-122">Откройте поток TNEF для декодирования с помощью функции [опентнефстреамекс](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="3ce9c-122">Open the TNEF stream for decoding using the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="3ce9c-123">Используйте метод [итнеф:: екстрактпропс](itnef-extractprops.md) для декодирования потока TNEF и записи инкапсулированных свойств в новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-123">Use the [ITnef::ExtractProps](itnef-extractprops.md) method to decode the TNEF stream and write the encapsulated properties into the new message.</span></span> <span data-ttu-id="3ce9c-124">Все зашифрованные свойства, которые являются дубликатами незакодированных свойств, будут перезаписывать незакодированные свойства при декодировании закодированных свойств.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-124">Any encoded properties that are duplicates of nonencoded properties will overwrite the nonencoded properties when the encoded properties are decoded.</span></span> 
    
6. <span data-ttu-id="3ce9c-125">Используйте метод [итнеф:: опентагжедбоди](itnef-opentaggedbody.md) для синтаксического анализа текста сообщения, чтобы восстановить позиции вложений из тегов в тексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="3ce9c-125">Use the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to parse the message text to recover attachment positions from the tags in the message text.</span></span> 
    

