---
title: Обработка уведомлений в таблице
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b36e4697bfd4360f4ea6ea47c70eaaae434696d8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595134"
---
# <a name="handling-table-notification"></a><span data-ttu-id="af12e-103">Обработка уведомлений в таблице</span><span class="sxs-lookup"><span data-stu-id="af12e-103">Handling table notification</span></span>

<span data-ttu-id="af12e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af12e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af12e-105">В качестве альтернативы для регистрации непосредственно с объектом источника уведомлений, например, папки или обмена мгновенными сообщениями пользователя, клиента можно зарегистрировать уведомления на содержимое или таблицы иерархии.</span><span class="sxs-lookup"><span data-stu-id="af12e-105">As an alternative to registering directly with an advise source object, such as a folder or a messaging user, a client can register for notifications on a contents or hierarchy table.</span></span> <span data-ttu-id="af12e-106">Отслеживание изменений в адресной книги, записи, папки и сообщения через содержимое или таблицы иерархии может быть проще и проще, чем через отдельные объекты.</span><span class="sxs-lookup"><span data-stu-id="af12e-106">Tracking changes to address book entries, folders, and messages through a contents or hierarchy table can be simpler and more straightforward than through individual objects.</span></span> 

<span data-ttu-id="af12e-107">Например можно вызвать [IMAPITable::Advise](imapitable-advise.md) на таблицу иерархии папок, чтобы узнать при внесении изменений в одну из ее вложенных папок.</span><span class="sxs-lookup"><span data-stu-id="af12e-107">For example, you can call [IMAPITable::Advise](imapitable-advise.md) on a folder's hierarchy table to discover when changes occur to one of its subfolders.</span></span> <span data-ttu-id="af12e-108">Если вы поддерживаете просмотра удаленных сообщений, зарегистрируйте в таблице состояния выполняли действия с поставщиками транспорта и диспетчер очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="af12e-108">If you support the viewing of remote messages, register with the status table to observe activity by transport providers and the MAPI spooler.</span></span> 
  
<span data-ttu-id="af12e-109">Тем не менее не всегда следует использовать уведомления о таблице вместо объекта уведомления.</span><span class="sxs-lookup"><span data-stu-id="af12e-109">However, it is not always preferable to use table notifications instead of object notifications.</span></span> <span data-ttu-id="af12e-110">Наблюдения за изменениями в поле число сообщений в папке приводится пример, когда клиент может потребоваться зарегистрировать объект уведомления на папку, а не в таблице, реализованный в папку.</span><span class="sxs-lookup"><span data-stu-id="af12e-110">Monitoring changes in the number of messages in a folder is an example of when your client might need to register for object notifications on a folder rather than on a table implemented by the folder.</span></span>
  

