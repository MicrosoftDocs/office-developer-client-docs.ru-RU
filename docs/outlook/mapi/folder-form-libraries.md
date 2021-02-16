---
title: Библиотеки форм папок
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62b7480e-b3eb-45fb-b74d-62f1dc918a53
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ec12cf567dbbd8c1710f835a3c19369dd3626fd4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414286"
---
# <a name="folder-form-libraries"></a><span data-ttu-id="813c0-103">Библиотеки форм папок</span><span class="sxs-lookup"><span data-stu-id="813c0-103">Folder Form Libraries</span></span>

  
  
<span data-ttu-id="813c0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="813c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="813c0-105">В некоторых случаях может потребоваться связать одну или несколько форм с определенной папкой.</span><span class="sxs-lookup"><span data-stu-id="813c0-105">In some cases, you might want to associate one or more forms with a specific folder.</span></span> <span data-ttu-id="813c0-106">Например, у сотрудников организации может быть папка "Отчет о ходе выполнения" в хранилище личных сообщений для создания и хранения отчетов о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="813c0-106">For example, employees in your organization could all have a Progress Report folder in their personal message store for creating and storing progress reports.</span></span> <span data-ttu-id="813c0-107">Поскольку отчет о ходе выполнения является специфическим для папки отчета о ходе выполнения каждого пользователя, может оказаться не подходящим хранить форму отчета о ходе выполнения в библиотеке форм на всей системе.</span><span class="sxs-lookup"><span data-stu-id="813c0-107">Because the progress report is specific to each user's Progress Report folder, it might not be appropriate to store the progress report form in the system wide form library.</span></span> <span data-ttu-id="813c0-108">Однако копию формы отчета о ходе выполнения можно сохранить в связанной таблице содержимого папки отчета о ходе выполнения каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="813c0-108">However, a copy of the progress report form can be kept in the associated-contents table of each user's Progress Report folder.</span></span> <span data-ttu-id="813c0-109">Это ограничивает использование пользователем форм отчетов о ходе выполнения за пределами указанной папки.</span><span class="sxs-lookup"><span data-stu-id="813c0-109">This restricts the user from using progress report forms outside of the designated folder.</span></span>
  
<span data-ttu-id="813c0-110">Концептуально существует одна библиотека форм папки для каждой папки в хранилище сообщений, даже если в ней не установлены серверы форм.</span><span class="sxs-lookup"><span data-stu-id="813c0-110">Conceptually, there is one folder form library for every folder in a message store, even if no form servers are installed in it.</span></span> <span data-ttu-id="813c0-111">Библиотеки форм папок реализуются так же, как и другие библиотеки форм— они хранятся в виде связанных таблиц содержимого в альтернативной части папки.</span><span class="sxs-lookup"><span data-stu-id="813c0-111">Folder form libraries are implemented like other form libraries — they are stored as associated-contents tables in the alternate part of the folder.</span></span> <span data-ttu-id="813c0-112">Так как библиотеки форм папок содержатся в папке, они копируется вместе с родительской папкой в операциях копирования.</span><span class="sxs-lookup"><span data-stu-id="813c0-112">Because folder form libraries are contained in the folder, they are copied along with their parent folder in copy operations.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="813c0-113">См. также</span><span class="sxs-lookup"><span data-stu-id="813c0-113">See also</span></span>



[<span data-ttu-id="813c0-114">Формы MAPI</span><span class="sxs-lookup"><span data-stu-id="813c0-114">MAPI Forms</span></span>](mapi-forms.md)

