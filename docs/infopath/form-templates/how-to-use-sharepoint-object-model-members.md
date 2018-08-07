---
title: Использование элементов объектной модели SharePoint
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8cbafca3-7831-4231-8e61-38330b5ad61b
description: Прежде чем начать программировать с использованием членов объектной модели SharePoint из кода, выполняемого в форме InfoPath, необходимо определить ссылку на сборку Microsoft.SharePoint.dll в проекте набора Visual Studio 2012 для формы. Для этого требуется доступ к файловой системе лицензионной копии Microsoft SharePoint Server 2010 или сервера, на котором выполняются Microsoft SharePoint Foundation 2010, чтобы получить копию сборки Microsoft.SharePoint.dll.
ms.openlocfilehash: c496f603f50a55ae2eaee237d6910d92612e1761
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807495"
---
# <a name="use-sharepoint-object-model-members"></a>Использование элементов объектной модели SharePoint

Прежде чем начать программировать с использованием членов объектной модели SharePoint из кода, выполняемого в форме InfoPath, необходимо определить ссылку на сборку Microsoft.SharePoint.dll в проекте набора Visual Studio 2012 для формы. Для этого требуется доступ к файловой системе лицензионной копии Microsoft SharePoint Server 2010 или сервера, на котором выполняются Microsoft SharePoint Foundation 2010, чтобы получить копию сборки Microsoft.SharePoint.dll. 
  
Кроме того, необходимо развернуть шаблон формы на сервере в качестве изолированного или утвержденного администратором решения. Дополнительные сведения об этих параметрах развертывания [Публикация форм с кодом](publishing-forms-with-code.md).
  
## <a name="add-and-reference-the-microsoftsharepoint-assembly-from-an-infopath-form-template"></a>Добавление ссылки на сборку Microsoft.SharePoint из шаблона формы InfoPath

> [!IMPORTANT]
> [!Важно!] Чтобы избежать конфликта с процессом управления системой проектов InfoPath файлами, добавляемыми в файл шаблона формы, не копируйте сборки, на которые требуется указать ссылки, в папку верхнего уровня проекта шаблона формы. По умолчанию это путь в следующем формате: < *диск*  >:\Users\  *имя_пользователя*  \Documents\InfoPath Projects\  *имя_проекта* > Если требуется переместить сборки, на которые требуется указать ссылки, внутри папки проекта, то следует создать вложенную папку в главной папке проекта  *ProjectName*  , скопировать сборки в эту вложенную папку и указать соответствующие ссылки на эту папку. Однако обратите внимание, что создавать вложенную папку для сборок, на которые добавлены ссылки, необязательно. Если такая сборка не расположена в папке верхнего уровня проекта, система проектов InfoPath скопирует сборку в файл шаблона формы (XSN-файл) при компиляции и публикации проекта. 
  
По умолчанию сборка Microsoft.SharePoint.Server.dll устанавливается в папку C:\Program Files\Common Files\Microsoft Shared\Web Server\Extensions\14\ISAPI в файловой системе SharePoint Server 2010 или сервера, на котором запущены службы SharePoint Foundation 2010.
  
### <a name="to-reference-the-microsoftsharepoint-assembly-from-an-infopath-forms-code-project"></a>Добавление ссылки на сборку Microsoft.SharePoint из проекта кода формы InfoPath

1. Скопируйте сборку Microsoft.SharePoint.Server.dll с сервера в локальную папку или получите доступ к сборке из общей папки.
    
2. Откройте проект шаблона формы в наборе Visual Studio 2012.
    
3. В меню **Проект** выберите пункт **Добавить ссылку**.
    
4. Найдите и укажите сборку на вкладке **Обзор**, после чего нажмите кнопку **ОК**, чтобы добавить ссылку. 
    
После этого можно создавать код с использованием членов объектной модели SharePoint в коде формы. Для большего удобства при использовании ссылок на члены пространства имен Microsoft.SharePoint добавьте директивы  `using Microsoft.SharePoint;` или  `Imports Microsoft.SharePoint` в раздел директив в начале файла кода. Пример, в котором показано использование членов объектной модели SharePoint в форме InfoPath, см. в разделе "Пример 2. Управление поставщиками в списке SharePoint" в статье [Примеры изолированных решений](sample-sandboxed-solutions.md).

