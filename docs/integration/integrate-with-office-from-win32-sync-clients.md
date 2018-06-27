---
title: Интеграция клиентов синхронизации Win32 с приложениями Office
manager: soliver
ms.date: 07/29/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 348555d3-3cd4-4e4a-b5ad-436571c25251
description: Интеграция клиентов синхронизации Win32 сторонних производителей с приложениями Excel Mobile, русская версия, PowerPoint Mobile и Word Mobile Office.
ms.openlocfilehash: 9f520ad36583a9aa7cd73638fe92158f70d13daf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807612"
---
# <a name="integrate-with-office-from-win32-sync-clients"></a>Интеграция клиентов синхронизации Win32 с приложениями Office

Интеграция клиентов синхронизации Win32 сторонних производителей с приложениями Excel Mobile, русская версия, PowerPoint Mobile и Word Mobile Office. 
  
Вы можете интегрировать универсальные приложения Windows с клиентами Excel Mobile, русская версия, PowerPoint Mobile и Word Mobile, зарегистрировавшись в качестве поставщика корня синхронизации. В этой статье вы найдете практические рекомендации, которые помогут обеспечить безошибочную совместную работу клиентов синхронизации Win32 с приложениями Office.
  
Для такой интеграции необходимо, чтобы клиент синхронизации Win32 имел обработчик синхронизации.
  
## <a name="register-as-a-sync-root-provider"></a>Регистрация в качестве поставщика корня синхронизации

Если ваш клиент синхронизации не зарегистрирован как поставщик корня синхронизации, то для приложений Office файлы в папке синхронизации не будут отличаться от обычных локальных файлов. Это значит, что при попытке пользователей предоставить общий доступ к документу, приложения Office будут предлагать им варианты "перехода к OneDrive". Чтобы это не происходило с синхронизируемыми файлами, вы должны зарегистрироваться как поставщик корня синхронизации. О том, как сделать это, можно узнать в [статье об интеграции с поставщиком облачного хранилища](https://msdn.microsoft.com/ru-RU/library/windows/desktop/dn889934%28v=vs.85%29.aspx).
  
## <a name="integrate-your-app-into-the-root-node-of-the-navigation-pane"></a>Интеграция приложения в корневом узле области навигации

Чтобы клиент синхронизации Win32 отображался как корневой узел в области навигации проводника и средства выбора файлов Windows, необходимо интегрировать приложение на корневом уровне. Сведения об этом можно найти в [статье об интеграции с поставщиком облачного хранилища](https://msdn.microsoft.com/ru-RU/library/windows/desktop/dn889934%28v=vs.85%29.aspx). 
  
## <a name="add-your-sync-folder-as-a-document-library-optional"></a>Добавление папки синхронизации в качестве библиотеки документов (необязательно)

В приложениях Office пользователи могут создавать документы в библиотеках документов одним действием. Добавить путь к папке синхронизации в библиотеку документов можно с помощью [функции SHAddFolderPathToLibrary](https://msdn.microsoft.com/ru-RU/library/windows/desktop/dd378432%28v=vs.85%29.aspx). 
  
## <a name="see-also"></a>См. также
<a name="bk_addresources"> </a>

- [Интеграция с Office](integrate-with-office.md)
    
- [Интеграция универсальных приложений Windows с Office](integrate-with-office-from-windows-universal-apps.md)
    

