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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298462"
---
# <a name="maintaining-a-form-library"></a><span data-ttu-id="152db-103">Обслуживание библиотеки форм</span><span class="sxs-lookup"><span data-stu-id="152db-103">Maintaining a Form Library</span></span>

  
  
<span data-ttu-id="152db-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="152db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="152db-105">В библиотеке форм хранятся все важные сведения о форме: ее свойствах, ее командах и исполняемых файлах сервера.</span><span class="sxs-lookup"><span data-stu-id="152db-105">A form library holds all of the important information about a form: its properties, its verbs, and its server's executable files.</span></span> <span data-ttu-id="152db-106">Некоторые клиенты позволяют пользователям поддерживать, устанавливать и удалять серверы форм.</span><span class="sxs-lookup"><span data-stu-id="152db-106">Some clients allow their users to maintain, install, or remove form servers.</span></span> <span data-ttu-id="152db-107">Если вы хотите предоставить эту функцию пользователям, у вас должен быть доступ к:</span><span class="sxs-lookup"><span data-stu-id="152db-107">If you want to offer this feature to your users, you must have access to:</span></span>
  
- <span data-ttu-id="152db-108">Файл конфигурации сервера форм, файл с расширением. Добавочный номер CFG.</span><span class="sxs-lookup"><span data-stu-id="152db-108">The form server's configuration file, a file with the .CFG extension.</span></span>
    
- <span data-ttu-id="152db-109">Объект контейнера библиотеки форм, объект, реализующий интерфейс [имапиформконтаинер: IUnknown](imapiformcontaineriunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="152db-109">The form library's container object, an object that implements the [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
<span data-ttu-id="152db-110">Чтобы получить доступ к файлу конфигурации или пути, используйте любое удобное средство.</span><span class="sxs-lookup"><span data-stu-id="152db-110">To access the configuration file or a pathname to it, use whatever means are convenient.</span></span> <span data-ttu-id="152db-111">Как правило, клиенты предоставляют пользователю диалоговое окно для установки и удаления серверов форм, которые также могут использоваться для приглашения пользователя указать расположение файла конфигурации.</span><span class="sxs-lookup"><span data-stu-id="152db-111">Usually, clients present the user with a dialog box for installing and removing form servers that can also be used to prompt the user for the location of the configuration file.</span></span>
  
<span data-ttu-id="152db-112">Чтобы получить доступ к контейнеру библиотеки форм, вызовите метод [имапиформмгр:: опенформконтаинер](imapiformmgr-openformcontainer.md) диспетчера форм.</span><span class="sxs-lookup"><span data-stu-id="152db-112">To access the form library's container, call the form manager's [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method.</span></span> <span data-ttu-id="152db-113">Передайте значение перечисления, чтобы указать, какую библиотеку форм следует открыть, и при необходимости указатель на объект, который диспетчер формы должен использовать для открытия библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="152db-113">Pass in an enumeration value to specify which form library to open, and if necessary, a pointer to the object that the form manager should use to open the form library.</span></span> <span data-ttu-id="152db-114">Например, при открытии [библиотек форм папки](folder-form-libraries.md)передается указатель [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="152db-114">For example, if you are opening a [Folder Form Libraries](folder-form-libraries.md), pass an [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) pointer.</span></span> 
  
<span data-ttu-id="152db-115">После того как **опенформконтаинер** возвратит указатель **имапиформконтаинер** , вызовите любой из [Имапиформконтаинер:: Инсталлформ](imapiformcontainer-installform.md) или [имапиформконтаинер:: RemoveForm](imapiformcontainer-removeform.md), в зависимости от выполняемого обслуживания.</span><span class="sxs-lookup"><span data-stu-id="152db-115">After **OpenFormContainer** returns the **IMAPIFormContainer** pointer, call either [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) or [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), depending on the maintenance to be performed.</span></span> <span data-ttu-id="152db-116">**Инсталлформ** добавляет сервер форм в библиотеку; **Ремовеформ** удаляет сервер форм из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="152db-116">**InstallForm** adds a form server to the library; **RemoveForm** deletes a form server from the library.</span></span> 
  

