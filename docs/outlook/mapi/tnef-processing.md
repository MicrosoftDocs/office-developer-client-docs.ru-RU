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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399572"
---
# <a name="tnef-processing"></a><span data-ttu-id="78167-103">Обработка TNEF</span><span class="sxs-lookup"><span data-stu-id="78167-103">TNEF Processing</span></span>

  
  
<span data-ttu-id="78167-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78167-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78167-105">Следующая последовательность действий описывают, как транспортов использовать методы TNEF для обработки входящих и исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="78167-105">The following series of actions describe how transports use TNEF methods to process outgoing and incoming messages.</span></span>
  
 <span data-ttu-id="78167-106">**Чтобы отправить сообщение, которое включает в себя поток TNEF**</span><span class="sxs-lookup"><span data-stu-id="78167-106">**To send a message that includes a TNEF stream**</span></span>
  
1. <span data-ttu-id="78167-107">Обработать свойства сообщений, поддерживаемые системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="78167-107">Process the message properties that are supported by the messaging system.</span></span>
    
2. <span data-ttu-id="78167-108">Пометить как сообщения в реализации конкретных способом, чтобы получающей поставщика транспорта можно определить, что сообщение требуется обработка TNEF.</span><span class="sxs-lookup"><span data-stu-id="78167-108">Mark the message in an implementation specific way so that the receiving transport provider can determine that the message requires TNEF processing.</span></span> <span data-ttu-id="78167-109">Например поставщика транспорта TNEF, отправка SMTP системы обмена сообщениями добавить настраиваемое поле заголовка как «X-содержит-TNEF» для указания, что сообщение содержит данные TNEF.</span><span class="sxs-lookup"><span data-stu-id="78167-109">For example, a TNEF transport provider sending to an SMTP messaging system might add a custom header field like "X-CONTAINS-TNEF" to indicate that the message contains TNEF data.</span></span>
    
3. <span data-ttu-id="78167-110">Получение объекта TNEF и используйте его для инкапсуляции свойства сообщений, не поддерживается системой обмена сообщениями в поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="78167-110">Obtain a TNEF object and use it to encapsulate the message properties not supported by the messaging system into a TNEF stream.</span></span>
    
4. <span data-ttu-id="78167-111">Кодирование поток TNEF, с помощью модели вложения системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="78167-111">Encode the TNEF stream using the messaging system's attachment model.</span></span> <span data-ttu-id="78167-112">К примеру Если базовую модель вложений для вложений uuencode и добавить их в текст сообщения, затем поставщика транспорта необходимо uuencode поток TNEF в другой вложения.</span><span class="sxs-lookup"><span data-stu-id="78167-112">For example, if the underlying attachment model is to uuencode attachments and append them to the message text, then the transport provider must uuencode the TNEF stream into another attachment.</span></span> <span data-ttu-id="78167-113">Поставщика транспорта, также необходимо реализовать метод для определения, какой вложение содержит зашифрованный поток TNEF при получении сообщения.</span><span class="sxs-lookup"><span data-stu-id="78167-113">The transport provider must also implement a method for recognizing which attachment contains the encoded TNEF stream when it receives a message.</span></span> <span data-ttu-id="78167-114">Стандартный способ пометить это вложение — задайте для него файла вложения «WINMAIL. DAT».</span><span class="sxs-lookup"><span data-stu-id="78167-114">The standard way to mark this attachment is to give it an attachment filename of "WINMAIL.DAT".</span></span> <span data-ttu-id="78167-115">Если ваш поставщик транспорта делает это, других поставщиков включена поддержка формата TNEF транспорта, выполните эти соглашения могут взаимодействовать с ним.</span><span class="sxs-lookup"><span data-stu-id="78167-115">If your transport provider does this, any other TNEF-enabled transport providers that follow this convention will be able to interoperate with it.</span></span>
    
5. <span data-ttu-id="78167-116">Использование [ITnef: IUnknown](itnefiunknown.md) интерфейс методов для вставки теги, описывающее положения вложений сообщений в качестве текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="78167-116">Use [ITnef : IUnknown](itnefiunknown.md) interface methods to insert tags describing the positions of message attachments in the message text.</span></span> 
    
6. <span data-ttu-id="78167-117">Доступ к текст с тегами сообщения с помощью методов [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) и отправьте его в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="78167-117">Access the tagged message text through [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) methods, and send it to the messaging system.</span></span> 
    
 <span data-ttu-id="78167-118">**Для получения инкапсулированное свойства**</span><span class="sxs-lookup"><span data-stu-id="78167-118">**To retrieve encapsulated properties**</span></span>
  
1. <span data-ttu-id="78167-119">Написание свойств, доступных в системе обмена сообщениями в новые сообщения, включая текст с тегами сообщения, содержащий инкапсулированное свойства.</span><span class="sxs-lookup"><span data-stu-id="78167-119">Write the properties supported by the messaging system into a new message, including the tagged message text that contains the encapsulated properties.</span></span>
    
2. <span data-ttu-id="78167-120">Декодирования поток TNEF из соответствующих прав вложения.</span><span class="sxs-lookup"><span data-stu-id="78167-120">Decode the TNEF stream from the proper attachment.</span></span>
    
3. <span data-ttu-id="78167-121">Декодирования другие вложения и записи их в новый вложений MAPI на сообщение.</span><span class="sxs-lookup"><span data-stu-id="78167-121">Decode any other attachments and write them to new MAPI attachments on a message.</span></span>
    
4. <span data-ttu-id="78167-122">Откройте в потоке TNEF для декодирования с помощью функции [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="78167-122">Open the TNEF stream for decoding using the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="78167-123">Метод [ITnef::ExtractProps](itnef-extractprops.md) используется для декодирования TNEF потока и запись инкапсулированное свойств в новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="78167-123">Use the [ITnef::ExtractProps](itnef-extractprops.md) method to decode the TNEF stream and write the encapsulated properties into the new message.</span></span> <span data-ttu-id="78167-124">Любые закодированный свойства, которые дублируют nonencoded свойства будут перезаписаны nonencoded свойства при декодирование закодированный свойства.</span><span class="sxs-lookup"><span data-stu-id="78167-124">Any encoded properties that are duplicates of nonencoded properties will overwrite the nonencoded properties when the encoded properties are decoded.</span></span> 
    
6. <span data-ttu-id="78167-125">Используйте метод [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) для анализа текста сообщения для восстановления положения вложения из теги в качестве текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="78167-125">Use the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to parse the message text to recover attachment positions from the tags in the message text.</span></span> 
    

