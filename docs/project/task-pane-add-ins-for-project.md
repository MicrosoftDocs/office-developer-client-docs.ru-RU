---
title: Надстройки области задач для Project
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 44712b7c-aead-433d-8c0e-76407264166c
description: Project Стандартный 2013 и Project Professional 2013 поддерживают области задач Office Add-ins. Использовать надстройки для области задач можно интегрировать project, задач, ресурсов и просмотр данных с других клиентских приложениях Office 2013, приложения SharePoint, веб-частей, других веб-страниц и внешних данных в проекте.
ms.openlocfilehash: 26942cab1d1b127872a230a46fbc6242ab27b754
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396017"
---
# <a name="task-pane-add-ins-for-project"></a>Надстройки области задач для Project

Project Стандартный 2013 и Project Professional 2013 поддерживают области задач Office Add-ins. Использовать надстройки для области задач можно интегрировать project, задач, ресурсов и просмотр данных с других клиентских приложениях Office 2013, приложения SharePoint, веб-частей, других веб-страниц и внешних данных в проекте.
  
Надстройки Office — это модель расширения, поддерживаемые в нескольких клиентских приложений Office 2013. Платформа полное надстройка содержит контекстную, контента и типов надстройки области задач. Outlook 2013 поддерживает почты надстройки, которые может отобразить веб-страницы в сообщении электронной почты или встречи элемента календаря, которая относится к содержимому в элементе. Excel 2013 и Word 2013 поддерживает контента надстройки, которые можно отобразить веб-страницы как внедренного содержимого в документе. Word 2013, Excel 2013 и Project Professional 2013 поддерживает задач области надстройки, которые можно показать веб-страницы в приложении области задач, где контент связан с контекстной информации в рамках проекта.
  
Например надстройки Project можно сведение данных в активном проекте и Показать дополнительные данные о выбранной задачи или ресурса. Связанные данные в надстройки могут поступать из внешнего источника, например списка SharePoint, отчетов таблиц в базе данных Project Server, веб-службы или другого приложения предприятия. Задача области надстройки с может быть разработан с HTML 5, JavaScript, JQuery и другие библиотеки JavaScript. Задача области надстройки с не поддерживает непосредственно ActiveX, Silverlight или флэш-компонентов. Несмотря на то, что надстройка Office может использовать элемент **IFrame** для доступа на сервере веб-приложения, использующего ASP.NET и .NET Framework 4.5 библиотеки, такого рода решения не рекомендуется или не поддерживается. Надстройка может быть разработан для сохранения данных локально или записи данных на внешний носитель. 
  
> [!NOTE]
> Область задач проекта надстройки могут доступ к данным из Project Online с использованием проверки подлинности OAuth. С помощью Project Professional 2013 можно разрабатывать задач области надстроек, которые обращаются оба локальных установок Project Server 2013 и в локальной или online SharePoint 2013. Например см [подключение области задач проекта надстройки для веб-клиента Project](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx) в блоге Programmibility проекта. > Project стандартный 2013 не поддерживает прямую интеграцию с данными Project Server или списками задач SharePoint, синхронизированными с Project Server. 
  
Дополнительные сведения о надстройках для Office 2013 можно [Office и SharePoint надстройки](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29). 
  
## <a name="developing-task-pane-add-ins"></a>Разработка надстроек для области задач

Документация разработчика для Office и SharePoint надстройки включает в себя подробные статьи и справочные материалы. Общие сведения о разработке надстроек для Project Professional 2013 и другие клиентские приложения Office 2013 и справочник по JavaScript и ссылку на манифест XML в разделе [надстроек Office](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29).
  
Загрузить пакет SDK Project 2013 включает в себя **Project OM Test** образец надстройки, показано, как получить идентификатор GUID для задач, ресурсов и представления, как получение свойств активного проекта и установке задач, ресурсов, или просмотреть обработчик события изменения выбора. Если извлечь и установить пакет SDK и примеры, в файле Project2013SDK.msi видеть `\Samples\Apps\Copy_to_AppSource_FileShare` подкаталог и `\Samples\Apps\Copy_to_AppManifests_FileShare` подкаталог. В примере JSOMCall.html используются функции JavaScript в файл office.js и project-15.js, которые включены в файл для загрузки. Вы можете изучать функции, используя соответствующие файлы отладки (office.debug.js и project-15.debug.js). 
  
**HelloProject_OData** пример надстройки Project Professional 2013 был разработан с помощью Visual Studio 2012. Надстройка использует запрос REST из службы **ProjectData** для получения отчетов данные для затрат на проект и другие сведения, а затем сравнивает текущего проекта со средние значения для всех проектов в Project Web App. 
  
## <a name="see-also"></a>См. также
<a name="bk_addresources"> </a>

- [Надстройки области задач для Project](https://msdn.microsoft.com/library/office/apps/fp161143%28v=office.15%29)
    
- [Подключение надстройки области задач Project к веб-клиента Project](https://blogs.msdn.com/b/project_programmability/archive/2012/11/02/connecting-a-project-task-pane-app-to-pwa.aspx)
    
- [Загрузка пакета SDK для Project 2013](https://www.microsoft.com/en-us/download/details.aspx?id=30435%20)
    
- [Надстройки Office и SharePoint](https://msdn.microsoft.com/library/office/fp161507%28v=office.15%29)
    
- [Надстройки Office](https://msdn.microsoft.com/library/office/apps/jj220060%28v=office.15%29)
    

