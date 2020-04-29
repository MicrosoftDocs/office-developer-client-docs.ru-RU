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
# <a name="handling-table-notification"></a><span data-ttu-id="31d53-103">Обработка уведомления о таблице</span><span class="sxs-lookup"><span data-stu-id="31d53-103">Handling table notification</span></span>

<span data-ttu-id="31d53-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31d53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31d53-105">В качестве альтернативы регистрации напрямую с исходным объектом advise, например папкой или пользователем обмена сообщениями, клиент может зарегистрироваться для получения уведомлений по содержимому или таблице иерархии.</span><span class="sxs-lookup"><span data-stu-id="31d53-105">As an alternative to registering directly with an advise source object, such as a folder or a messaging user, a client can register for notifications on a contents or hierarchy table.</span></span> <span data-ttu-id="31d53-106">Отслеживание изменений записей адресной книги, папок и сообщений с помощью таблицы контента или иерархии может быть проще и проще, чем через отдельные объекты.</span><span class="sxs-lookup"><span data-stu-id="31d53-106">Tracking changes to address book entries, folders, and messages through a contents or hierarchy table can be simpler and more straightforward than through individual objects.</span></span> 

<span data-ttu-id="31d53-107">Например, вы можете вызвать метод [IMAPITable:: Advise](imapitable-advise.md) для таблицы иерархии папки, чтобы определить, когда изменения происходят в одной из вложенных в нее папок.</span><span class="sxs-lookup"><span data-stu-id="31d53-107">For example, you can call [IMAPITable::Advise](imapitable-advise.md) on a folder's hierarchy table to discover when changes occur to one of its subfolders.</span></span> <span data-ttu-id="31d53-108">Если вы поддерживаете Просмотр удаленных сообщений, зарегистрируйте их в таблице состояния, чтобы наблюдать за действиями от поставщиков транспорта и диспетчера очереди MAPI.</span><span class="sxs-lookup"><span data-stu-id="31d53-108">If you support the viewing of remote messages, register with the status table to observe activity by transport providers and the MAPI spooler.</span></span> 
  
<span data-ttu-id="31d53-109">Тем не менее, не всегда рекомендуется использовать уведомления таблиц вместо уведомлений объектов.</span><span class="sxs-lookup"><span data-stu-id="31d53-109">However, it is not always preferable to use table notifications instead of object notifications.</span></span> <span data-ttu-id="31d53-110">Наблюдение за изменениями в количестве сообщений в папке — это пример того, что клиенту может понадобиться зарегистрировать уведомления объектов в папке, а не в таблице, реализуемой папкой.</span><span class="sxs-lookup"><span data-stu-id="31d53-110">Monitoring changes in the number of messages in a folder is an example of when your client might need to register for object notifications on a folder rather than on a table implemented by the folder.</span></span>
  

