---
title: Удаление записей адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 107ebcd7-b612-4139-b676-c3851f15bc74
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1fb7224e110bbee6844cf2820782aac8be213ba3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812110"
---
# <a name="removing-address-book-entries"></a><span data-ttu-id="3ecea-103">Удаление записей адресной книги</span><span class="sxs-lookup"><span data-stu-id="3ecea-103">Removing address book entries</span></span>
  
<span data-ttu-id="3ecea-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3ecea-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3ecea-105">Метод [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) контейнера вызывается для удаления одного или нескольких получателей.</span><span class="sxs-lookup"><span data-stu-id="3ecea-105">Your container's [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method is called to remove one or more recipients.</span></span> <span data-ttu-id="3ecea-106">**Внешнее** имеет два параметра: массив идентификаторов записи, представляющее получателей для удаления и значение зарезервировано флагов.</span><span class="sxs-lookup"><span data-stu-id="3ecea-106">**DeleteEntries** has two parameters: an array of entry identifiers representing the recipients to be deleted and a reserved flags value.</span></span> <span data-ttu-id="3ecea-107">Удаление получателя влияет на таблицу содержимого контейнера; Помимо удаления получателя, контейнера необходимо удалить строку в таблице содержимое, представляющий получателя.</span><span class="sxs-lookup"><span data-stu-id="3ecea-107">Deleting a recipient affects the contents table of your container; in addition to deleting the recipient, your container must delete the contents table row that represents the recipient.</span></span> <span data-ttu-id="3ecea-108">При удалении строку из таблицы контейнера выполнить уведомление о таблице для каждого зарегистрированных клиентов.</span><span class="sxs-lookup"><span data-stu-id="3ecea-108">When the row has been removed from the table, your container must issue a table notification to each registered client.</span></span> 
  
### <a name="to-implement-iabcontainerdeleteentries"></a><span data-ttu-id="3ecea-109">Для реализации IABContainer::DeleteEntries</span><span class="sxs-lookup"><span data-stu-id="3ecea-109">To implement IABContainer::DeleteEntries</span></span>
  
1. <span data-ttu-id="3ecea-110">Удаление каждого получателя, представленное идентификатор записи из контейнера.</span><span class="sxs-lookup"><span data-stu-id="3ecea-110">Delete each recipient represented by the entry identifier from your container.</span></span>
    
2. <span data-ttu-id="3ecea-111">Если открыта таблицу содержимого контейнера:</span><span class="sxs-lookup"><span data-stu-id="3ecea-111">If your container's contents table is open:</span></span>
    
   - <span data-ttu-id="3ecea-112">Отправьте уведомление о _fnevTableModified_ с **ulTableEvent** набор элементов для TABLE_ROW_DELETED зарегистрированным пользователям для каждой строки в таблице удаленное содержимое.</span><span class="sxs-lookup"><span data-stu-id="3ecea-112">Send an  _fnevTableModified_ notification with the **ulTableEvent** member set to TABLE_ROW_DELETED to registered clients for each deleted contents table row.</span></span> <span data-ttu-id="3ecea-113">Если ваш поставщик использует служебная программа уведомлений, вызовите [IMAPISupport::Notify](imapisupport-notify.md) для отправки этих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3ecea-113">If your provider uses the notification utility, call [IMAPISupport::Notify](imapisupport-notify.md) to send these notifications.</span></span> 
    
   - <span data-ttu-id="3ecea-114">Если ваш поставщик поддерживает объект уведомлений, отправьте уведомление о _fnevObjectDeleted_ .</span><span class="sxs-lookup"><span data-stu-id="3ecea-114">If your provider supports object notifications, also send an  _fnevObjectDeleted_ notification.</span></span> 
    

