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
ms.openlocfilehash: 1d5ae33b08c85c9ee93764d762c2ec251fddd265
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425262"
---
# <a name="removing-address-book-entries"></a><span data-ttu-id="0806e-103">Удаление записей адресной книги</span><span class="sxs-lookup"><span data-stu-id="0806e-103">Removing address book entries</span></span>
  
<span data-ttu-id="0806e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0806e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0806e-105">Для удаления одного или нескольких получателей вызывается метод [иабконтаинер::D елетинтриес](iabcontainer-deleteentries.md) .</span><span class="sxs-lookup"><span data-stu-id="0806e-105">Your container's [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) method is called to remove one or more recipients.</span></span> <span data-ttu-id="0806e-106">**Делетинтриес** имеет два параметра: массив идентификаторов записей, представляющих удаляемых получателей и зарезервированное значение флагов.</span><span class="sxs-lookup"><span data-stu-id="0806e-106">**DeleteEntries** has two parameters: an array of entry identifiers representing the recipients to be deleted and a reserved flags value.</span></span> <span data-ttu-id="0806e-107">Удаление получателя влияет на таблицу содержимого контейнера; в дополнение к удалению получателя, в контейнере должна быть удалена строка таблицы содержимого, представляющая получателя.</span><span class="sxs-lookup"><span data-stu-id="0806e-107">Deleting a recipient affects the contents table of your container; in addition to deleting the recipient, your container must delete the contents table row that represents the recipient.</span></span> <span data-ttu-id="0806e-108">Когда строка удалена из таблицы, ваш контейнер должен выдать табличное уведомление каждому зарегистрированному клиенту.</span><span class="sxs-lookup"><span data-stu-id="0806e-108">When the row has been removed from the table, your container must issue a table notification to each registered client.</span></span> 
  
### <a name="to-implement-iabcontainerdeleteentries"></a><span data-ttu-id="0806e-109">Реализация Иабконтаинер::D Елетинтриес</span><span class="sxs-lookup"><span data-stu-id="0806e-109">To implement IABContainer::DeleteEntries</span></span>
  
1. <span data-ttu-id="0806e-110">Удалите из контейнера каждого получателя, представленного идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="0806e-110">Delete each recipient represented by the entry identifier from your container.</span></span>
    
2. <span data-ttu-id="0806e-111">Если таблица содержимое контейнера открыта:</span><span class="sxs-lookup"><span data-stu-id="0806e-111">If your container's contents table is open:</span></span>
    
   - <span data-ttu-id="0806e-112">Отправьте уведомление _фневтаблемодифиед_ с набором элементов **ултабливент** в табле_ров_делетед для зарегистрированных клиентов для каждой строки удаленной таблицы содержимого.</span><span class="sxs-lookup"><span data-stu-id="0806e-112">Send an  _fnevTableModified_ notification with the **ulTableEvent** member set to TABLE_ROW_DELETED to registered clients for each deleted contents table row.</span></span> <span data-ttu-id="0806e-113">Если поставщик использует программу уведомления, вызовите [имаписуппорт:: notify](imapisupport-notify.md) для отправки этих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0806e-113">If your provider uses the notification utility, call [IMAPISupport::Notify](imapisupport-notify.md) to send these notifications.</span></span> 
    
   - <span data-ttu-id="0806e-114">Если поставщик поддерживает уведомления объектов, также отправляет уведомление _фневобжектделетед_ .</span><span class="sxs-lookup"><span data-stu-id="0806e-114">If your provider supports object notifications, also send an  _fnevObjectDeleted_ notification.</span></span> 
    

