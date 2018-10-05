---
title: Справочник по REST для Project Server и библиотеки JavaScript
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 67b47b8b-d34b-4fad-af49-0c258c345ad2
description: Библиотеки JavaScript и REST ссылки для Project Server 2013 содержит сведения об объектной модели JavaScript и интерфейс REST, которая используется для доступа к возможностям Project Server. Можно использовать эти интерфейсы API для разработки веб-браузеров приложений, Project Professional 2013 надстроек и приложений для устройств отличных от Windows, доступ к Project Server 2013 и Project Online.
ms.openlocfilehash: fb58de1e3858a39f42cc9a643a7394cec191a462
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399034"
---
# <a name="javascript-library-and-rest-reference-for-project-server"></a>Справочник по REST для Project Server и библиотеки JavaScript

Библиотеки JavaScript и REST ссылки для Project Server 2013 содержит сведения об объектной модели JavaScript и интерфейс REST, которая используется для доступа к возможностям Project Server. Можно использовать эти интерфейсы API для разработки веб-браузеров приложений, Project Professional 2013 надстроек и приложений для устройств отличных от Windows, доступ к Project Server 2013 и Project Online.
  
> [!NOTE]
> Объектная модель JavaScript и интерфейс REST выровнять с Project Server клиентской объектной модели (CSOM). Они предоставляют функциональность для пространства имен **Microsoft.ProjectServer.Client** в CSOM. 
  
Функциональные возможности Project Server доступны по объектной модели JavaScript, которая определена в пространстве имен [PS](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) в `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.js` файла. Объект [ProjectContext](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx) в пространстве имен [PS](https://msdn.microsoft.com/library/e3156167-a4fd-1bf6-8d1c-e180de1844ed%28Office.15%29.aspx) — точка входа для объектной модели JavaScript. 
  
> [!NOTE]
> При отладке и обзор объектной модели JavaScript, можно использовать файл PS.debug.js в том же каталоге. Для облегчения разработки на удаленном компьютере, [Загрузите пакет SDK Project 2013](https://www.microsoft.com/en-us/download/details.aspx?id=30435) включает в себя сборки .NET Framework для CSOM и файлы PS.js и PS.debug.js. 
  
Можно также получить доступ к функциональности Project Server через интерфейс REST. Точка входа в интерфейсе REST является ресурсом **ProjectServer** , доступ к которому осуществляется с помощью `https://ServerName/pwaName/_api/ProjectServer` URI конечной точки. Например, следующий запрос получает назначения в указанный проект (Замените _имя сервера_ и _pwaName_и измените идентификатор GUID в соответствии с проектом).
  
`https://ServerName/pwaName/_api/ProjectServer/Projects('263fc8d7-427c-e111-92fc-00155d3ba208')/Assignments`

Ресурс **ProjectServer** описан в [ProjectServer ресурсы в интерфейсе REST](https://msdn.microsoft.com/library/a490b675-a845-ee94-3877-b99ada9bf2b0%28Office.15%29.aspx#bk_ProjectServerResources). Другие ресурсы REST, описаны в документации для соответствующих объектов JavaScript и его элементы в этой справке. Дополнительные сведения об использовании REST можно [со стороны клиента объектной модели (CSOM) для Project Server](client-side-object-model-csom-for-project-2013.md) , а также [программирование с помощью службы REST для SharePoint 2013](https://msdn.microsoft.com/library/fp142385%28office.15%29.aspx).
  
## <a name="javascript-library-and-rest-reference-for-project-server"></a>Справочник по REST для Project Server и библиотеки JavaScript
<a name="pj15_JavaScriptAPIReference_PS"> </a>

- [Справочник по REST и библиотеку PS.js JavaScript](https://msdn.microsoft.com/library/5a140021-380a-d9e0-e36d-106df85f56d6%28Office.15%29.aspx) Содержит сведения об объектной модели JavaScript и интерфейс REST для Project Server 2013. 
    
## <a name="see-also"></a>См. также
<a name="bk_addresources"> </a>

- [Документация для разработчиков Project 2013](project-2013-developer-documentation.md)   
- [Клиентская объектная модель (CSOM) для Project Server](client-side-object-model-csom-for-project-2013.md)   
- [Начало работы с объектной моделью JavaScript](getting-started-with-the-project-server-2013-javascript-object-model.md)  
- [Работа с проектами с помощью объектной модели JavaScript](create-retrieve-update-delete-projects-using-project-server-javascript.md)
    

