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
# <a name="folder-form-libraries"></a><span data-ttu-id="2d9c0-103">Библиотеки форм папок</span><span class="sxs-lookup"><span data-stu-id="2d9c0-103">Folder Form Libraries</span></span>

  
  
<span data-ttu-id="2d9c0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d9c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d9c0-105">В некоторых случаях может потребоваться связать одну или несколько форм с определенной папкой.</span><span class="sxs-lookup"><span data-stu-id="2d9c0-105">In some cases, you might want to associate one or more forms with a specific folder.</span></span> <span data-ttu-id="2d9c0-106">Например, сотрудники Организации могут иметь папку отчетов о ходе выполнения в своем личном хранилище сообщений для создания и хранения отчетов о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="2d9c0-106">For example, employees in your organization could all have a Progress Report folder in their personal message store for creating and storing progress reports.</span></span> <span data-ttu-id="2d9c0-107">Так как отчет о ходе выполнения относится к папке отчетов о ходе выполнения каждого пользователя, может оказаться нецелесообразным хранить форму отчета о ходе выполнения в системной библиотеке форм.</span><span class="sxs-lookup"><span data-stu-id="2d9c0-107">Because the progress report is specific to each user's Progress Report folder, it might not be appropriate to store the progress report form in the system wide form library.</span></span> <span data-ttu-id="2d9c0-108">Тем не менее копия формы отчета о ходе выполнения может храниться в таблице сопоставлений содержимого папки отчетов о ходе выполнения каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="2d9c0-108">However, a copy of the progress report form can be kept in the associated-contents table of each user's Progress Report folder.</span></span> <span data-ttu-id="2d9c0-109">Он запрещает пользователю использовать формы отчетов о ходе выполнения вне указанной папки.</span><span class="sxs-lookup"><span data-stu-id="2d9c0-109">This restricts the user from using progress report forms outside of the designated folder.</span></span>
  
<span data-ttu-id="2d9c0-110">Концептуально, существует одна библиотека форм папки для каждой папки в хранилище сообщений, даже если в ней не установлены серверы форм.</span><span class="sxs-lookup"><span data-stu-id="2d9c0-110">Conceptually, there is one folder form library for every folder in a message store, even if no form servers are installed in it.</span></span> <span data-ttu-id="2d9c0-111">Библиотеки форм папки реализуются так же, как и другие библиотеки форм — они хранятся в виде таблиц с содержимым в альтернативной части папки.</span><span class="sxs-lookup"><span data-stu-id="2d9c0-111">Folder form libraries are implemented like other form libraries — they are stored as associated-contents tables in the alternate part of the folder.</span></span> <span data-ttu-id="2d9c0-112">Так как библиотеки форм папки хранятся в папке, они копируются вместе с родительской папкой в операциях копирования.</span><span class="sxs-lookup"><span data-stu-id="2d9c0-112">Because folder form libraries are contained in the folder, they are copied along with their parent folder in copy operations.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2d9c0-113">См. также</span><span class="sxs-lookup"><span data-stu-id="2d9c0-113">See also</span></span>



[<span data-ttu-id="2d9c0-114">Формы MAPI</span><span class="sxs-lookup"><span data-stu-id="2d9c0-114">MAPI Forms</span></span>](mapi-forms.md)

