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
ms.openlocfilehash: 9a3006b43eb9f210603ff3a3d890118e7fd61d7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808268"
---
# <a name="deleting-a-recipient"></a><span data-ttu-id="8e02b-103">Удаление получателя</span><span class="sxs-lookup"><span data-stu-id="8e02b-103">Deleting a Recipient</span></span>

  
  
<span data-ttu-id="8e02b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8e02b-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="8e02b-105">**Чтобы удалить одного или нескольких записей адресной книги из изменяемые контейнера**</span><span class="sxs-lookup"><span data-stu-id="8e02b-105">**To remove one or more address book entries from a modifiable container**</span></span>
  
- <span data-ttu-id="8e02b-106">Вызовите метод [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) , передав массив идентификаторов записи, которые представляют адресной книги к удалению.</span><span class="sxs-lookup"><span data-stu-id="8e02b-106">Call the [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method, passing an array of entry identifiers that represent the address book entries to be deleted.</span></span> <span data-ttu-id="8e02b-107">**Внешнее** может вернуть предупреждение MAPI_W_PARTIAL_COMPLETION, чтобы указать, что она не удается удалить одну или несколько записей.</span><span class="sxs-lookup"><span data-stu-id="8e02b-107">**DeleteEntries** can return a warning, MAPI_W_PARTIAL_COMPLETION, to indicate that it couldn't delete one or more of the entries.</span></span> <span data-ttu-id="8e02b-108">Тестирование этого возвращаемого значения с помощью макроса **HR_FAILED** и вызовите метод [IMAPIProp::GetLastError](imapiprop-getlasterror.md) контейнера, если требуется дополнительная информация о проблеме.</span><span class="sxs-lookup"><span data-stu-id="8e02b-108">Test for this return value with the **HR_FAILED** macro and call the container's [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if more information about the problem is needed.</span></span> 
    
<span data-ttu-id="8e02b-109">Если навести указатель структуру [ADRENTRY](adrentry.md) удаленные записи в кэше по-прежнему можно для извлечения свойств с помощью его идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="8e02b-109">When you hold a pointer to a deleted entry's [ADRENTRY](adrentry.md) structure in your cache, you will still be able to retrieve properties using its entry identifier.</span></span> <span data-ttu-id="8e02b-110">Это, так как операция только помеченным для удаления.</span><span class="sxs-lookup"><span data-stu-id="8e02b-110">This is because the entry is only marked for deletion.</span></span> <span data-ttu-id="8e02b-111">Уровень доступа к эти помеченные записи поддерживает MAPI, разработки.</span><span class="sxs-lookup"><span data-stu-id="8e02b-111">MAPI maintains a level of access to these marked entries by design.</span></span> 
  

