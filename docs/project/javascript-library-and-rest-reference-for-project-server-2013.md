---
title: Библиотека JavaScript и справочные материалы по REST для Project Server
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 67b47b8b-d34b-4fad-af49-0c258c345ad2
description: Библиотека JavaScript и ссылка REST для Project Server 2013 содержит сведения об объектной модели JavaScript и интерфейсе REST, которые используются для доступа к функциям Project Server. Эти API можно использовать для разработки веб-приложений с перекрестными браузерами, надстроек Project профессиональный 2013 и приложений для устройств, отличных от Windows, которые обращаются к Project Server 2013 и Project Online.
ms.openlocfilehash: fb58de1e3858a39f42cc9a643a7394cec191a462
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358109"
---
# <a name="javascript-library-and-rest-reference-for-project-server"></a>Библиотека JavaScript и справочные материалы по REST для Project Server

Библиотека JavaScript и ссылка REST для Project Server 2013 содержит сведения об объектной модели JavaScript и интерфейсе REST, которые используются для доступа к функциям Project Server. Эти API можно использовать для разработки веб-приложений с перекрестными браузерами, надстроек Project профессиональный 2013 и приложений для устройств, отличных от Windows, которые обращаются к Project Server 2013 и Project Online.
  
> [!NOTE]
> Объектная модель JavaScript и интерфейс REST выравниваются с помощью клиентской объектной модели Project Server (CSOM). Они предоставляют эквивалентные функции пространству имен **Microsoft. Project. Client** в CSOM. 
  
Можно получить доступ к функциям Project Server с помощью объектной модели JavaScript, которая определена в пространстве имен `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js` [PS](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) в файле. Объект [ProjectContext](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) в пространстве имен [PS](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) является точкой входа для объектной модели JavaScript. 
  
> [!NOTE]
> Чтобы просмотреть объектную модель JavaScript и упростить отладку, можно использовать файл PS. Debug. js в том же каталоге. Для упрощения разработки на удаленном компьютере [загружаемый пакет SDK для Project 2013](https://www.microsoft.com/en-us/download/details.aspx?id=30435) включает сборки .NET Framework для CSOM, а также файлы PS. js и PS. Debug. js. 
  
Вы также можете получать доступ к функциям Project Server с помощью интерфейса REST. Точкой входа для интерфейса REST является ресурс **Project** , доступ к которому осуществляется с помощью URI `https://ServerName/pwaName/_api/ProjectServer` конечной точки. Например, следующий запрос получает назначения в указанном проекте (Replace _ServerName_ и _ПВАНАМЕ_и изменяет GUID в соответствии с проектом).
  
`https://ServerName/pwaName/_api/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments`

Ресурс **Project** описывается в [ресурсах Project в интерфейсе REST](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx#bk_ProjectServerResources). Другие ресурсы REST описаны в документации по соответствующим объектам JavaScript и элементам в этой справочной статье. Дополнительные сведения об использовании REST можно найти в статье [клиентская объектная модель (CSOM) для Project Server](client-side-object-model-csom-for-project-2013.md) и [программирование с помощью службы SharePoint 2013 REST](https://msdn.microsoft.com/library/fp142385%28office.15%29.aspx).
  
## <a name="javascript-library-and-rest-reference-for-project-server"></a>Библиотека JavaScript и справочные материалы по REST для Project Server
<a name="pj15_JavaScriptAPIReference_PS"> </a>

- [Библиотека JavaScript для PS. js и справочные материалы по REST](https://msdn.microsoft.com/library/5a140021-380a-d9e0-e36d-106df85f56d6%28Office.15%29.aspx) Содержит сведения об объектной модели JavaScript и интерфейсе REST для Project Server 2013. 
    
## <a name="see-also"></a>См. также
<a name="bk_addresources"> </a>

- [Документация для разработчиков Project 2013](project-2013-developer-documentation.md)   
- [Клиентская объектная модель (CSOM) для Project Server](client-side-object-model-csom-for-project-2013.md)   
- [Начало работы с объектной моделью JavaScript](getting-started-with-the-project-server-2013-javascript-object-model.md)  
- [Работа с проектами при помощи объектной модели JavaScript](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    

