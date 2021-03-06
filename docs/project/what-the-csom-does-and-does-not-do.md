---
title: Какие задачи CSOM выполняет, а какие — нет
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 6828485c-040b-4278-923f-4cc7c8fe0fb1
description: Клиентская объектная модель (CSOM) — это набор API для Project Server 2013, которые разработаны для применения как в Интернете, так и в локальных средах. Они используются в приложениях, разрабатываемых для ПК, мобильных устройств и планшетов. В этой статье описаны типовые сценарии использования CSOM и перечислены характерные для CSOM ограничения.
localization_priority: Priority
ms.openlocfilehash: 6cdcb72c24e352365b6dcc9268ddf0bd249369af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315227"
---
# <a name="what-the-csom-does-and-does-not-do"></a>Какие задачи CSOM выполняет, а какие — нет

Клиентская объектная модель (CSOM) — это набор API для Project Server 2013, которые разработаны для применения как в Интернете, так и в локальных средах. Они используются в приложениях, разрабатываемых для ПК, мобильных устройств и планшетов. В этой статье описаны типовые сценарии использования CSOM и перечислены характерные для CSOM ограничения.
  
|||
|:-----|:-----|
|||
   
CSOM позволяет разрабатывать приложения для Project Server 2013 и интегрировать Project Server c другими приложениями. Приложения можно разрабатывать для ПК, мобильных устройств, например телефонов с Windows Phone 7.5, планшетов, например устройств с Windows 8, а также для устройств с iOS и Android. CSOM предоставляет API, включающие функции 12 чаще всего используемых служб PSI в Project Server. API CSOM упорядочены не так, как службы PSI на основе ASMX и WCF, и их проще использовать, чем эти службы. В CSOM не используются наборы данных ADO.NET, и доступ к ней можно получить по протоколу OData. Вы можете вести разработку с использованием CSOM, применяя библиотеки .NET Framework 4, JavaScript или запросы передачи репрезентативного состояния (REST).
  
Общие сведения о CSOM и перечень статей, в которых рассказывается, как использовать JavaScript и .NET Framework 4 при работе с CSOM, см. в статье [Клиентская объектная модель (CSOM) для Project Server](client-side-object-model-csom-for-project-2013.md). Дополнительные сведения о сборках, классах и элементах CSOM см. в справочнике по пространству имен [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx). 
  
## <a name="usage-scenarios-for-the-csom"></a>Сценарии использования для CSOM
<a name="pj15_WhatTheCSOM_UsageScenarios"> </a>

Ниже приведены примеры приложений, поддерживаемых CSOM. CSOM можно использовать вместо PSI во многих сценариях, например в перечисленных ниже.
  
- **Разработка приложений, расширяющих возможности Project Server.** Основная цель CSOM — разработка приложений для Project Server 2013, в котором можно создавать приложения для самых разных устройств, в том числе ПК, мобильных устройств и планшетов. Приложения можно распространять через частный каталог приложений или через общедоступный Магазин Office. 
    
- **Автоматизация процесса создания объектов в Project Server или управления ими.** CSOM может выполнять операции CRUD для объектов, например проектов, задач, назначений, корпоративных ресурсов, настраиваемых полей, таблиц подстановки, расписаний, обработчиков событий, а также этапов и стадий рабочих процессов. Зачастую пользовательское приложение может сэкономить время при выполнении громоздких или повторяющихся заданий. 
    
- **Получение данных, хранящихся в опубликованных таблицах базы данных Project.** Так как непосредственный доступ к черновым, опубликованным и архивным таблицам базы данных не поддерживается, вы можете использовать CSOM для чтения данных, недоступных в таблицах и представлениях отчетов. Например, таким способом вы можете получать информацию о стадиях, этапах и действиях рабочего процесса. Для чтения данных в таблицах отчетов вы можете использовать запросы OData. 
    
- **Проверка данных отчетов о состоянии и расписаний.** Используйте CSOM в локальных обработчиках событий или удаленных приемниках событий для событий до операций, чтобы проверять состояния назначений или данные расписаний, которые вводят пользователи, перед сохранением этих данных в Project Web App. 
    
- **Создание финансовых проектов.** Создавайте проекты для резервирования времени с помощью расписаний для последующей интеграции с финансовыми системами. Создавайте иерархию финансовых кодов, отражающих структуру детализации затрат финансовой системы. Для финансовых проектов не требуется выполнять планирование или обновлять состояния. 
    
- **Интеграция с системами бухгалтерского учета.** Регистрируйте затраты на ресурсы и расходы, связанные с проектами, и передавайте данные в финансовые системы и системы выставления счетов, а также используйте эти данные для целей сравнения с бюджетом. Синхронизируйте задачи, ресурсы и назначения между системами. Отметьте данные расписания в одной системе для передачи в другую (вопрос о том, какое расписание должно использоваться, зависит от потребностей организации или от индивидуальных проектов). 
    
