---
title: Кодирование сообщения с использованием формата TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cdaa03cfbc0bbd0fcf6a320ecf8fae9f372d5781
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336703"
---
# <a name="encoding-a-message-with-tnef"></a><span data-ttu-id="3365c-103">Кодирование сообщения с использованием формата TNEF</span><span class="sxs-lookup"><span data-stu-id="3365c-103">Encoding a message with TNEF</span></span>

<span data-ttu-id="3365c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3365c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3365c-105">При отправке сообщения поставщик транспорта может создать файл, который будет использоваться для хранения сообщения во время передачи.</span><span class="sxs-lookup"><span data-stu-id="3365c-105">When a message is submitted, the transport provider can create a file that is used to contain the message during transmission.</span></span> <span data-ttu-id="3365c-106">После этого интерфейс [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) упаковывается вокруг файла.</span><span class="sxs-lookup"><span data-stu-id="3365c-106">Next, an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface is wrapped around the file.</span></span> <span data-ttu-id="3365c-107">Затем поставщик транспорта использует методы [итнеф](itnefiunknown.md) для записи свойств сообщения в поток в формате с тегом, что позволяет легко раскодировать их принимающими поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="3365c-107">The transport provider then uses [ITnef](itnefiunknown.md) methods to write the message properties to the stream in a tagged format that enables the properties to be easily decoded by the receiving transport providers.</span></span> 
  
<span data-ttu-id="3365c-108">**Представление всего сообщения в отдельном файле**</span><span class="sxs-lookup"><span data-stu-id="3365c-108">**To represent an entire message in a single file**</span></span>
  
1. <span data-ttu-id="3365c-109">Получите объект TNEF, передав объект [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) и сообщение в функцию [опентнефстреамекс](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="3365c-109">Obtain a TNEF object by passing an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="3365c-110">Получите список всех определенных свойств сообщения, вызвав метод [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="3365c-110">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="3365c-111">Используйте методы [IMAPIProp](imapipropiunknown.md) , чтобы исключить все свойства, поддерживаемые системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="3365c-111">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="3365c-112">В нужное время запишите эти свойства в систему обмена сообщениями в формате, требуемом системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="3365c-112">At an appropriate time, write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="3365c-113">Call [итнеф:: аддпропс](itnef-addprops.md) для кодирования остальных свойств, включая все вложения.</span><span class="sxs-lookup"><span data-stu-id="3365c-113">Call [ITnef::AddProps](itnef-addprops.md) to encode the remaining properties, including all attachments.</span></span> 
    
5. <span data-ttu-id="3365c-114">Вызовите метод [итнеф:: Finish](itnef-finish.md) для кодирования сообщения в поток TNEF после добавления всех запрошенных свойств.</span><span class="sxs-lookup"><span data-stu-id="3365c-114">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
6. <span data-ttu-id="3365c-115">Вызовите метод [итнеф:: опентагжедбоди](itnef-opentaggedbody.md) , чтобы получить текст сообщения с тегами.</span><span class="sxs-lookup"><span data-stu-id="3365c-115">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to obtain the tagged message text.</span></span> <span data-ttu-id="3365c-116">Этот текст с тегами записывается в систему обмена сообщениями с помощью методов из интерфейса OLE [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3365c-116">This tagged text is written out to the messaging system using methods from the OLE [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
    
7. <span data-ttu-id="3365c-117">Вызовите метод [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) , чтобы освободить объект **итнеф** .</span><span class="sxs-lookup"><span data-stu-id="3365c-117">Call the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method to release the **ITnef** object.</span></span> 
    
<span data-ttu-id="3365c-118">**Обработка входящего сообщения в формате TNEF**</span><span class="sxs-lookup"><span data-stu-id="3365c-118">**To process an inbound TNEF message**</span></span>
  
1. <span data-ttu-id="3365c-119">Получение объекта сообщения MAPI из буфера обмена MAPI и запись свойств заголовка сообщения в новое сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="3365c-119">Get a MAPI message object from the MAPI spooler and write message header properties into the new MAPI message.</span></span>
    
2. <span data-ttu-id="3365c-120">Создайте и инициализируйте объект [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) , который будет содержать данные TNEF из входящего сообщения.</span><span class="sxs-lookup"><span data-stu-id="3365c-120">Create and initialize an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object to contain the TNEF data from the inbound message.</span></span> 
    
3. <span data-ttu-id="3365c-121">Передайте сообщение MAPI и объект [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) в функцию [опентнефстреамекс](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="3365c-121">Pass the MAPI message and the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
4. <span data-ttu-id="3365c-122">Расшифровать данные в формате TNEF, вызвав метод [итнеф:: екстрактпропс](itnef-extractprops.md) .</span><span class="sxs-lookup"><span data-stu-id="3365c-122">Decode the information in the TNEF data by calling the [ITnef::ExtractProps](itnef-extractprops.md) method.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="3365c-123">Все, что раскодировано с помощью **екстрактпропс** , заменят свойства, декодированные из конверта входящего сообщения.</span><span class="sxs-lookup"><span data-stu-id="3365c-123">Anything decoded by **ExtractProps** will overwrite properties decoded from the incoming message's envelope.</span></span> <span data-ttu-id="3365c-124">То есть извлеченные свойства TNEF будут перезаписаны существующие свойства сообщения.</span><span class="sxs-lookup"><span data-stu-id="3365c-124">That is, extracted TNEF properties will overwrite the existing properties in a message.</span></span> 
  
5. <span data-ttu-id="3365c-125">Обработайте текст сообщения с тегами с помощью вызова [итнеф:: опентагжедбоди](itnef-opentaggedbody.md) и синтаксического анализа текста для восстановления положений вложений.</span><span class="sxs-lookup"><span data-stu-id="3365c-125">Process the tagged message text by calling [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) and parse the text to recover attachment positions.</span></span> 
    
6. <span data-ttu-id="3365c-126">Сохраните сообщение, вызвав [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="3365c-126">Save the message by calling [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
7. <span data-ttu-id="3365c-127">Освободите объект TNEF, вызвав метод [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3365c-127">Release the TNEF object by calling the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method.</span></span> 
    

