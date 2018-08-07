---
title: Отправка сообщений с использованием настраиваемой обработки вложений TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da318b6f-128a-44b5-8357-a130022030a1
description: '���� ���������� ���������: 7 ������� 2015 �.'
ms.openlocfilehash: 1dae8d3a7830ddbc50176ec09415457ca9fdac23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812235"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="0e57c-103">Отправка сообщений с использованием настраиваемой обработки вложений TNEF</span><span class="sxs-lookup"><span data-stu-id="0e57c-103">Sending Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="0e57c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0e57c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0e57c-105">Для настройки обработки вложений при отправке сообщения:</span><span class="sxs-lookup"><span data-stu-id="0e57c-105">To customize attachment processing when sending a message:</span></span>
  
1. <span data-ttu-id="0e57c-106">Получение объекта TNEF, передав интерфейс **IStream** и сообщение в функцию [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="0e57c-106">Obtain a TNEF object by passing an **IStream** interface and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="0e57c-107">Получите список всех свойств, определенных для сообщения путем вызова метода [IMAPIProp::GetPropList](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="0e57c-107">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="0e57c-108">Используйте методы [IMAPIProp](imapipropiunknown.md) , чтобы исключить все свойства, поддерживаемые системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="0e57c-108">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="0e57c-109">Во время записи этих свойств в систему обмена сообщениями в формате, необходимые для системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="0e57c-109">At an appropriate time write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="0e57c-110">Вызовите метод [ITnef::AddProps](itnef-addprops.md) для добавления только свойства в окне сообщения — то есть, ни одно из свойств на вложения, установив для флага TNEF_PROP_MESSAGE_ONLY.</span><span class="sxs-lookup"><span data-stu-id="0e57c-110">Call the [ITnef::AddProps](itnef-addprops.md) method to add only the properties on the message — that is, none of the properties on the attachments — by setting the TNEF_PROP_MESSAGE_ONLY flag.</span></span> 
    
5. <span data-ttu-id="0e57c-111">Вызовите [ITnef::AddProps](itnef-addprops.md) с этих элементов: флаг TNEF_PROP_EXCLUDE, массив тега свойства, который содержит **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) или **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) свойство и идентификатор вложения, указывающее вложений для обработки.</span><span class="sxs-lookup"><span data-stu-id="0e57c-111">Call [ITnef::AddProps](itnef-addprops.md) with these items: the TNEF_PROP_EXCLUDE flag, a property tag array that contains the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property, and an attachment identifier that specifies the attachment to be processed.</span></span>
    
6. <span data-ttu-id="0e57c-112">Метод [ITnef::SetProps](itnef-setprops.md) используется для добавления тега свойства **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) с уникальная строка, которая идентифицирует вложения в системе обмена сообщениями, если вложение содержит имя файла, который не поддерживает системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="0e57c-112">Use the [ITnef::SetProps](itnef-setprops.md) method to add the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property tag with a unique string that identifies the attachment to the messaging system if the attachment has a filename that the messaging system cannot support.</span></span> <span data-ttu-id="0e57c-113">Например несколько вложений с тем же именем исходного файла или имени файла, который не является допустимым именем файла для системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="0e57c-113">For example, multiple attachments with the same original filename, or a filename that is not a valid filename for the messaging system.</span></span> <span data-ttu-id="0e57c-114">Эта строка будет использоваться с номер ключа при записи теги вложений в текст с тегами сообщения для связи с данными вложения.</span><span class="sxs-lookup"><span data-stu-id="0e57c-114">This string will be used with a key number when writing the attachment tags in the tagged message text to associate an attachment with its data.</span></span> <span data-ttu-id="0e57c-115">Дополнительные сведения см., [TNEF-Tagged текста сообщения](tnef-tagged-message-text.md).</span><span class="sxs-lookup"><span data-stu-id="0e57c-115">For more information, see, [TNEF-Tagged Message Text](tnef-tagged-message-text.md).</span></span>
    
7. <span data-ttu-id="0e57c-116">Повторите **AddProps** и **SetProps** звонков для каждого вложения.</span><span class="sxs-lookup"><span data-stu-id="0e57c-116">Repeat the **AddProps** and **SetProps** calls for each attachment.</span></span> 
    
8. <span data-ttu-id="0e57c-117">Вызовите метод [ITnef::Finish](itnef-finish.md) для кодирования сообщений в поток TNEF после добавления все запрошенные свойства.</span><span class="sxs-lookup"><span data-stu-id="0e57c-117">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
9. <span data-ttu-id="0e57c-118">Получает текст с тегами сообщения путем вызова метода [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) .</span><span class="sxs-lookup"><span data-stu-id="0e57c-118">Obtain the tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="0e57c-119">Этот текст с тегами считываются с помощью методов из интерфейса **IStream** , кодируются с помощью модели вложения системе обмена сообщениями и записывается в системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="0e57c-119">This tagged text is read using methods from the **IStream** interface, encoded using the messaging system's attachment model, and written out to the messaging system.</span></span> 
    
10. <span data-ttu-id="0e57c-120">Вызовите метод [функции IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) для освобождения объекта [ITnef](itnefiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="0e57c-120">Call the [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to release the [ITnef](itnefiunknown.md) object.</span></span> 
    
11. <span data-ttu-id="0e57c-121">Написание оставшихся вложения в системе обмена сообщениями через модель вложения системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="0e57c-121">Write the remaining attachments to the messaging system through the messaging system's attachment model.</span></span>
    
<span data-ttu-id="0e57c-122">Поставщика транспорта следует использовать уже было сказано процедуру, чтобы процесс вложения.</span><span class="sxs-lookup"><span data-stu-id="0e57c-122">Your transport provider should use the previously described procedure to process attachments.</span></span> <span data-ttu-id="0e57c-123">Если это невозможно, поставщика транспорта следует использовать следующие шаги для обработки настраиваемых вложений:</span><span class="sxs-lookup"><span data-stu-id="0e57c-123">If that is not possible, the transport provider should use the following steps for customized attachment processing:</span></span>
  
1. <span data-ttu-id="0e57c-124">Поставщика транспорта гарантирует, что свойства **PR_ATTACH_TRANSPORT_NAME** всех вложений содержит уникальные значения, которые являются идентификаторы допустимого вложения для системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="0e57c-124">The transport provider ensures that the **PR_ATTACH_TRANSPORT_NAME** properties of all the attachments contain unique values that are valid attachment identifiers for the messaging system.</span></span> 
    
2. <span data-ttu-id="0e57c-125">Поставщика транспорта затем использует один вызов **ITnef::AddProps** для каждого вложения, передав в флаг TNEF_PROP_CONTAINED.</span><span class="sxs-lookup"><span data-stu-id="0e57c-125">The transport provider then uses a single call to **ITnef::AddProps** for each attachment, passing in the TNEF_PROP_CONTAINED flag.</span></span> 
    