- **Автоматизация обновлений, получаемых от участников рабочих групп.** При работе с проектами, которые не являются активно управляемыми, вы можете автоматически обновлять проекты на сервере по мере прогресса и внесения изменений в проекты участниками рабочих групп. Проекты можно обновлять и повторно публиковать без участия руководителей проектов, проверяющих результаты или корректирующих планы. 
    
    > [!NOTE]
    > CSOM поддерживает отправку обновлений сведений о состоянии, но на данный момент не поддерживает утверждение состояний. 
  
- **Оценка данных Project Server в удаленных приемниках событий.** Удаленный приемник событий для событий до операций **ProjectCreating** может использовать данные Project Server, получаемые из CSOM, чтобы определять, необходимо ли отменить событие. Например, прежде чем создать проект, можно сравнить предлагаемый проект с существующими проектами. 
    
- **Поддержка декларативных рабочих процессов Project Server.** CSOM позволяет использовать рабочие процессы Project Server, созданные в SharePoint Designer 2013. CSOM поддерживает определения рабочих процессов, в которых используется Windows Workflow Foundation версии 4 (WF4). (PSI не поддерживает рабочие процессы WF4.) 
    
- **Создание сложных рабочих процессов Project Server.** Когда вы разрабатываете рабочие процессы с использованием Visual Studio 2012, вы можете применять CSOM для выполнения сложных действий в рамках стадий рабочих процессов либо для создания дополнительных действий рабочих процессов. 
    
## <a name="what-the-csom-does-not-do"></a>Какие задачи CSOM не выполняет
<a name="pj15_WhatTheCSOM_DoesNotDo"> </a>

CSOM — это не полноценная замена PSI. Так как внутри CSOM используются службы PSI, CSOM присущи многие функциональные ограничения, характерные для PSI. Помимо ограничений, имеющихся в PSI, например отсутствия доступа к данным в локальных проектах (MPP-файлах), CSOM не включает функции администрирования, которые обычно выполняет Project Web App. Например, создание пользовательских групп безопасности можно выполнить на странице "Параметры сайта — Разрешения" для Project Web App. 
  
Список действий, которые не поддерживаются ни в PSI, ни в CSOM, см. в разделе *Какие задачи PSI не выполняет* статьи [Какие задачи PSI выполняет, а какие — нет](what-the-psi-does-and-does-not-do.md).
  
### <a name="psi-services-that-the-csom-does-not-cover"></a>Службы PSI, не охватываемые CSOM
<a name="pj15_WhatTheCSOM_PSIServices"> </a>

CSOM не включает функции указанных ниже служб PSI.
  
