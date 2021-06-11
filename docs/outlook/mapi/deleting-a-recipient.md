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
# <a name="deleting-a-recipient"></a><span data-ttu-id="06d0c-103">Удаление получателя</span><span class="sxs-lookup"><span data-stu-id="06d0c-103">Deleting a Recipient</span></span>

  
  
<span data-ttu-id="06d0c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06d0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="06d0c-105">**Удаление одной или более записей адресной книги из изменяемого контейнера**</span><span class="sxs-lookup"><span data-stu-id="06d0c-105">**To remove one or more address book entries from a modifiable container**</span></span>
  
- <span data-ttu-id="06d0c-106">Вызовите [метод IABContainer::D eleteEntries, передав](iabcontainer-deleteentries.md) массив идентификаторов записей, которые представляют удаленные записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="06d0c-106">Call the [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method, passing an array of entry identifiers that represent the address book entries to be deleted.</span></span> <span data-ttu-id="06d0c-107">**DeleteEntries** может вернуть предупреждение, MAPI_W_PARTIAL_COMPLETION, чтобы указать, что он не может удалить одну или несколько записей.</span><span class="sxs-lookup"><span data-stu-id="06d0c-107">**DeleteEntries** can return a warning, MAPI_W_PARTIAL_COMPLETION, to indicate that it couldn't delete one or more of the entries.</span></span> <span data-ttu-id="06d0c-108">Проверьте это возвращаемого значения с помощью **макроса HR_FAILED** и позвоните по методу [IMAPIProp::GetLastError,](imapiprop-getlasterror.md) если требуется дополнительные сведения о проблеме.</span><span class="sxs-lookup"><span data-stu-id="06d0c-108">Test for this return value with the **HR_FAILED** macro and call the container's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if more information about the problem is needed.</span></span> 
    
<span data-ttu-id="06d0c-109">При удержании указателя к структуре [ADRENTRY](adrentry.md) удаленной записи в кэше вы все равно сможете получить свойства с помощью идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="06d0c-109">When you hold a pointer to a deleted entry's [ADRENTRY](adrentry.md) structure in your cache, you will still be able to retrieve properties using its entry identifier.</span></span> <span data-ttu-id="06d0c-110">Это потому, что запись помечена только для удаления.</span><span class="sxs-lookup"><span data-stu-id="06d0c-110">This is because the entry is only marked for deletion.</span></span> <span data-ttu-id="06d0c-111">MAPI поддерживает уровень доступа к этим отмеченным записям по дизайну.</span><span class="sxs-lookup"><span data-stu-id="06d0c-111">MAPI maintains a level of access to these marked entries by design.</span></span> 
  

