---
title: Обслуживание библиотеки форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 5ccb5a2881d3cef3ff21a106e7e9ea33e0aedd9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809669"
---
# <a name="maintaining-a-form-library"></a><span data-ttu-id="bc7f6-103">Обслуживание библиотеки форм</span><span class="sxs-lookup"><span data-stu-id="bc7f6-103">Maintaining a Form Library</span></span>

  
  
<span data-ttu-id="bc7f6-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bc7f6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bc7f6-105">Библиотека форм хранит все важные сведения об формы: его свойства, его команды и его сервер исполняемых файлов.</span><span class="sxs-lookup"><span data-stu-id="bc7f6-105">A form library holds all of the important information about a form: its properties, its verbs, and its server's executable files.</span></span> <span data-ttu-id="bc7f6-106">Некоторые клиенты их пользователи могли поддерживать, Установка и удаление серверов формы.</span><span class="sxs-lookup"><span data-stu-id="bc7f6-106">Some clients allow their users to maintain, install, or remove form servers.</span></span> <span data-ttu-id="bc7f6-107">Если вы хотите предлагать этой функции для пользователей, должны иметь доступ к:</span><span class="sxs-lookup"><span data-stu-id="bc7f6-107">If you want to offer this feature to your users, you must have access to:</span></span>
  
- <span data-ttu-id="bc7f6-108">Файл конфигурации сервера форм, файла с помощью. Расширение CFG.</span><span class="sxs-lookup"><span data-stu-id="bc7f6-108">The form server's configuration file, a file with the .CFG extension.</span></span>
    
- <span data-ttu-id="bc7f6-109">Объект-контейнер библиотеки форм, объект, реализующий [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bc7f6-109">The form library's container object, an object that implements the [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
<span data-ttu-id="bc7f6-110">Для доступа к файлу конфигурации или путь к нему, использование удобны доступным способом.</span><span class="sxs-lookup"><span data-stu-id="bc7f6-110">To access the configuration file or a pathname to it, use whatever means are convenient.</span></span> <span data-ttu-id="bc7f6-111">Как правило клиенты предоставить пользователю диалогового окна Установка и удаление серверов форм, которые также могут использоваться для запроса пользователя для расположения файла конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bc7f6-111">Usually, clients present the user with a dialog box for installing and removing form servers that can also be used to prompt the user for the location of the configuration file.</span></span>
  
<span data-ttu-id="bc7f6-112">Для доступа к container библиотека форм, вызовите метод [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) диспетчер форм.</span><span class="sxs-lookup"><span data-stu-id="bc7f6-112">To access the form library's container, call the form manager's [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method.</span></span> <span data-ttu-id="bc7f6-113">Передайте значение перечисления, чтобы указать, какие библиотеки форм, чтобы открыть и при необходимости указатель на объект, который необходимо использовать диспетчер форм, чтобы открыть библиотеку форм.</span><span class="sxs-lookup"><span data-stu-id="bc7f6-113">Pass in an enumeration value to specify which form library to open, and if necessary, a pointer to the object that the form manager should use to open the form library.</span></span> <span data-ttu-id="bc7f6-114">Например, при открытии [Библиотеки форм папки](folder-form-libraries.md)передать [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) указателя.</span><span class="sxs-lookup"><span data-stu-id="bc7f6-114">For example, if you are opening a [Folder Form Libraries](folder-form-libraries.md), pass an [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) pointer.</span></span> 
  
<span data-ttu-id="bc7f6-115">После **OpenFormContainer** возвращает указатель **IMAPIFormContainer** , вызовите [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) или [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), в зависимости от обслуживания необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="bc7f6-115">After **OpenFormContainer** returns the **IMAPIFormContainer** pointer, call either [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) or [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), depending on the maintenance to be performed.</span></span> <span data-ttu-id="bc7f6-116">**InstallForm** Добавление сервера формы в библиотеке. **RemoveForm** удаление сервера формы из библиотеки.</span><span class="sxs-lookup"><span data-stu-id="bc7f6-116">**InstallForm** adds a form server to the library; **RemoveForm** deletes a form server from the library.</span></span> 
  

