---
title: Элементы API, объявленные устаревшими в этом выпуске
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: 'Дата последнего изменения: 25 июня 2012 года'
ms.openlocfilehash: e40bcbfffc6f149837f4a11351f2bdbbf0dcc524
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571600"
---
# <a name="api-elements-deprecated-in-this-edition"></a><span data-ttu-id="b42cf-103">Элементы API, объявленные устаревшими в этом выпуске</span><span class="sxs-lookup"><span data-stu-id="b42cf-103">API Elements Deprecated in This Edition</span></span>

  
  
<span data-ttu-id="b42cf-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b42cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b42cf-105">Следующие элементы API поддерживаются в Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="b42cf-105">The following API elements are deprecated in Microsoft Outlook 2013.</span></span> <span data-ttu-id="b42cf-106">Больше не поддерживаются и их не следует использовать в новых проектах.</span><span class="sxs-lookup"><span data-stu-id="b42cf-106">They are no longer supported and you should not use them in new projects.</span></span>
  
## <a name="deprecation-of-message-and-recipient-options"></a><span data-ttu-id="b42cf-107">Об использовании параметров получателей и сообщений</span><span class="sxs-lookup"><span data-stu-id="b42cf-107">Deprecation of Message and Recipient Options</span></span>

<span data-ttu-id="b42cf-108">Следующие элементы API поддерживаются в этой версии из-за устаревших сообщений и получателей параметры:</span><span class="sxs-lookup"><span data-stu-id="b42cf-108">The following API elements are deprecated in this release because of obsolete message and recipient options:</span></span>
  
- <span data-ttu-id="b42cf-109">**IXPLogon::RegisterOptions**— подсистемы MAPI больше не вызывает этот метод, чтобы установить все значения по умолчанию для доступа к параметрам сообщений и получателей для поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="b42cf-109">**IXPLogon::RegisterOptions**—The MAPI subsystem no longer calls this method to establish any default values for message and recipient options for a transport provider.</span></span>
    
- <span data-ttu-id="b42cf-110">**OPTIONDATA**— эта структура данных, поддерживаемые свойства для доступа к параметрам сообщение и получатель является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="b42cf-110">**OPTIONDATA**—This data structure that supported properties for message and recipient options is obsolete.</span></span> <span data-ttu-id="b42cf-111">Подсистема MAPI больше не вызывает **IXPLogon::RegisterOptions** для получения любое сообщение или получателей параметры, поставщика транспорта для типа определенного адреса.</span><span class="sxs-lookup"><span data-stu-id="b42cf-111">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** to obtain any message or recipient options that a transport provider supports for a particular address type.</span></span> 
    
- <span data-ttu-id="b42cf-112">**OPTIONCALLBACK**— в этом прототипа функции, которая транспорта поставщика используется для объявления функции обратного вызова и который, в свою очередь, подсистемы MAPI, используемой для разрешения свойства поставщика является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="b42cf-112">**OPTIONCALLBACK**—This function prototype, which a transport provider used to declare a callback function and which, in turn, the MAPI subsystem used to resolve the provider's properties, is obsolete.</span></span> <span data-ttu-id="b42cf-113">Подсистема MAPI больше не вызывает **IXPLogon::RegisterOptions** или любой функция обратного вызова, возвращаемые поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="b42cf-113">The MAPI subsystem no longer calls **IXPLogon::RegisterOptions** or uses any callback function returned by the transport provider.</span></span> 
    
- <span data-ttu-id="b42cf-114">**IMAPISession::MessageOptions**— клиент и служба поставщики MAPI больше не должны вызывать этот метод для отображения свойств или пользователи могут задавать свойства, управляющие определенного типа сообщения и адрес.</span><span class="sxs-lookup"><span data-stu-id="b42cf-114">**IMAPISession::MessageOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control a particular message and address type.</span></span> <span data-ttu-id="b42cf-115">Метод всегда возвращает MAPI_E_NOT_FOUND, это означает, что нет способа сообщения для определенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="b42cf-115">The method always returns MAPI_E_NOT_FOUND, which indicates that there are no message options for the particular message.</span></span>
    
- <span data-ttu-id="b42cf-116">**IMAPISession::QueryDefaultMessageOpt**— клиент и служба поставщики MAPI больше не должны вызывать этот метод для извлечения свойств, определяющих параметры сообщения для определенного адреса типа.</span><span class="sxs-lookup"><span data-stu-id="b42cf-116">**IMAPISession::QueryDefaultMessageOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control message options for a particular address type.</span></span> <span data-ttu-id="b42cf-117">Метод больше не возвращает указатель на какой-либо массив значений свойств.</span><span class="sxs-lookup"><span data-stu-id="b42cf-117">The method no longer returns a pointer to any array of property values.</span></span>
    
- <span data-ttu-id="b42cf-118">**IAddrBook::RecipOptions**— клиент и служба поставщики MAPI больше не должны вызывать этот метод для отображения свойств или пользователи могут задавать свойства этого элемента управления обработки для получателя, адрес определенного типа.</span><span class="sxs-lookup"><span data-stu-id="b42cf-118">**IAddrBook::RecipOptions**—MAPI client and service providers should no longer call this method to display properties or let users set properties that control processing for a recipient of a particular address type.</span></span> <span data-ttu-id="b42cf-119">Метод всегда возвращает MAPI_W_ERRORS_RETURNED, это означает, что нет способа получателей для определенного получателя.</span><span class="sxs-lookup"><span data-stu-id="b42cf-119">The method always returns MAPI_W_ERRORS_RETURNED, which indicates that there are no recipient options for the particular recipient.</span></span>
    
- <span data-ttu-id="b42cf-120">**IAddrBook::QueryDefaultRecipOpt**— клиент и служба поставщики MAPI больше не должны вызывать этот метод для извлечения свойств, которые управляют получателей параметры для типа определенного адреса.</span><span class="sxs-lookup"><span data-stu-id="b42cf-120">**IAddrBook::QueryDefaultRecipOpt**—MAPI client and service providers should no longer call this method to retrieve properties that control recipient options for a particular address type.</span></span> <span data-ttu-id="b42cf-121">Метод больше не возвращает указатель на какой-либо массив значений свойств.</span><span class="sxs-lookup"><span data-stu-id="b42cf-121">The method no longer returns a pointer to any array of property values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b42cf-122">См. также</span><span class="sxs-lookup"><span data-stu-id="b42cf-122">See also</span></span>



[<span data-ttu-id="b42cf-123">Начало работы со справочником по MAPI для Outlook</span><span class="sxs-lookup"><span data-stu-id="b42cf-123">Getting Started with the Outlook MAPI Reference</span></span>](getting-started-with-the-outlook-mapi-reference.md)

