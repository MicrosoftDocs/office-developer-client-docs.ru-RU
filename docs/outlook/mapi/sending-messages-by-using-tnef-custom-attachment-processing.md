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
ms.openlocfilehash: f9d154b26319f5ed72b1abd6aeef307d07a63bda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339699"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a><span data-ttu-id="a30ac-103">Отправка сообщений с использованием настраиваемой обработки вложений TNEF</span><span class="sxs-lookup"><span data-stu-id="a30ac-103">Sending Messages by Using TNEF Custom Attachment Processing</span></span>

 
  
<span data-ttu-id="a30ac-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a30ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a30ac-105">Настройка обработки вложений при отправке сообщения:</span><span class="sxs-lookup"><span data-stu-id="a30ac-105">To customize attachment processing when sending a message:</span></span>
  
1. <span data-ttu-id="a30ac-106">Получите объект TNEF, передав интерфейс **IStream** и сообщение в функцию [опентнефстреамекс](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="a30ac-106">Obtain a TNEF object by passing an **IStream** interface and a message into the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
2. <span data-ttu-id="a30ac-107">Получите список всех определенных свойств сообщения, вызвав метод [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="a30ac-107">Get a list of all defined properties for the message by calling the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method.</span></span> 
    
3. <span data-ttu-id="a30ac-108">Используйте методы [IMAPIProp](imapipropiunknown.md) , чтобы исключить все свойства, поддерживаемые системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a30ac-108">Use [IMAPIProp](imapipropiunknown.md) methods to exclude all properties supported by the messaging system.</span></span> <span data-ttu-id="a30ac-109">В нужное время эти свойства записываются в систему обмена сообщениями в формате, требуемом системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a30ac-109">At an appropriate time write those properties to the messaging system in the format required by the messaging system.</span></span> 
    
4. <span data-ttu-id="a30ac-110">ВыЗовите метод [итнеф:: аддпропс](itnef-addprops.md) , чтобы добавить только свойства сообщения (то есть ни одно из свойств вложений), УСТАНОВИВ флаг тнеф_проп_мессаже_онли.</span><span class="sxs-lookup"><span data-stu-id="a30ac-110">Call the [ITnef::AddProps](itnef-addprops.md) method to add only the properties on the message — that is, none of the properties on the attachments — by setting the TNEF_PROP_MESSAGE_ONLY flag.</span></span> 
    
5. <span data-ttu-id="a30ac-111">Call [итнеф:: аддпропс](itnef-addprops.md) с этими элементами: флаг тнеф_проп_ексклуде, массив тегов свойств, который содержит **пр_аттач_дата_бин** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) или **пр_аттач_дата_обж** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) и идентификатор вложения, который указывает вложение для обработки.</span><span class="sxs-lookup"><span data-stu-id="a30ac-111">Call [ITnef::AddProps](itnef-addprops.md) with these items: the TNEF_PROP_EXCLUDE flag, a property tag array that contains the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) or **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property, and an attachment identifier that specifies the attachment to be processed.</span></span>
    
6. <span data-ttu-id="a30ac-112">Используйте метод [итнеф:: SetProps](itnef-setprops.md) , чтобы добавить тег свойства **пр_аттач_транспорт_наме** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) с уникальной строкой, которая определяет вложение в систему обмена сообщениями, если вложение содержит имя файла, система обмена сообщениями не поддерживает эту возможность.</span><span class="sxs-lookup"><span data-stu-id="a30ac-112">Use the [ITnef::SetProps](itnef-setprops.md) method to add the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property tag with a unique string that identifies the attachment to the messaging system if the attachment has a filename that the messaging system cannot support.</span></span> <span data-ttu-id="a30ac-113">Например, несколько вложений с одинаковым исходным именем или имя файла, которое не является допустимым именем для системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a30ac-113">For example, multiple attachments with the same original filename, or a filename that is not a valid filename for the messaging system.</span></span> <span data-ttu-id="a30ac-114">Эта строка будет использоваться с номером ключа при записи тегов вложений в тексте сообщения с тегами, чтобы связать вложение с его данными.</span><span class="sxs-lookup"><span data-stu-id="a30ac-114">This string will be used with a key number when writing the attachment tags in the tagged message text to associate an attachment with its data.</span></span> <span data-ttu-id="a30ac-115">Для получения дополнительных сведений см [текст сообщения с тегами в формате TNEF](tnef-tagged-message-text.md).</span><span class="sxs-lookup"><span data-stu-id="a30ac-115">For more information, see, [TNEF-Tagged Message Text](tnef-tagged-message-text.md).</span></span>
    
