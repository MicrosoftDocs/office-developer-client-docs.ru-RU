---
title: Отправка сообщений с помощью настраиваемой обработки вложений в TNEF
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da318b6f-128a-44b5-8357-a130022030a1
description: '���� ���������� ���������: 7 ������� 2015 �.'
ms.openlocfilehash: f9d154b26319f5ed72b1abd6aeef307d07a63bda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339699"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="a88f5-103">Отправка сообщений с помощью настраиваемой обработки вложений в TNEF</span><span class="sxs-lookup"><span data-stu-id="a88f5-103">Sending Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="a88f5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a88f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a88f5-105">Настройка обработки вложений при отправке сообщения:</span><span class="sxs-lookup"><span data-stu-id="a88f5-105">To customize attachment processing when sending a message:</span></span>
  
1. <span data-ttu-id="a88f5-106">Получите объект TNEF, передав **интерфейс IStream** и сообщение в [функцию OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="a88f5-106">Obtain a TNEF object by passing an **IStream** interface and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="a88f5-107">Получите список всех определенных свойств сообщения, вызывая метод [IMAPIProp::GetPropList.](imapiprop-getproplist.md)</span><span class="sxs-lookup"><span data-stu-id="a88f5-107">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="a88f5-108">Используйте [методы IMAPIProp,](imapipropiunknown.md) чтобы исключить все свойства, поддерживаемые системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a88f5-108">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="a88f5-109">В соответствующее время запишите эти свойства в систему обмена сообщениями в формате, требуемом системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a88f5-109">At an appropriate time write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="a88f5-110">Вызовите метод [ITnef::AddProps,](itnef-addprops.md) чтобы добавить только свойства сообщения ( то есть ни одно из свойств вложений), установив флаг TNEF_PROP_MESSAGE_ONLY.</span><span class="sxs-lookup"><span data-stu-id="a88f5-110">Call the [ITnef::AddProps](itnef-addprops.md) method to add only the properties on the message — that is, none of the properties on the attachments — by setting the TNEF_PROP_MESSAGE_ONLY flag.</span></span> 
    
5. <span data-ttu-id="a88f5-111">Вызовите [ITnef::AddProps](itnef-addprops.md) с помощью этих элементов: флаг TNEF_PROP_EXCLUDE, массив тегов свойств, содержащий **свойство PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary)](pidtagattachdatabinary-canonical-property.md)или **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject),](pidtagattachdataobject-canonical-property.md)а также идентификатор вложения, который указывает вложение для обработки.</span><span class="sxs-lookup"><span data-stu-id="a88f5-111">Call [ITnef::AddProps](itnef-addprops.md) with these items: the TNEF_PROP_EXCLUDE flag, a property tag array that contains the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property, and an attachment identifier that specifies the attachment to be processed.</span></span>
    
6. <span data-ttu-id="a88f5-112">Используйте метод [ITnef::SetProps,](itnef-setprops.md) чтобы добавить тег свойства **PR_ATTACH_TRANSPORT_NAME** [(PidTagAttachTransportName)](pidtagattachtransportname-canonical-property.md)с уникальной строкой, идентифицирующий вложение в системе обмена сообщениями, если вложение имеет имя файла, которое система обмена сообщениями не может поддерживать.</span><span class="sxs-lookup"><span data-stu-id="a88f5-112">Use the [ITnef::SetProps](itnef-setprops.md) method to add the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property tag with a unique string that identifies the attachment to the messaging system if the attachment has a filename that the messaging system cannot support.</span></span> <span data-ttu-id="a88f5-113">Например, несколько вложений с одним и тем же исходным именом файла или имя файла, которое не является допустимым и имям файла для системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a88f5-113">For example, multiple attachments with the same original filename, or a filename that is not a valid filename for the messaging system.</span></span> <span data-ttu-id="a88f5-114">Эта строка будет использоваться с номером ключа при написании тегов вложений в тексте помеченного сообщения, чтобы связать вложение с его данными.</span><span class="sxs-lookup"><span data-stu-id="a88f5-114">This string will be used with a key number when writing the attachment tags in the tagged message text to associate an attachment with its data.</span></span> <span data-ttu-id="a88f5-115">Дополнительные сведения см. в тексте сообщения с тегом [TNEF.](tnef-tagged-message-text.md)</span><span class="sxs-lookup"><span data-stu-id="a88f5-115">For more information, see, [TNEF-Tagged Message Text](tnef-tagged-message-text.md).</span></span>
    
7. <span data-ttu-id="a88f5-116">Повторите **вызовы AddProps** и **SetProps** для каждого вложения.</span><span class="sxs-lookup"><span data-stu-id="a88f5-116">Repeat the **AddProps** and **SetProps** calls for each attachment.</span></span> 
    
8. <span data-ttu-id="a88f5-117">Вызовите [метод ITnef::Finish,](itnef-finish.md) чтобы закодировать сообщение в поток TNEF после того, как будут добавлены все запрашиваемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a88f5-117">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
9. <span data-ttu-id="a88f5-118">Получите помеченный текст сообщения, вызывая метод [ITnef::OpenTaggedBody.](itnef-opentaggedbody.md)</span><span class="sxs-lookup"><span data-stu-id="a88f5-118">Obtain the tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="a88f5-119">Этот помеченный текст считывания с помощью методов из интерфейса **IStream,** закодирован с помощью модели вложений системы обмена сообщениями и записан в систему обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a88f5-119">This tagged text is read using methods from the **IStream** interface, encoded using the messaging system's attachment model, and written out to the messaging system.</span></span> 
    
10. <span data-ttu-id="a88f5-120">Вызовите [метод IUnknown::Release,](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) чтобы освободить объект [ITnef.](itnefiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="a88f5-120">Call the [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to release the [ITnef](itnefiunknown.md) object.</span></span> 
    
11. <span data-ttu-id="a88f5-121">Запишите оставшиеся вложения в систему обмена сообщениями с помощью модели вложений системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a88f5-121">Write the remaining attachments to the messaging system through the messaging system's attachment model.</span></span>
    
<span data-ttu-id="a88f5-122">Поставщик транспорта должен использовать описанную выше процедуру для обработки вложений.</span><span class="sxs-lookup"><span data-stu-id="a88f5-122">Your transport provider should use the previously described procedure to process attachments.</span></span> <span data-ttu-id="a88f5-123">Если это невозможно, поставщик транспорта должен использовать следующие действия для обработки настраиваемых вложений:</span><span class="sxs-lookup"><span data-stu-id="a88f5-123">If that is not possible, the transport provider should use the following steps for customized attachment processing:</span></span>
  
1. <span data-ttu-id="a88f5-124">Поставщик транспорта гарантирует,  что PR_ATTACH_TRANSPORT_NAME всех вложений содержат уникальные значения, которые являются допустимым идентификатором вложений для системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a88f5-124">The transport provider ensures that the **PR_ATTACH_TRANSPORT_NAME** properties of all the attachments contain unique values that are valid attachment identifiers for the messaging system.</span></span> 
    
2. <span data-ttu-id="a88f5-125">Затем поставщик транспорта использует один вызов **ITnef::AddProps** для каждого вложения, передав TNEF_PROP_CONTAINED флаг.</span><span class="sxs-lookup"><span data-stu-id="a88f5-125">The transport provider then uses a single call to **ITnef::AddProps** for each attachment, passing in the TNEF_PROP_CONTAINED flag.</span></span> 
    

