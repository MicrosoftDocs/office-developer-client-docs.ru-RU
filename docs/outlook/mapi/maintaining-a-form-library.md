---
title: Обслуживание библиотеки форм
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
# <a name="maintaining-a-form-library"></a><span data-ttu-id="7a3a1-103">Обслуживание библиотеки форм</span><span class="sxs-lookup"><span data-stu-id="7a3a1-103">Maintaining a Form Library</span></span>

  
  
<span data-ttu-id="7a3a1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a3a1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a3a1-105">Библиотека форм содержит все важные сведения о форме: ее свойства, команды и исполняемые файлы сервера.</span><span class="sxs-lookup"><span data-stu-id="7a3a1-105">A form library holds all of the important information about a form: its properties, its verbs, and its server's executable files.</span></span> <span data-ttu-id="7a3a1-106">Некоторые клиенты позволяют своим пользователям обслуживать, устанавливать или удалять серверы форм.</span><span class="sxs-lookup"><span data-stu-id="7a3a1-106">Some clients allow their users to maintain, install, or remove form servers.</span></span> <span data-ttu-id="7a3a1-107">Если вы хотите предложить эту функцию пользователям, у вас должен быть доступ к:</span><span class="sxs-lookup"><span data-stu-id="7a3a1-107">If you want to offer this feature to your users, you must have access to:</span></span>
  
- <span data-ttu-id="7a3a1-108">Файл конфигурации сервера форм, файл с файлом . Расширение CFG.</span><span class="sxs-lookup"><span data-stu-id="7a3a1-108">The form server's configuration file, a file with the .CFG extension.</span></span>
    
- <span data-ttu-id="7a3a1-109">Объект контейнера библиотеки форм, который реализует [интерфейс IMAPIFormContainer : IUnknown.](imapiformcontaineriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="7a3a1-109">The form library's container object, an object that implements the [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
<span data-ttu-id="7a3a1-110">Чтобы получить к нему доступ к файлу конфигурации или имени пути, используйте любые удобные средства.</span><span class="sxs-lookup"><span data-stu-id="7a3a1-110">To access the configuration file or a pathname to it, use whatever means are convenient.</span></span> <span data-ttu-id="7a3a1-111">Обычно клиенты представляют пользователю диалоговое окно для установки и удаления серверов форм, которое также можно использовать для запроса расположения файла конфигурации.</span><span class="sxs-lookup"><span data-stu-id="7a3a1-111">Usually, clients present the user with a dialog box for installing and removing form servers that can also be used to prompt the user for the location of the configuration file.</span></span>
  
<span data-ttu-id="7a3a1-112">Чтобы получить доступ к контейнеру библиотеки форм, вызовите метод [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) диспетчера форм.</span><span class="sxs-lookup"><span data-stu-id="7a3a1-112">To access the form library's container, call the form manager's [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method.</span></span> <span data-ttu-id="7a3a1-113">Передав значение из enumeration, укажите, какую библиотеку форм следует открыть, и при необходимости указатель на объект, который диспетчер форм должен использовать для открытия библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="7a3a1-113">Pass in an enumeration value to specify which form library to open, and if necessary, a pointer to the object that the form manager should use to open the form library.</span></span> <span data-ttu-id="7a3a1-114">Например, если вы открываете библиотеки форм [папок,](folder-form-libraries.md)передав [указатель IMAPIFolder : IMAPIContainer.](imapifolderimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="7a3a1-114">For example, if you are opening a [Folder Form Libraries](folder-form-libraries.md), pass an [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) pointer.</span></span> 
  
<span data-ttu-id="7a3a1-115">После того как **OpenFormContainer** вернет указатель **IMAPIFormContainer,** вызовите [либо IMAPIFormContainer::InstallForm,](imapiformcontainer-installform.md) либо [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), в зависимости от выполняемого обслуживания.</span><span class="sxs-lookup"><span data-stu-id="7a3a1-115">After **OpenFormContainer** returns the **IMAPIFormContainer** pointer, call either [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) or [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), depending on the maintenance to be performed.</span></span> <span data-ttu-id="7a3a1-116">**InstallForm** добавляет сервер форм в библиотеку; **RemoveForm** удаляет сервер форм из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="7a3a1-116">**InstallForm** adds a form server to the library; **RemoveForm** deletes a form server from the library.</span></span> 
  

