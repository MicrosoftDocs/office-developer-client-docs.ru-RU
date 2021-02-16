---
title: Получение свойств получателя
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 358f892b-54a7-4213-b3c0-94f28f99716f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 38063cebe70b153decce6713ac5fc31d6916dbf6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426676"
---
# <a name="retrieving-recipient-properties"></a><span data-ttu-id="3a698-103">Получение свойств получателя</span><span class="sxs-lookup"><span data-stu-id="3a698-103">Retrieving recipient properties</span></span>
  
<span data-ttu-id="3a698-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a698-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
### <a name="to-access-one-or-more-properties-of-an-address-book-entry"></a><span data-ttu-id="3a698-105">Доступ к одному или более свойствам записи адресной книги</span><span class="sxs-lookup"><span data-stu-id="3a698-105">To access one or more properties of an address book entry</span></span>
  
1. <span data-ttu-id="3a698-106">Для каждой интересующих вас записей адресной книги вызовите [IAddrBook::OpenEntry,](iaddrbook-openentry.md)передав идентификатор записи целевого пользователя обмена сообщениями или списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="3a698-106">For each address book entry of interest, call [IAddrBook::OpenEntry](iaddrbook-openentry.md), passing the entry identifier of the target messaging user or distribution list.</span></span>
    
2. <span data-ttu-id="3a698-107">Затем сделайте одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="3a698-107">Then do one of the following:</span></span>
    
   - <span data-ttu-id="3a698-108">Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) пользователя или списка рассылки для каждой интересующих вас адресных книг со списком свойств, которые необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="3a698-108">Call the messaging user or distribution list's [IMAPIProp::GetProps](imapiprop-getprops.md) method for each address book entry of interest, with a list of the one or more properties to retrieve.</span></span> 
    
   - <span data-ttu-id="3a698-109">Вызовите [IAddrBook::P repareRecips, передав](iaddrbook-preparerecips.md)структуру [ADRLIST,](adrlist.md) которая содержит все свойства для всех нужных записей адресной книги.</span><span class="sxs-lookup"><span data-stu-id="3a698-109">Call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md), passing an [ADRLIST](adrlist.md) structure that holds all of the properties for all of the desired address book entries.</span></span> <span data-ttu-id="3a698-110">Так как один вызов **PrepareRecips** может возвращать сведения о нескольких записях адресной книги, это предпочтительный вариант, если вас интересует несколько получателей.</span><span class="sxs-lookup"><span data-stu-id="3a698-110">Because one call to **PrepareRecips** can return information for multiple address book entries, it is the preferable strategy when you are interested in more than one recipient.</span></span> 
    