- **Служба Admin.** Для управления параметрами администрирования и операциями в Project Server, а также для работы со связанными сайтами проектов, например при создании финансовых периодов и настройке параметров расписаний, используйте методы PSI в классе [WebSvcAdmin.Admin](https://msdn.microsoft.com/library/WebSvcAdmin.Admin.aspx). В Project Web App методы **Admin** используются во многих страницах, связанных со страницей "Параметры сервера" (https://*ИмяСервера*  /  *ИмяProjectServer*  /_layouts/15/pwa/Admin/Admin.aspx). 
    
- **Служба Archive.** Для сохранения объектов, например проектов, ресурсов и настраиваемых полей в архивных таблицах, а также для управления ими используйте методы PSI в классе [Archive](https://msdn.microsoft.com/library/WebSvcArchive.Archive.aspx). 
    
- **Служба CubeAdmin.** Для создания кубов OLAP для локальных установок, а также для управления ими используйте методы PSI в классе [WebSvcCubeAdmin.CubeAdmin](https://msdn.microsoft.com/library/WebSvcCubeAdmin.CubeAdmin.aspx) либо страницу "Управление базой данных OLAP" (https://*ИмяСервера*  /  *ИмяProjectServer*  /_layouts/15/pwa/CubeAdmin/CubeAnalysisAdmin.aspx) в Project Web App. 
    
    > [!NOTE]
    > Project Online не поддерживает кубы OLAP. 
  
- **Служба Driver.** Для создания бизнес-целей для анализа портфолио проектов, а также для управления такими бизнес-целями используйте методы PSI в классе [WebSvcDriver.Driver](https://msdn.microsoft.com/library/WebSvcDriver.Driver.aspx). 
    
- **Службы LoginForms и LoginWindows.** В CSOM проверка подлинности выполняется во время инициализации объекта **ProjectContext** вместе с проверкой подлинности OAuth или Windows. Чтобы создавать приложения для выполнения нескольких видов проверки подлинности, когда локальное приложение с полным доверием может выполнять и проверку подлинности Forms, и проверку подлинности Windows, используйте методы PSI в классах [WebSvcLoginForms.LoginForms](https://msdn.microsoft.com/library/WebSvcLoginForms.LoginForms.aspx) и [WebSvcLoginWindows.LoginWindows](https://msdn.microsoft.com/library/WebSvcLoginWindows.LoginWindows.aspx). 
    
- **Служба Notification.** Для создания предупреждений и напоминаний, а также для управления ими используйте методы PSI в классе [WebSvcNotifications.Notifications](https://msdn.microsoft.com/library/WebSvcNotifications.Notifications.aspx). 
    
- **Служба ObjectLinkProvider.** Для создания веб-объектов и ссылок на документы и элементы списков SharePoint, а также для управления ими используйте методы PSI в классе [WebSvcObjectLinkProvider.ObjectLinkProvider](https://msdn.microsoft.com/library/WebSvcObjectLinkProvider.ObjectLinkProvider.aspx). 
    
- **Служба PortfolioAnalyses.** Для создания операций анализа портфолио проектов, в том числе решений планировщиков и оптимизаторов, и управления ими используйте методы PSI в классе [WebSvcPortfolioAnalyses.PortfolioAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.aspx). 
    
- **Служба QueueSystem.** CSOM может получать базовые сведения о заданиях очереди Project Server и включает метод [ProjectContext.WaitForQueue](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.WaitForQueue.aspx). Для более широкого управления системой очереди в Project Server используйте методы PSI в классе [WebSvcQueueSystem.QueueSystem](https://msdn.microsoft.com/library/WebSvcQueueSystem.QueueSystem.aspx). 
    
- **Служба Security.** Для создания групп безопасности, шаблонов и категорий Project Server, а также для управления ими и проверки разрешений для текущего пользователя используйте методы PSI в классе [WebSvcSecurity.Security](https://msdn.microsoft.com/library/WebSvcSecurity.Security.aspx). 
    
- **Служба WssInterop.** Для получения информации о сайтах проектов и управления ими используйте методы PSI в классе [WebSvcWssInterop.WssInterop](https://msdn.microsoft.com/library/WebSvcWssInterop.WssInterop.aspx). 
    
    > [!NOTE]
    > Вы можете использовать CSOM в SharePoint Server 2013. Сайты проектов — это сайты SharePoint. 
  
CSOM не позволяет использовать расширения, которые, например, можно использовать в PSI. Например, если вы создадите расширение PSI для использования в локальной среде, вам не удастся изменить CSOM так, чтобы использовать расширение PSI. Вы можете реализовать сценарии использования расширений другими указанными ниже способами.
  
- Агрегируйте вызовы CSOM в локальном компоненте или в компоненте, который выполняется в Microsoft Azure.
    
- Используйте запросы OData к данным отчетов вместо того чтобы напрямую обращаться к таблицам отчетов в базе данных Project Server.
    
- Интегрируйте вызовы CSOM со сторонними приложениями с помощью функции проверки подлинности OAuth в Project Online или с помощью серверных компонентов для использования в локальной среде.
    
- Приложения, в которых применяется CSOM, могут также использовать пользовательские базы данных как в локальной среде, так и с применением SQL Azure.
    
### <a name="request-limits-of-the-csom"></a>Ограничения для запросов в CSOM
<a name="pj15_WhatTheCSOM_RequestLimits"> </a>

CSOM в Project Server 2013 создана на основе реализации CSOM в SharePoint Server 2013 и в ней унаследованы ограничения на максимальный размер запроса. В SharePoint имеется ограничение в 2 МБ для запросов на выполнение операций и ограничение в 50 МБ на размер передаваемых двоичных объектов. Размер запроса ограничен, чтобы не допустить появления чрезмерно длинных очередей операций на сервере и избежать задержек, возникающих при обработке больших двоичных объектов.
  
Например, если вы создаете проект с помощью CSOM, а затем изменяете проект и добавляете в него 252 задачи с минимальным объемом информации, например с коротким именем, GUID задачи и длительностью 1d, общий объем данных в запросе **DraftProject.Update** будет меньше 2 МБ. Но если вы попытаетесь добавить 253 таких задачи в пустой проект, ограничение в 2 Мб будет превышено и возникнет следующее исключение: **Microsoft.SharePoint.Client.ServerException: запрос использует слишком много ресурсов**.
  
Для сбора данных в запросе CSOM по протоколу HTTP или HTTPS вы можете использовать средство веб-отладки, например [Fiddler](https://www.fiddler2.com) (https://www.fiddler2.com). Пример кода, в котором реализован тест на размер запроса и который включает решение, разбивающее большой запрос на маленькие группы, см. в статье [DraftProject.Update](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.DraftProject.Update.aspx) . 
  
## <a name="see-also"></a>См. также
<a name="pj15_WhatTheCSOM_AR"> </a>

- [Клиентская объектная модель (CSOM) для Project Server](client-side-object-model-csom-for-project-2013.md)
    
- [Какие задачи PSI выполняет, а какие — нет](what-the-psi-does-and-does-not-do.md)
    
- [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)
    

