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
# <a name="encoding-a-message-with-tnef"></a><span data-ttu-id="b2f14-103">Кодирование сообщения с использованием формата TNEF</span><span class="sxs-lookup"><span data-stu-id="b2f14-103">Encoding a message with TNEF</span></span>

<span data-ttu-id="b2f14-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2f14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2f14-105">При отправке сообщения поставщик транспорта может создать файл, который используется для отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="b2f14-105">When a message is submitted, the transport provider can create a file that is used to contain the message during transmission.</span></span> <span data-ttu-id="b2f14-106">Затем интерфейс [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) обмотается вокруг файла.</span><span class="sxs-lookup"><span data-stu-id="b2f14-106">Next, an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface is wrapped around the file.</span></span> <span data-ttu-id="b2f14-107">Затем поставщик транспорта использует методы [ITnef](itnefiunknown.md) для записи свойств сообщений в поток в помеченном формате, который позволяет легко декодировать свойства принимающих поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="b2f14-107">The transport provider then uses [ITnef](itnefiunknown.md) methods to write the message properties to the stream in a tagged format that enables the properties to be easily decoded by the receiving transport providers.</span></span> 
  
<span data-ttu-id="b2f14-108">**Для представления всего сообщения в одном файле**</span><span class="sxs-lookup"><span data-stu-id="b2f14-108">**To represent an entire message in a single file**</span></span>
  
1. <span data-ttu-id="b2f14-109">Получение объекта TNEF путем передачи [объекта IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) и сообщения в функцию [OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="b2f14-109">Obtain a TNEF object by passing an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="b2f14-110">Получите список всех определенных свойств для сообщения, позвонив по [методу IMAPIProp::GetPropList.](imapiprop-getproplist.md)</span><span class="sxs-lookup"><span data-stu-id="b2f14-110">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="b2f14-111">Используйте [методы IMAPIProp,](imapipropiunknown.md) чтобы исключить все свойства, поддерживаемые системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="b2f14-111">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="b2f14-112">В соответствующее время напишите эти свойства в систему обмена сообщениями в формате, требуемом системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="b2f14-112">At an appropriate time, write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="b2f14-113">Вызов [ITnef::AddProps для](itnef-addprops.md) кодирования оставшихся свойств, включая все вложения.</span><span class="sxs-lookup"><span data-stu-id="b2f14-113">Call [ITnef::AddProps](itnef-addprops.md) to encode the remaining properties, including all attachments.</span></span> 
    
5. <span data-ttu-id="b2f14-114">Вызов метода [ITnef::Finish,](itnef-finish.md) чтобы закодировать сообщение в поток TNEF после того, как будут добавлены все запрашиваемые свойства.</span><span class="sxs-lookup"><span data-stu-id="b2f14-114">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
6. <span data-ttu-id="b2f14-115">Чтобы получить помеченный текст сообщения, позвоните по методу [ITnef::OpenTaggedBody.](itnef-opentaggedbody.md)</span><span class="sxs-lookup"><span data-stu-id="b2f14-115">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to obtain the tagged message text.</span></span> <span data-ttu-id="b2f14-116">Этот помеченный текст выписано в систему обмена сообщениями с помощью методов из интерфейса OLE [IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2f14-116">This tagged text is written out to the messaging system using methods from the OLE [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
    
7. <span data-ttu-id="b2f14-117">Вызов метода [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) для выпуска **объекта ITnef.**</span><span class="sxs-lookup"><span data-stu-id="b2f14-117">Call the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method to release the **ITnef** object.</span></span> 
    
<span data-ttu-id="b2f14-118">**Обработка входящие сообщения TNEF**</span><span class="sxs-lookup"><span data-stu-id="b2f14-118">**To process an inbound TNEF message**</span></span>
  
1. <span data-ttu-id="b2f14-119">Получите объект сообщения MAPI из пульпера MAPI и напишите свойства загона сообщений в новое сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="b2f14-119">Get a MAPI message object from the MAPI spooler and write message header properties into the new MAPI message.</span></span>
    
2. <span data-ttu-id="b2f14-120">Создание и инициализация [объекта IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) для хранения данных TNEF из входящего сообщения.</span><span class="sxs-lookup"><span data-stu-id="b2f14-120">Create and initialize an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object to contain the TNEF data from the inbound message.</span></span> 
    
3. <span data-ttu-id="b2f14-121">Передай сообщение MAPI и [объект IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) функции [OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="b2f14-121">Pass the MAPI message and the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
4. <span data-ttu-id="b2f14-122">Расшифровка сведений в данных TNEF с помощью метода [ITnef::ExtractProps.](itnef-extractprops.md)</span><span class="sxs-lookup"><span data-stu-id="b2f14-122">Decode the information in the TNEF data by calling the [ITnef::ExtractProps](itnef-extractprops.md) method.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="b2f14-123">Все, что декодировали **в ExtractProps,** будет перезаписывать свойства, декодироваться из конверта входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="b2f14-123">Anything decoded by **ExtractProps** will overwrite properties decoded from the incoming message's envelope.</span></span> <span data-ttu-id="b2f14-124">То есть извлеченные свойства TNEF переопишет существующие свойства в сообщении.</span><span class="sxs-lookup"><span data-stu-id="b2f14-124">That is, extracted TNEF properties will overwrite the existing properties in a message.</span></span> 
  
5. <span data-ttu-id="b2f14-125">Обработать помеченный текст сообщения, позвонив [в ITnef::OpenTaggedBody](itnef-opentaggedbody.md) и разбор текста для восстановления позиций вложений.</span><span class="sxs-lookup"><span data-stu-id="b2f14-125">Process the tagged message text by calling [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) and parse the text to recover attachment positions.</span></span> 
    
6. <span data-ttu-id="b2f14-126">Сохраните сообщение, позвонив [в IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="b2f14-126">Save the message by calling [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
7. <span data-ttu-id="b2f14-127">Отпустите объект TNEF, позвонив [методу IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2f14-127">Release the TNEF object by calling the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method.</span></span> 
    

