---
title: Кодировка сообщение с TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5043c338f309b5da21ca828a47daf1d8b6abfd5d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577753"
---
# <a name="encoding-a-message-with-tnef"></a><span data-ttu-id="7cda5-103">Кодировка сообщение с TNEF</span><span class="sxs-lookup"><span data-stu-id="7cda5-103">Encoding a message with TNEF</span></span>

<span data-ttu-id="7cda5-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7cda5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7cda5-105">При отправке сообщения поставщика транспорта можно создать файл, который используется для хранения сообщения во время передачи.</span><span class="sxs-lookup"><span data-stu-id="7cda5-105">When a message is submitted, the transport provider can create a file that is used to contain the message during transmission.</span></span> <span data-ttu-id="7cda5-106">Рассмотрим процедуру интерфейс [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) является переход через файл.</span><span class="sxs-lookup"><span data-stu-id="7cda5-106">Next, an [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface is wrapped around the file.</span></span> <span data-ttu-id="7cda5-107">Поставщика транспорта затем использует методы [ITnef](itnefiunknown.md) для записи свойств сообщения поток в виде с тегами, включает свойства для декодирования легко получающей поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="7cda5-107">The transport provider then uses [ITnef](itnefiunknown.md) methods to write the message properties to the stream in a tagged format that enables the properties to be easily decoded by the receiving transport providers.</span></span> 
  
<span data-ttu-id="7cda5-108">**Для представления все сообщение в одном файле**</span><span class="sxs-lookup"><span data-stu-id="7cda5-108">**To represent an entire message in a single file**</span></span>
  
1. <span data-ttu-id="7cda5-109">Получение объекта TNEF, передав объект [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) и сообщение в функцию [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="7cda5-109">Obtain a TNEF object by passing an [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="7cda5-110">Получите список всех свойств, определенных для сообщения путем вызова метода [IMAPIProp::GetPropList](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="7cda5-110">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="7cda5-111">Используйте методы [IMAPIProp](imapipropiunknown.md) , чтобы исключить все свойства, поддерживаемые системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="7cda5-111">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="7cda5-112">Во время запись этих свойств в системе обмена сообщениями в формате, необходимые для системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="7cda5-112">At an appropriate time, write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="7cda5-113">Вызов [ITnef::AddProps](itnef-addprops.md) для кодирования остальные свойства, включая все вложения.</span><span class="sxs-lookup"><span data-stu-id="7cda5-113">Call [ITnef::AddProps](itnef-addprops.md) to encode the remaining properties, including all attachments.</span></span> 
    
5. <span data-ttu-id="7cda5-114">Вызовите метод [ITnef::Finish](itnef-finish.md) для кодирования сообщений в поток TNEF после добавления все запрошенные свойства.</span><span class="sxs-lookup"><span data-stu-id="7cda5-114">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
6. <span data-ttu-id="7cda5-115">Вызовите метод [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) получает текст с тегами сообщения.</span><span class="sxs-lookup"><span data-stu-id="7cda5-115">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to obtain the tagged message text.</span></span> <span data-ttu-id="7cda5-116">Этот текст с тегами записывается в системе обмена сообщениями, с помощью методов из интерфейса OLE [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7cda5-116">This tagged text is written out to the messaging system using methods from the OLE [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
    
7. <span data-ttu-id="7cda5-117">Вызовите метод [функции IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) для освобождения объекта **ITnef** .</span><span class="sxs-lookup"><span data-stu-id="7cda5-117">Call the [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) method to release the **ITnef** object.</span></span> 
    
<span data-ttu-id="7cda5-118">**Для обработки входящего сообщения в формате TNEF**</span><span class="sxs-lookup"><span data-stu-id="7cda5-118">**To process an inbound TNEF message**</span></span>
  
1. <span data-ttu-id="7cda5-119">Получите объект MAPI сообщения из очереди MAPI и запись свойств заголовка сообщения в новое сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="7cda5-119">Get a MAPI message object from the MAPI spooler and write message header properties into the new MAPI message.</span></span>
    
2. <span data-ttu-id="7cda5-120">Создание и инициализация объекта [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) для хранения данных TNEF из входящего сообщения.</span><span class="sxs-lookup"><span data-stu-id="7cda5-120">Create and initialize an [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object to contain the TNEF data from the inbound message.</span></span> 
    
3. <span data-ttu-id="7cda5-121">Передача сообщений MAPI и объект [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) функции [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="7cda5-121">Pass the MAPI message and the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
4. <span data-ttu-id="7cda5-122">Сведения, приведенные в данных TNEF декодирования путем вызова метода [ITnef::ExtractProps](itnef-extractprops.md) .</span><span class="sxs-lookup"><span data-stu-id="7cda5-122">Decode the information in the TNEF data by calling the [ITnef::ExtractProps](itnef-extractprops.md) method.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="7cda5-123">Все действия по **ExtractProps** свойства, декодированных из конверт входящие сообщения будут перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="7cda5-123">Anything decoded by **ExtractProps** will overwrite properties decoded from the incoming message's envelope.</span></span> <span data-ttu-id="7cda5-124">То есть извлеченные свойства TNEF будет перезаписывать существующие свойства в сообщении.</span><span class="sxs-lookup"><span data-stu-id="7cda5-124">That is, extracted TNEF properties will overwrite the existing properties in a message.</span></span> 
  
5. <span data-ttu-id="7cda5-125">Процедура текст с тегами сообщения путем вызова [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) и синтаксический анализ текста для восстановления положения вложения.</span><span class="sxs-lookup"><span data-stu-id="7cda5-125">Process the tagged message text by calling [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) and parse the text to recover attachment positions.</span></span> 
    
6. <span data-ttu-id="7cda5-126">Сохраните сообщение, путем вызова [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="7cda5-126">Save the message by calling [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
7. <span data-ttu-id="7cda5-127">Освободите объект TNEF путем вызова метода [функции IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7cda5-127">Release the TNEF object by calling the [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) method.</span></span> 
    

