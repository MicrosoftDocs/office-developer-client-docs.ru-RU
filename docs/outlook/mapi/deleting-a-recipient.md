---
title: Удаление получателя
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f7495030-e3b8-4c7c-9e19-284ba820e846
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bd01c66d9fff7c94ffb1ce9f956f1951bc482020
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421048"
---
# <a name="deleting-a-recipient"></a><span data-ttu-id="6d864-103">Удаление получателя</span><span class="sxs-lookup"><span data-stu-id="6d864-103">Deleting a Recipient</span></span>

  
  
<span data-ttu-id="6d864-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d864-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="6d864-105">**Удаление одной или нескольких записей адресной книги из изменяемого контейнера**</span><span class="sxs-lookup"><span data-stu-id="6d864-105">**To remove one or more address book entries from a modifiable container**</span></span>
  
- <span data-ttu-id="6d864-106">ВыЗовите метод [иабконтаинер::D елетинтриес](iabcontainer-deleteentries.md) , передав массив идентификаторов записей, представляющих удаляемые записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="6d864-106">Call the [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method, passing an array of entry identifiers that represent the address book entries to be deleted.</span></span> <span data-ttu-id="6d864-107">**Делетинтриес** может возвращать предупреждение, мапи_в_партиал_комплетион, чтобы показать, что не удалось удалить одну или несколько записей.</span><span class="sxs-lookup"><span data-stu-id="6d864-107">**DeleteEntries** can return a warning, MAPI_W_PARTIAL_COMPLETION, to indicate that it couldn't delete one or more of the entries.</span></span> <span data-ttu-id="6d864-108">Проверьте возвращаемое значение с помощью макроса **хр_фаилед** и вызовите метод Container [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) , если требуется больше сведений о проблеме.</span><span class="sxs-lookup"><span data-stu-id="6d864-108">Test for this return value with the **HR_FAILED** macro and call the container's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if more information about the problem is needed.</span></span> 
    
<span data-ttu-id="6d864-109">Когда вы наводите указатель на структуру [адрентри](adrentry.md) удаленного элемента в кэше, вы по-прежнему сможете получать свойства с помощью идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="6d864-109">When you hold a pointer to a deleted entry's [ADRENTRY](adrentry.md) structure in your cache, you will still be able to retrieve properties using its entry identifier.</span></span> <span data-ttu-id="6d864-110">Это вызвано тем, что запись отмечена только для удаления.</span><span class="sxs-lookup"><span data-stu-id="6d864-110">This is because the entry is only marked for deletion.</span></span> <span data-ttu-id="6d864-111">MAPI поддерживает уровень доступа к этим помеченным записям по проектированию.</span><span class="sxs-lookup"><span data-stu-id="6d864-111">MAPI maintains a level of access to these marked entries by design.</span></span> 
  

