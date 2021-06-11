---
title: Библиотека JavaScript и ссылка REST для Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 67b47b8b-d34b-4fad-af49-0c258c345ad2
description: Библиотека JavaScript и ссылка REST для Project Server 2013 содержат сведения об объектной модели JavaScript и интерфейсе REST, которые используются для доступа к Project Server. Эти API можно использовать для разработки меж браузерных веб-приложений, надстройок Project профессиональный 2013 г., а также приложений для устройств Windows, которые имеют доступ к Project Server 2013 и Project Online.
ms.openlocfilehash: fb58de1e3858a39f42cc9a643a7394cec191a462
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358109"
---
# <a name="javascript-library-and-rest-reference-for-project-server"></a>Библиотека JavaScript и ссылка REST для Project Server

Библиотека JavaScript и ссылка REST для Project Server 2013 содержат сведения об объектной модели JavaScript и интерфейсе REST, которые используются для доступа к Project Server. Эти API можно использовать для разработки меж браузерных веб-приложений, надстройок Project профессиональный 2013 г., а также приложений для устройств Windows, которые имеют доступ к Project Server 2013 и Project Online.
  
> [!NOTE]
> Объектная модель JavaScript и интерфейс REST совпадают с клиентской объектной моделью Project Server (CSOM). Они предоставляют эквивалентные функции пространству **имен Microsoft.ProjectServer.Client** в CSOM. 
  
Вы можете получить доступ Project Server с помощью объектной модели JavaScript, которая определяется в [пространстве имен PS](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) в `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js` файле. Объект [ProjectContext в](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) [пространстве имен PS](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) является точкой входа в объектную модель JavaScript. 
  
> [!NOTE]
> Чтобы просмотреть объектную модель JavaScript и помочь в отладки, вы можете использовать PS.debug.js в том же каталоге. Чтобы помочь в разработке на удаленном компьютере, [загрузка SDK Project 2013](https://www.microsoft.com/en-us/download/details.aspx?id=30435) включает сборки платформа .NET Framework для CSOM, а также PS.js и PS.debug.js файлов. 
  
Вы также можете получить доступ Project Server с помощью интерфейса REST. Точкой входа в интерфейс REST является ресурс **ProjectServer,** к которому можно получить доступ с помощью  `https://ServerName/pwaName/_api/ProjectServer` конечной URI точки. Например, следующий запрос получает назначения в указанном проекте  _(замените ServerName_ и  _pwaName_ и измените GUID в соответствии с проектом).
  
`https://ServerName/pwaName/_api/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments`

Ресурс **ProjectServer** описан в ресурсах [ProjectServer в интерфейсе REST.](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx#bk_ProjectServerResources) Другие ресурсы REST описаны в документации для соответствующих объектов и участников JavaScript в этой ссылке. Дополнительные сведения об использовании REST см. в примере Клиентская объектная модель [(CSOM)](client-side-object-model-csom-for-project-2013.md) для Project Server и Программирование с помощью [службы REST 2013 SharePoint 2013 года.](https://msdn.microsoft.com/library/fp142385%28office.15%29.aspx)
  
## <a name="javascript-library-and-rest-reference-for-project-server"></a>Библиотека JavaScript и ссылка REST для Project Server
<a name="pj15_JavaScriptAPIReference_PS"> </a>

- [PS.js JavaScript и ссылка REST](https://msdn.microsoft.com/library/5a140021-380a-d9e0-e36d-106df85f56d6%28Office.15%29.aspx) Содержит сведения об объектной модели JavaScript и интерфейсе REST для Project Server 2013. 
    
## <a name="see-also"></a>См. также
<a name="bk_addresources"> </a>

- [Документация для разработчиков Project 2013](project-2013-developer-documentation.md)   
- [Клиентская объектная модель (CSOM) для Project Server](client-side-object-model-csom-for-project-2013.md)   
- [Начало работы с объектной моделью JavaScript](getting-started-with-the-project-server-2013-javascript-object-model.md)  
- [Работа с проектами при помощи объектной модели JavaScript](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    

