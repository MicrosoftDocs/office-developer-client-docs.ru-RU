---
title: Ведение библиотеки форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 51c7c3f8ba70dcb3d35dc50806e984fd4b193818
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408805"
---
# <a name="maintaining-a-form-library"></a><span data-ttu-id="ae684-103">Ведение библиотеки форм</span><span class="sxs-lookup"><span data-stu-id="ae684-103">Maintaining a Form Library</span></span>

  
  
<span data-ttu-id="ae684-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae684-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae684-105">Библиотека форм содержит всю важную информацию о форме: ее свойствах, глаголах и исполняемых файлах сервера.</span><span class="sxs-lookup"><span data-stu-id="ae684-105">A form library holds all of the important information about a form: its properties, its verbs, and its server's executable files.</span></span> <span data-ttu-id="ae684-106">Некоторые клиенты позволяют пользователям поддерживать, устанавливать или удалять серверы форм.</span><span class="sxs-lookup"><span data-stu-id="ae684-106">Some clients allow their users to maintain, install, or remove form servers.</span></span> <span data-ttu-id="ae684-107">Если вы хотите предложить эту функцию пользователям, у вас должен быть доступ к:</span><span class="sxs-lookup"><span data-stu-id="ae684-107">If you want to offer this feature to your users, you must have access to:</span></span>
  
- <span data-ttu-id="ae684-108">Файл конфигурации сервера форм, файл с файлом . Расширение CFG.</span><span class="sxs-lookup"><span data-stu-id="ae684-108">The form server's configuration file, a file with the .CFG extension.</span></span>
    
- <span data-ttu-id="ae684-109">Контейнерный объект библиотеки форм, объект, который реализует [интерфейс IMAPIFormContainer: IUnknown.](imapiformcontaineriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="ae684-109">The form library's container object, an object that implements the [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
<span data-ttu-id="ae684-110">Чтобы получить доступ к файлу конфигурации или имени пути к нему, используйте любые удобные средства.</span><span class="sxs-lookup"><span data-stu-id="ae684-110">To access the configuration file or a pathname to it, use whatever means are convenient.</span></span> <span data-ttu-id="ae684-111">Обычно клиенты представляют пользователю диалоговое окно для установки и удаления серверов форм, которые также могут быть использованы для запроса пользователя на расположение файла конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ae684-111">Usually, clients present the user with a dialog box for installing and removing form servers that can also be used to prompt the user for the location of the configuration file.</span></span>
  
<span data-ttu-id="ae684-112">Чтобы получить доступ к контейнеру библиотеки форм, позвоните по методу [IMAPIFormMgr::OpenFormContainer.](imapiformmgr-openformcontainer.md)</span><span class="sxs-lookup"><span data-stu-id="ae684-112">To access the form library's container, call the form manager's [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method.</span></span> <span data-ttu-id="ae684-113">Передай в значении переоформления, чтобы указать, какую библиотеку форм открыть, а при необходимости - указатель на объект, который должен использовать руководитель форм для открытия библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="ae684-113">Pass in an enumeration value to specify which form library to open, and if necessary, a pointer to the object that the form manager should use to open the form library.</span></span> <span data-ttu-id="ae684-114">Например, если вы открываете библиотеки форм [папок,](folder-form-libraries.md)передай [указатель IMAPIFolder: IMAPIContainer.](imapifolderimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="ae684-114">For example, if you are opening a [Folder Form Libraries](folder-form-libraries.md), pass an [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) pointer.</span></span> 
  
<span data-ttu-id="ae684-115">После того как **OpenFormContainer** возвращает указатель **IMAPIFormContainer,** позвоните либо [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) или [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), в зависимости от выполняемого обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ae684-115">After **OpenFormContainer** returns the **IMAPIFormContainer** pointer, call either [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) or [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), depending on the maintenance to be performed.</span></span> <span data-ttu-id="ae684-116">**InstallForm** добавляет сервер формы в библиотеку; **RemoveForm** удаляет сервер формы из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="ae684-116">**InstallForm** adds a form server to the library; **RemoveForm** deletes a form server from the library.</span></span> 
  

