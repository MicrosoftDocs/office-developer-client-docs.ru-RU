---
title: Обработка уведомления о таблице
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6e6c24c3836f295054c1880dc506c5051078a9ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435896"
---
# <a name="handling-table-notification"></a><span data-ttu-id="89ddc-103">Обработка уведомления о таблице</span><span class="sxs-lookup"><span data-stu-id="89ddc-103">Handling table notification</span></span>

<span data-ttu-id="89ddc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89ddc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89ddc-105">В качестве альтернативы регистрации непосредственно с помощью объекта источника консультации, например папки или пользователя обмена сообщениями, клиент может зарегистрироваться для уведомлений в содержимом или таблице иерархии.</span><span class="sxs-lookup"><span data-stu-id="89ddc-105">As an alternative to registering directly with an advise source object, such as a folder or a messaging user, a client can register for notifications on a contents or hierarchy table.</span></span> <span data-ttu-id="89ddc-106">Отслеживание изменений записей, папок и сообщений адресной книги с помощью содержимого или таблицы иерархии может быть проще и проще, чем с помощью отдельных объектов.</span><span class="sxs-lookup"><span data-stu-id="89ddc-106">Tracking changes to address book entries, folders, and messages through a contents or hierarchy table can be simpler and more straightforward than through individual objects.</span></span> 

<span data-ttu-id="89ddc-107">Например, можно вызвать [IMAPITable::Advise](imapitable-advise.md) в таблице иерархии папки, чтобы узнать, когда происходят изменения в одной из ее вложенных папок.</span><span class="sxs-lookup"><span data-stu-id="89ddc-107">For example, you can call [IMAPITable::Advise](imapitable-advise.md) on a folder's hierarchy table to discover when changes occur to one of its subfolders.</span></span> <span data-ttu-id="89ddc-108">Если вы поддерживаете просмотр удаленных сообщений, зарегистрируйтесь в таблице состояния, чтобы наблюдать за действиями поставщиков транспорта и пула MAPI.</span><span class="sxs-lookup"><span data-stu-id="89ddc-108">If you support the viewing of remote messages, register with the status table to observe activity by transport providers and the MAPI spooler.</span></span> 
  
<span data-ttu-id="89ddc-109">Однако не всегда предпочтительнее использовать уведомления таблиц вместо уведомлений об объектах.</span><span class="sxs-lookup"><span data-stu-id="89ddc-109">However, it is not always preferable to use table notifications instead of object notifications.</span></span> <span data-ttu-id="89ddc-110">Мониторинг изменений количества сообщений в папке является примером того, когда клиенту может потребоваться зарегистрироваться для уведомлений об объектах в папке, а не в таблице, реализованной этой папкой.</span><span class="sxs-lookup"><span data-stu-id="89ddc-110">Monitoring changes in the number of messages in a folder is an example of when your client might need to register for object notifications on a folder rather than on a table implemented by the folder.</span></span>
  

