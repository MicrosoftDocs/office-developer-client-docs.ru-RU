---
title: Библиотеки форм в папках
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62b7480e-b3eb-45fb-b74d-62f1dc918a53
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f95aa26d6104da657c6ae6ab0c449d45c073223a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580553"
---
# <a name="folder-form-libraries"></a><span data-ttu-id="e4a20-103">Библиотеки форм в папках</span><span class="sxs-lookup"><span data-stu-id="e4a20-103">Folder Form Libraries</span></span>

  
  
<span data-ttu-id="e4a20-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4a20-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4a20-105">В некоторых случаях может потребоваться связать одну или несколько форм с указанной папки.</span><span class="sxs-lookup"><span data-stu-id="e4a20-105">In some cases, you might want to associate one or more forms with a specific folder.</span></span> <span data-ttu-id="e4a20-106">Например сотрудников в организации может все иметь папку отчетов о ходе выполнения в хранилище личных сообщений для создания и хранения отчетов о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="e4a20-106">For example, employees in your organization could all have a Progress Report folder in their personal message store for creating and storing progress reports.</span></span> <span data-ttu-id="e4a20-107">Поскольку отчет о ходе выполнения определенных папку отчет о ходе выполнения каждого пользователя, он может быть неприемлема для хранения форма отчета о ходе выполнения в библиотеке форм широкий системы.</span><span class="sxs-lookup"><span data-stu-id="e4a20-107">Because the progress report is specific to each user's Progress Report folder, it might not be appropriate to store the progress report form in the system wide form library.</span></span> <span data-ttu-id="e4a20-108">Тем не менее копию форма отчета о ходе выполнения можно сохраняются в таблице связанное содержимое папки отчет о ходе выполнения каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="e4a20-108">However, a copy of the progress report form can be kept in the associated-contents table of each user's Progress Report folder.</span></span> <span data-ttu-id="e4a20-109">Это запрещает пользователя с помощью форм отчет о ходе выполнения не из указанной папки.</span><span class="sxs-lookup"><span data-stu-id="e4a20-109">This restricts the user from using progress report forms outside of the designated folder.</span></span>
  
<span data-ttu-id="e4a20-110">Концептуально существует один библиотека форм папки для каждой папки в банке сообщений, даже в том случае, если нет формы серверов установлены в нем.</span><span class="sxs-lookup"><span data-stu-id="e4a20-110">Conceptually, there is one folder form library for every folder in a message store, even if no form servers are installed in it.</span></span> <span data-ttu-id="e4a20-111">Библиотеки форм папки реализуются как другие библиотеки форм, сохраняемые в виде таблицы связанного содержимого в альтернативных части папки.</span><span class="sxs-lookup"><span data-stu-id="e4a20-111">Folder form libraries are implemented like other form libraries — they are stored as associated-contents tables in the alternate part of the folder.</span></span> <span data-ttu-id="e4a20-112">Так как библиотеки форм папки содержатся в папке, они копируются вместе с родительской папки в операции копирования.</span><span class="sxs-lookup"><span data-stu-id="e4a20-112">Because folder form libraries are contained in the folder, they are copied along with their parent folder in copy operations.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e4a20-113">См. также</span><span class="sxs-lookup"><span data-stu-id="e4a20-113">See also</span></span>



[<span data-ttu-id="e4a20-114">Формы MAPI</span><span class="sxs-lookup"><span data-stu-id="e4a20-114">MAPI Forms</span></span>](mapi-forms.md)

