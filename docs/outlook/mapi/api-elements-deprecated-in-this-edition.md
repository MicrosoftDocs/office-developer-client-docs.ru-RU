---
title: Элементы API, устаревшие в этом выпуске
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: abfe734ad8af436f52fc0308d0cd236078bb47df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436890"
---
# <a name="api-elements-deprecated-in-this-edition"></a><span data-ttu-id="e484c-103">Элементы API, устаревшие в этом выпуске</span><span class="sxs-lookup"><span data-stu-id="e484c-103">API Elements Deprecated in This Edition</span></span>

  
  
<span data-ttu-id="e484c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e484c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e484c-105">Следующие элементы API являются устаревшими в Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="e484c-105">The following API elements are deprecated in Microsoft Outlook 2013.</span></span> <span data-ttu-id="e484c-106">Они больше не поддерживаются, и их не следует использовать в новых проектах.</span><span class="sxs-lookup"><span data-stu-id="e484c-106">They are no longer supported and you should not use them in new projects.</span></span>
  
## <a name="deprecation-of-message-and-recipient-options"></a><span data-ttu-id="e484c-107">Устаревшие параметры сообщений и получателей</span><span class="sxs-lookup"><span data-stu-id="e484c-107">Deprecation of Message and Recipient Options</span></span>

<span data-ttu-id="e484c-108">Следующие элементы API являются устаревшими в этом выпуске из-за устаревших параметров сообщений и получателей:</span><span class="sxs-lookup"><span data-stu-id="e484c-108">The following API elements are deprecated in this release because of obsolete message and recipient options:</span></span>
  
- <span data-ttu-id="e484c-109">**Иксплогон:: регистероптионс**— подсистема MAPI больше не вызывает этот метод, чтобы задать значения по умолчанию для параметров Message и Recipient для поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="e484c-109">**IXPLogon::RegisterOptions**—The MAPI subsystem no longer calls this method to establish any default values for message and recipient options for a transport provider.</span></span>
    
- <span data-ttu-id="e484c-110">**Оптиондата**— эта структура данных, в которой поддерживаются свойства для параметров сообщений и получателей, устарела.</span><span class="sxs-lookup"><span data-stu-id="e484c-110">**OPTIONDATA**—This data structure that supported properties for message and recipient options is obsolete.</span></span> <span data-ttu-id="e484c-111">Подсистема MAPI больше не вызывает **иксплогон:: регистероптионс** для получения всех параметров сообщений или получателей, поддерживаемых поставщиком транспорта для определенного типа адреса.</span><span class="sxs-lookup"><span data-stu-id="e484c-111">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** to obtain any message or recipient options that a transport provider supports for a particular address type.</span></span> 
    
- <span data-ttu-id="e484c-112">**Оптионкаллбакк**— этот прототип функции, используемый поставщиком транспорта для объявления функции обратного вызова и который, в свою очередь, является устаревшим подсистемой MAPI, используемой для разрешения свойств поставщика.</span><span class="sxs-lookup"><span data-stu-id="e484c-112">**OPTIONCALLBACK**—This function prototype, which a transport provider used to declare a callback function and which, in turn, the MAPI subsystem used to resolve the provider's properties, is obsolete.</span></span> <span data-ttu-id="e484c-113">Подсистема MAPI больше не вызывает **иксплогон:: регистероптионс** или использует любую функцию обратного вызова, возвращенную поставщиком транспорта.</span><span class="sxs-lookup"><span data-stu-id="e484c-113">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** or uses any callback function returned by the transport provider.</span></span> 
    
- <span data-ttu-id="e484c-114">**IMAPISession:: мессажеоптионс**— клиент MAPI and Service Providers больше не должны вызывать этот метод для отображения свойств или позволить пользователям задавать свойства, управляющие конкретным сообщением и типом адреса.</span><span class="sxs-lookup"><span data-stu-id="e484c-114">**IMAPISession::MessageOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control a particular message and address type.</span></span> <span data-ttu-id="e484c-115">Метод всегда возвращает MAPI_E_NOT_FOUND, что указывает на то, что для конкретного сообщения нет параметров.</span><span class="sxs-lookup"><span data-stu-id="e484c-115">The method always returns MAPI_E_NOT_FOUND, which indicates that there are no message options for the particular message.</span></span>
    
- <span data-ttu-id="e484c-116">**IMAPISession:: куеридефаултмессажеопт**— клиент MAPI и поставщики услуг не должны больше вызывать этот метод для получения свойств, управляющих параметрами сообщений для определенного типа адреса.</span><span class="sxs-lookup"><span data-stu-id="e484c-116">**IMAPISession::QueryDefaultMessageOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control message options for a particular address type.</span></span> <span data-ttu-id="e484c-117">Метод больше не возвращает указатель на любой массив значений свойств.</span><span class="sxs-lookup"><span data-stu-id="e484c-117">The method no longer returns a pointer to any array of property values.</span></span>
    
- <span data-ttu-id="e484c-118">**IAddrBook:: реЦипоптионс**— клиент MAPI and Service Providers больше не должны вызывать этот метод для отображения свойств или позволить пользователям задавать свойства, управляющие обработкой для получателя определенного типа адреса.</span><span class="sxs-lookup"><span data-stu-id="e484c-118">**IAddrBook::RecipOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control processing for a recipient of a particular address type.</span></span> <span data-ttu-id="e484c-119">Метод всегда возвращает MAPI_W_ERRORS_RETURNED, что указывает на то, что для конкретного получателя не заданы параметры получателя.</span><span class="sxs-lookup"><span data-stu-id="e484c-119">The method always returns MAPI_W_ERRORS_RETURNED, which indicates that there are no recipient options for the particular recipient.</span></span>
    
- <span data-ttu-id="e484c-120">**IAddrBook:: куеридефаултреЦипопт**— клиент MAPI и поставщики услуг не должны больше вызывать этот метод для получения свойств, контролирующих параметры получателей для определенного типа адреса.</span><span class="sxs-lookup"><span data-stu-id="e484c-120">**IAddrBook::QueryDefaultRecipOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control recipient options for a particular address type.</span></span> <span data-ttu-id="e484c-121">Метод больше не возвращает указатель на любой массив значений свойств.</span><span class="sxs-lookup"><span data-stu-id="e484c-121">The method no longer returns a pointer to any array of property values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e484c-122">См. также</span><span class="sxs-lookup"><span data-stu-id="e484c-122">See also</span></span>



[<span data-ttu-id="e484c-123">Начало работы со справочником по MAPI для Outlook</span><span class="sxs-lookup"><span data-stu-id="e484c-123">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)

