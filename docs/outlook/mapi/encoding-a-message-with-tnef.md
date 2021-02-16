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
# <a name="encoding-a-message-with-tnef"></a><span data-ttu-id="77eb7-103">Кодирование сообщения с использованием формата TNEF</span><span class="sxs-lookup"><span data-stu-id="77eb7-103">Encoding a message with TNEF</span></span>

<span data-ttu-id="77eb7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77eb7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77eb7-105">При отправке сообщения поставщик транспорта может создать файл, который будет содержать сообщение во время передачи.</span><span class="sxs-lookup"><span data-stu-id="77eb7-105">When a message is submitted, the transport provider can create a file that is used to contain the message during transmission.</span></span> <span data-ttu-id="77eb7-106">Затем интерфейс [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) обвязывают файл.</span><span class="sxs-lookup"><span data-stu-id="77eb7-106">Next, an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface is wrapped around the file.</span></span> <span data-ttu-id="77eb7-107">Затем поставщик транспорта использует методы [ITnef](itnefiunknown.md) для записи свойств сообщения в поток в формате с тегами, который позволяет принимающим поставщикам транспорта легко декодировать свойства.</span><span class="sxs-lookup"><span data-stu-id="77eb7-107">The transport provider then uses [ITnef](itnefiunknown.md) methods to write the message properties to the stream in a tagged format that enables the properties to be easily decoded by the receiving transport providers.</span></span> 
  
<span data-ttu-id="77eb7-108">**Чтобы представить все сообщение в одном файле**</span><span class="sxs-lookup"><span data-stu-id="77eb7-108">**To represent an entire message in a single file**</span></span>
  
1. <span data-ttu-id="77eb7-109">Получите объект TNEF, передав [объект IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) и сообщение в [функцию OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="77eb7-109">Obtain a TNEF object by passing an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="77eb7-110">Получите список всех определенных свойств сообщения, вызывая метод [IMAPIProp::GetPropList.](imapiprop-getproplist.md)</span><span class="sxs-lookup"><span data-stu-id="77eb7-110">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="77eb7-111">Используйте [методы IMAPIProp,](imapipropiunknown.md) чтобы исключить все свойства, поддерживаемые системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="77eb7-111">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="77eb7-112">В соответствующее время запишите эти свойства в систему обмена сообщениями в формате, требуемом системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="77eb7-112">At an appropriate time, write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="77eb7-113">Вызовите [ITnef::AddProps,](itnef-addprops.md) чтобы закодировать оставшиеся свойства, включая все вложения.</span><span class="sxs-lookup"><span data-stu-id="77eb7-113">Call [ITnef::AddProps](itnef-addprops.md) to encode the remaining properties, including all attachments.</span></span> 
    
5. <span data-ttu-id="77eb7-114">Вызовите [метод ITnef::Finish,](itnef-finish.md) чтобы закодировать сообщение в поток TNEF после того, как будут добавлены все запрашиваемые свойства.</span><span class="sxs-lookup"><span data-stu-id="77eb7-114">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
6. <span data-ttu-id="77eb7-115">Вызовите [метод ITnef::OpenTaggedBody,](itnef-opentaggedbody.md) чтобы получить помеченный текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="77eb7-115">Call the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to obtain the tagged message text.</span></span> <span data-ttu-id="77eb7-116">Этот помеченный текст заносит в систему обмена сообщениями с помощью методов из интерфейса OLE [IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="77eb7-116">This tagged text is written out to the messaging system using methods from the OLE [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface.</span></span> 
    
7. <span data-ttu-id="77eb7-117">Вызовите [метод IUnknown::Release,](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) чтобы освободить объект **ITnef.**</span><span class="sxs-lookup"><span data-stu-id="77eb7-117">Call the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method to release the **ITnef** object.</span></span> 
    
<span data-ttu-id="77eb7-118">**Обработка входящий TNEF-сообщения**</span><span class="sxs-lookup"><span data-stu-id="77eb7-118">**To process an inbound TNEF message**</span></span>
  
1. <span data-ttu-id="77eb7-119">Получите объект сообщения MAPI из пула MAPI и запишите свойства загона сообщения в новое сообщение MAPI.</span><span class="sxs-lookup"><span data-stu-id="77eb7-119">Get a MAPI message object from the MAPI spooler and write message header properties into the new MAPI message.</span></span>
    
2. <span data-ttu-id="77eb7-120">Создание и инициализация [объекта IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) для хранения данных TNEF из входящего сообщения.</span><span class="sxs-lookup"><span data-stu-id="77eb7-120">Create and initialize an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object to contain the TNEF data from the inbound message.</span></span> 
    
3. <span data-ttu-id="77eb7-121">Передав сообщение MAPI и [объект IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) [функции OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="77eb7-121">Pass the MAPI message and the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object to the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
4. <span data-ttu-id="77eb7-122">Декодирует сведения в данных TNEF, вызывая метод [ITnef::ExtractProps.](itnef-extractprops.md)</span><span class="sxs-lookup"><span data-stu-id="77eb7-122">Decode the information in the TNEF data by calling the [ITnef::ExtractProps](itnef-extractprops.md) method.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="77eb7-123">Все, что декодировали с помощью **ExtractProps,** перезаписывание свойств, декодирования из конверта входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="77eb7-123">Anything decoded by **ExtractProps** will overwrite properties decoded from the incoming message's envelope.</span></span> <span data-ttu-id="77eb7-124">То есть извлеченные свойства TNEF переопишют существующие свойства в сообщении.</span><span class="sxs-lookup"><span data-stu-id="77eb7-124">That is, extracted TNEF properties will overwrite the existing properties in a message.</span></span> 
  
5. <span data-ttu-id="77eb7-125">Обработать помеченный текст сообщения, вызывая [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) и разбор текста для восстановления позиций вложений.</span><span class="sxs-lookup"><span data-stu-id="77eb7-125">Process the tagged message text by calling [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) and parse the text to recover attachment positions.</span></span> 
    
6. <span data-ttu-id="77eb7-126">Сохраните сообщение, вызывая [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="77eb7-126">Save the message by calling [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
7. <span data-ttu-id="77eb7-127">Освободите объект TNEF, вызывая метод [IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="77eb7-127">Release the TNEF object by calling the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method.</span></span> 
    