7. <span data-ttu-id="a30ac-116">Повторите вызовы **аддпропс** и **SetProps** для каждого вложения.</span><span class="sxs-lookup"><span data-stu-id="a30ac-116">Repeat the **AddProps** and **SetProps** calls for each attachment.</span></span> 
    
8. <span data-ttu-id="a30ac-117">ВыЗовите метод [итнеф:: Finish](itnef-finish.md) для кодирования сообщения в поток TNEF после добавления всех запрошенных свойств.</span><span class="sxs-lookup"><span data-stu-id="a30ac-117">Call the [ITnef::Finish](itnef-finish.md) method to encode the message into the TNEF stream after all the requested properties are added.</span></span> 
    
9. <span data-ttu-id="a30ac-118">Получите текст сообщения с тегами, вызвав метод [итнеф:: опентагжедбоди](itnef-opentaggedbody.md) .</span><span class="sxs-lookup"><span data-stu-id="a30ac-118">Obtain the tagged message text by calling the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method.</span></span> <span data-ttu-id="a30ac-119">Этот текст с тегами считывается с помощью методов из интерфейса **IStream** и кодируется с помощью модели вложений системы обмена сообщениями и записывается в систему обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a30ac-119">This tagged text is read using methods from the **IStream** interface, encoded using the messaging system's attachment model, and written out to the messaging system.</span></span> 
    
10. <span data-ttu-id="a30ac-120">ВыЗовите метод [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) , чтобы освободить объект [итнеф](itnefiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="a30ac-120">Call the [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to release the [ITnef](itnefiunknown.md) object.</span></span> 
    
11. <span data-ttu-id="a30ac-121">ЗаПишите оставшиеся вложения в систему обмена сообщениями через модель вложений системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a30ac-121">Write the remaining attachments to the messaging system through the messaging system's attachment model.</span></span>
    
<span data-ttu-id="a30ac-122">Поставщик транспорта должен использовать описанную выше процедуру для обработки вложений.</span><span class="sxs-lookup"><span data-stu-id="a30ac-122">Your transport provider should use the previously described procedure to process attachments.</span></span> <span data-ttu-id="a30ac-123">Если это невозможно, поставщик транспорта должен выполнить следующие действия для настроенной обработки вложений:</span><span class="sxs-lookup"><span data-stu-id="a30ac-123">If that is not possible, the transport provider should use the following steps for customized attachment processing:</span></span>
  
1. <span data-ttu-id="a30ac-124">Поставщик транспорта гарантирует, что свойства **пр_аттач_транспорт_наме** всех вложений содержат уникальные значения, которые являются допустимыми идентификаторами вложений для системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="a30ac-124">The transport provider ensures that the **PR_ATTACH_TRANSPORT_NAME** properties of all the attachments contain unique values that are valid attachment identifiers for the messaging system.</span></span> 
    
2. <span data-ttu-id="a30ac-125">Затем поставщик транспорта использует один вызов **итнеф:: аддпропс** для каждого вложения, передавая флаг тнеф_проп_контаинед.</span><span class="sxs-lookup"><span data-stu-id="a30ac-125">The transport provider then uses a single call to **ITnef::AddProps** for each attachment, passing in the TNEF_PROP_CONTAINED flag.</span></span> 
    

