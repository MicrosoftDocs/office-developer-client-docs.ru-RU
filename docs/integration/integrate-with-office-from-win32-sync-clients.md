---
title: Интеграция клиентов синхронизации Win32 с приложениями Office
manager: soliver
ms.date: 07/29/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 348555d3-3cd4-4e4a-b5ad-436571c25251
description: Интеграция клиентов синхронизации Win32 сторонних производителей с приложениями Excel Mobile, русская версия, PowerPoint Mobile и Word Mobile Office.
ms.openlocfilehash: 83bc6e4cddc17e539b371999fff620c72c595534
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303138"
---
# <a name="integrate-with-office-from-win32-sync-clients"></a><span data-ttu-id="85ac6-103">Интеграция клиентов синхронизации Win32 с приложениями Office</span><span class="sxs-lookup"><span data-stu-id="85ac6-103">Integrate with Office from Win32 sync clients</span></span>

<span data-ttu-id="85ac6-104">Интеграция клиентов синхронизации Win32 сторонних производителей с приложениями Excel Mobile, русская версия, PowerPoint Mobile и Word Mobile Office.</span><span class="sxs-lookup"><span data-stu-id="85ac6-104">Integrate your third-party Win32 sync clients with Excel Mobile, PowerPoint Mobile, and Word Mobile Office applications.</span></span> 
  
<span data-ttu-id="85ac6-p101">Вы можете интегрировать универсальные приложения Windows с клиентами Excel Mobile, русская версия, PowerPoint Mobile и Word Mobile, зарегистрировавшись в качестве поставщика корня синхронизации. В этой статье вы найдете практические рекомендации, которые помогут обеспечить безошибочную совместную работу клиентов синхронизации Win32 с приложениями Office.</span><span class="sxs-lookup"><span data-stu-id="85ac6-p101">You can integrate your Windows universal app with Excel Mobile, PowerPoint Mobile, and Word Mobile clients by registering as a sync root provider. This article describes the best practices to apply to ensure that your Win32 sync clients work well with Office applications.</span></span>
  
<span data-ttu-id="85ac6-107">Для такой интеграции необходимо, чтобы клиент синхронизации Win32 имел обработчик синхронизации.</span><span class="sxs-lookup"><span data-stu-id="85ac6-107">This integration requires that your Win32 sync client has a sync engine.</span></span>
  
## <a name="register-as-a-sync-root-provider"></a><span data-ttu-id="85ac6-108">Регистрация в качестве поставщика корня синхронизации</span><span class="sxs-lookup"><span data-stu-id="85ac6-108">Register as a sync root provider</span></span>

<span data-ttu-id="85ac6-p102">Если ваш клиент синхронизации не зарегистрирован как поставщик корня синхронизации, то для приложений Office файлы в папке синхронизации не будут отличаться от обычных локальных файлов. Это значит, что при попытке пользователей предоставить общий доступ к документу, приложения Office будут предлагать им варианты "перехода к OneDrive". Чтобы это не происходило с синхронизируемыми файлами, вы должны зарегистрироваться как поставщик корня синхронизации. О том, как сделать это, можно узнать в [статье об интеграции с поставщиком облачного хранилища](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="85ac6-p102">Unless your sync client is registered as a sync root provider, Office will treat files in your sync folder the way that it treats regular local files. This means that Office will provide "move to OneDrive" options for users when they attempt to share the document. To avoid this for files you sync, you must register as a sync root provider. For information about how to register, see [Integrate a Cloud Storage Provider](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx).</span></span>
  
## <a name="integrate-your-app-into-the-root-node-of-the-navigation-pane"></a><span data-ttu-id="85ac6-113">Интеграция приложения в корневом узле области навигации</span><span class="sxs-lookup"><span data-stu-id="85ac6-113">Integrate your app into the root node of the navigation pane</span></span>

<span data-ttu-id="85ac6-p103">Чтобы клиент синхронизации Win32 отображался как корневой узел в области навигации проводника и средства выбора файлов Windows, необходимо интегрировать приложение на корневом уровне. Сведения об этом можно найти в [статье об интеграции с поставщиком облачного хранилища](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="85ac6-p103">In order for your Win32 sync client to show up as a root node in the navigation pane in the File Explorer and Windows file picker, you need to integrate your app into the root level. For information about how to do this, see [Integrate a Cloud Storage Provider](https://msdn.microsoft.com/library/windows/desktop/dn889934%28v=vs.85%29.aspx).</span></span> 
  
## <a name="add-your-sync-folder-as-a-document-library-optional"></a><span data-ttu-id="85ac6-116">Добавление папки синхронизации в качестве библиотеки документов (необязательно)</span><span class="sxs-lookup"><span data-stu-id="85ac6-116">Add your sync folder as a document library (optional)</span></span>

<span data-ttu-id="85ac6-p104">В приложениях Office пользователи могут создавать документы в библиотеках документов одним действием. Добавить путь к папке синхронизации в библиотеку документов можно с помощью [функции SHAddFolderPathToLibrary](https://msdn.microsoft.com/library/windows/desktop/dd378432%28v=vs.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="85ac6-p104">In Office, users can create documents in their document libraries with a single action. To add your sync location to the document library, use the [SHAddFolderPathToLibrary function](https://msdn.microsoft.com/library/windows/desktop/dd378432%28v=vs.85%29.aspx).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="85ac6-119">См. также</span><span class="sxs-lookup"><span data-stu-id="85ac6-119">See also</span></span>
<span data-ttu-id="85ac6-120"><a name="bk_addresources"> </a></span><span class="sxs-lookup"><span data-stu-id="85ac6-120"><a name="bk_addresources"> </a></span></span>

- [<span data-ttu-id="85ac6-121">Интеграция с Office</span><span class="sxs-lookup"><span data-stu-id="85ac6-121">Integrate with Office</span></span>](integrate-with-office.md)
    
- [<span data-ttu-id="85ac6-122">Интеграция универсальных приложений Windows с Office</span><span class="sxs-lookup"><span data-stu-id="85ac6-122">Integrate with Office from Windows universal apps</span></span>](integrate-with-office-from-windows-universal-apps.md)
    

