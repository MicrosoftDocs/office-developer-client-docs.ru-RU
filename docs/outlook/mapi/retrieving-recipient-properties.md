---
title: Извлечение свойств получателя
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a7bdcf133b8b2b5d8eb906cc0f5b5803838e27a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812139"
---
# <a name="retrieving-recipient-properties"></a><span data-ttu-id="0b6ff-103">Извлечение свойств получателя</span><span class="sxs-lookup"><span data-stu-id="0b6ff-103">Retrieving recipient properties</span></span>
  
<span data-ttu-id="0b6ff-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0b6ff-104">**Applies to**: Outlook</span></span> 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a><span data-ttu-id="0b6ff-105">Для доступа к одного или нескольких свойств записи адресной книги</span><span class="sxs-lookup"><span data-stu-id="0b6ff-105">To access one or more properties of an address book entry</span></span>
  
1. <span data-ttu-id="0b6ff-106">Для каждой записи адресной книги интересов вызовите [IAddrBook::OpenEntry](iaddrbook-openentry.md), передав идентификатор записи конечного пользователя или список рассылки системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="0b6ff-106">For each address book entry of interest, call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing the entry identifier of the target messaging user or distribution list.</span></span>
    
2. <span data-ttu-id="0b6ff-107">Затем выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="0b6ff-107">Then do one of the following:</span></span>
    
   - <span data-ttu-id="0b6ff-108">Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) списка рассылки или обмена мгновенными сообщениями пользователя для каждой записи адресной книги интересов, со списком одно или несколько свойств для извлечения.</span><span class="sxs-lookup"><span data-stu-id="0b6ff-108">Call the messaging user or distribution list's [IMAPIProp::GetProps](imapiprop-getprops.md) method for each address book entry of interest, with a list of the one or more properties to retrieve.</span></span> 
    
   - <span data-ttu-id="0b6ff-109">Вызовите [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), передав структуру [ADRLIST](adrlist.md) , в котором содержатся все свойства для всех записей желаемую адресной книги.</span><span class="sxs-lookup"><span data-stu-id="0b6ff-109">Call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), passing an [ADRLIST](adrlist.md) structure that holds all of the properties for all of the desired address book entries.</span></span> <span data-ttu-id="0b6ff-110">Так как один вызов **PrepareRecips** можно получить сведения о нескольких адрес записей книги, это предпочтительными стратегии, когда вы заинтересованы в нескольких получателей.</span><span class="sxs-lookup"><span data-stu-id="0b6ff-110">Because one call to **PrepareRecips** can return information for multiple address book entries, it is the preferable strategy when you are interested in more than one recipient.</span></span> 
    

