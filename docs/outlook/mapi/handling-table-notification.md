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
# <a name="handling-table-notification"></a><span data-ttu-id="55d65-103">Обработка уведомления о таблице</span><span class="sxs-lookup"><span data-stu-id="55d65-103">Handling table notification</span></span>

<span data-ttu-id="55d65-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55d65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55d65-105">В качестве альтернативы непосредственной регистрации с помощью объекта-источника консультаций, например папки или пользователя обмена сообщениями, клиент может зарегистрироваться для уведомлений на содержимом или таблице иерархии.</span><span class="sxs-lookup"><span data-stu-id="55d65-105">As an alternative to registering directly with an advise source object, such as a folder or a messaging user, a client can register for notifications on a contents or hierarchy table.</span></span> <span data-ttu-id="55d65-106">Отслеживание изменений в записях адресных книг, папок и сообщений с помощью содержимого или таблицы иерархии может быть проще и проще, чем через отдельные объекты.</span><span class="sxs-lookup"><span data-stu-id="55d65-106">Tracking changes to address book entries, folders, and messages through a contents or hierarchy table can be simpler and more straightforward than through individual objects.</span></span> 

<span data-ttu-id="55d65-107">Например, вы можете вызвать [IMAPITable::Advise](imapitable-advise.md) в таблице иерархии папки, чтобы узнать, когда происходят изменения в одном из подстановок.</span><span class="sxs-lookup"><span data-stu-id="55d65-107">For example, you can call [IMAPITable::Advise](imapitable-advise.md) on a folder's hierarchy table to discover when changes occur to one of its subfolders.</span></span> <span data-ttu-id="55d65-108">Если вы поддерживаете просмотр удаленных сообщений, зарегистрируйтесь в таблице состояния, чтобы наблюдать за действиями поставщиков транспорта и пульпера MAPI.</span><span class="sxs-lookup"><span data-stu-id="55d65-108">If you support the viewing of remote messages, register with the status table to observe activity by transport providers and the MAPI spooler.</span></span> 
  
<span data-ttu-id="55d65-109">Однако не всегда предпочтительнее использовать уведомления таблиц вместо уведомлений об объектах.</span><span class="sxs-lookup"><span data-stu-id="55d65-109">However, it is not always preferable to use table notifications instead of object notifications.</span></span> <span data-ttu-id="55d65-110">Мониторинг изменений количества сообщений в папке является примером того, когда клиенту может потребоваться зарегистрироваться для уведомлений об объектах в папке, а не на таблице, реализуемой папкой.</span><span class="sxs-lookup"><span data-stu-id="55d65-110">Monitoring changes in the number of messages in a folder is an example of when your client might need to register for object notifications on a folder rather than on a table implemented by the folder.</span></span>
  

