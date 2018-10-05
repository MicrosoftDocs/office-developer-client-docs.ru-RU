---
title: Какие задачи PSI выполняет, а какие — нет
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eac6be6a-9a20-4bc0-8da2-b2fd93aab04f
description: Интерфейс Project Server (PSI) помогает автоматизировать много процессов на сервере в локальной установки Project Server 2013. Однако несколько функций необходимо использовать Microsoft Project профессиональный 2013.
ms.openlocfilehash: b93c3535ca6693a84d11370de17bc18375f168ab
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386343"
---
# <a name="what-the-psi-does-and-does-not-do"></a>Какие задачи PSI выполняет, а какие — нет

Интерфейс Project Server (PSI) помогает автоматизировать много процессов на сервере в локальной установки Project Server 2013. Однако несколько функций необходимо использовать Microsoft Project профессиональный 2013.
  
|||
|:-----|:-----|
|||
   
Предоставляет интерфейс PSI дополняющих набор возможностей Project Professional 2013, а не предоставляют альтернатива на стороне сервера для всех функций Project профессиональный. Сторонние разработчики можно использовать для создания веб-частей для локальных установок Project Web App и рабочие области проектов, создания пользовательских приложений и веб-приложений, которые взаимодействуют с данными Project Server в локальной, Разработка рабочего процесса PSI (en) логика для управления портфелем проектов разработки обработчиков событий локального с полным доверием и интеграции Project Server с другими приложениями. PSI не может использоваться для разработки приложений для магазина Office, мобильных устройств и планшетных компьютеров; для этого можно использовать клиентскую объектную модель (CSOM).
  
> [!NOTE]
> PSI содержит более подробные программный интерфейс для Project Server 2013 не предоставляет CSOM. Однако если CSOM не предоставляет функциональные возможности, которые могут потребоваться, мы рекомендуем использовать CSOM для разработки новых приложений. Для получения дополнительных сведений см [CSOM что делает и действия не выполняются](what-the-csom-does-and-does-not-do.md). 
  
## <a name="usage-scenarios-for-the-psi"></a>Сценарии использования для PSI (en)
<a name="pj14_WhatPSIDoes_UsageScenarios"> </a>

Ниже приведены примеры некоторых приложений, которые поддерживает PSI для проектов на сервере и вычисления:
  
- **Автоматизация создания или управления сущностей в Project Server** Хотя Project Professional 2013 и Project Web App вместе предназначены для обработки управление и создание сущностей, таких как проекты, корпоративные ресурсы и настраиваемые поля, часто имеется случаев настраиваемого приложения можно использовать для размещения времени с неполным или повторяющиеся задания. PSI можно автоматизировать несколько типов заданий, которые не CSOM, например, с помощью кубов OLAP, анализа портфеля проектов, бизнес-факторов, уведомления, объект ссылку поставщики, безопасности и взаимодействие с SharePoint. 
    
- **Получение данных в опубликованной или таблицы архива базы данных Project** Так как прямой базы данных, доступ к черновиков, опубликованных проектов и архивировать таблицы не поддерживается, PSI можно использовать для считывания данных, недоступны в отчетности таблицы или представления. Например, получение сведений о версии project, дат и изменения, которые хранятся в таблицах архив и заполните управления JS Grid в веб-части с данными. 
    
- **Проверять данные на отчеты о состоянии и расписаний** Используйте PSI в локальном обработчиков события до операции для проверки назначения состояние "или" расписание данных, вводимых пользователями, перед сохранением данных в Project Web App. 
    
- **Проектов обслуживания.** Создание заполнитель проектов для использования с планов ресурсов. Резервирование или книга время, по ресурсы для работ по обслуживанию или базовый бизнес. Проекты обслуживания обычно нет задач. 
    
- **Создать финансовые проекты** Создание проектов для захвата времени через табеля учета рабочего времени для интеграции с финансовой системы. Создание иерархии финансовые коды, чтобы отразить структуры декомпозиции стоимость финансовой системы. Финансовые проекты не требуют планирования и состояние обновления. 
    
- **Интеграция с системами бухгалтерского учета.** Запись ресурса затраты и расходы, связанные с проектами для веб-канала системы финансовые и выставления счетов и для сравнения бюджета. Синхронизация задач, ресурсов и назначений между системами. Запись данных табеля учета рабочего времени в одной системе для веб-канала другое (какие расписания используется зависит от потребностей организации или отдельных проектов). 
    
- **Автоматизация обновлений от участников группы** Для проектов, которые не управляются активно автоматически обновите проекты на сервере с помощью хода выполнения и другие изменения членов группы проекта. Проекты можно обновить и повторной публикации без руководителя проектов с помощью изучения результатов и выполнение корректировок в план. 
    
- **Оценка Project Server данных в обработчиках событий локального с полным доверием** Локальный обработчик для события до операции **ProjectCreating** можно использовать данные Project Server из PSI можно определить, следует ли отменить событие. Например перед созданием проекта, сравните предложения проекта с существующими проектами. 
    
- **Создать настраиваемые действия рабочего процесса для управления запросами** Используйте PSI в действия рабочего процесса локального, с полным доверием для изменения и обновить корпоративных шаблонов проектов на основе предложений по проекту. Используйте настраиваемые поля проекта, чтобы пометить проекта с информацию, необходимую для запуска и процессам утверждения. Добавление задач для идентификации этапов проекта для этапы или конечные результаты. После утверждения предложений по проекту рабочего процесса можно изменить предложений в полномасштабное проекты, которые управляются с помощью Project Professional. 
    
- **Создание PSI расширений** (**Устаревшие.** Расширения поддерживаются в Project Server 2013 и не будет поддерживаться в будущих выпусках.) PSI могут быть расширены с помощью пользовательских служб с помощью интерфейса Windows Communication Foundation (WCF). Расширения PSI выполните на сервере Project Server и можно использовать встроенные службы PSI используют инфраструктуру безопасности. Расширения можно запрашивать отчетов таблицы, используйте таблицу отдельной базе данных, консолидировать вызовов PSI для сохранения пропускной способности и интеграции с приложениями сторонних производителей и других компонентов на сервере. Дополнительные сведения см в [Разработке расширения PSI](https://msdn.microsoft.com/library/1b484623-94fb-47c9-84c1-3e68a9133042%28Office.15%29.aspx).
    
- **Использование олицетворения в локальных приложениях с полным доверием** Вызовы интерфейса PSI WCF могут иметь олицетворение, таким образом, чтобы приложение предполагает настройки безопасности для олицетворения пользователя. Олицетворение можно использовать только в случае необходимости и точно. Чтение и обновление сведения о состоянии для других пользователей не требует олицетворения. Новые приложения, которые требуют олицетворения должны использовать протокол OAuth и CSOM вместо PSI. Дополнительные сведения о олицетворения с помощью PSI содержатся в разделе [Использование олицетворения с WCF](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx).
    
> [!NOTE]
> В некоторых случаях можно использовать PSI в клиентских приложениях с помощью CSOM и Project Online. При использовании на веб-службы на основе ASMX PSI приложения необходимо включить метод проверки подлинности объекта [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) в CSOM и метод проверки подлинности ** System.Web.Services.Protocols.SoapHttpClientProtocol** клиентского объекта. Например, использующего веб-службы с помощью SharePoint CSOM видеть [Удаленной проверки подлинности в SharePoint Online Using Claims-Based проверки подлинности](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx). > Из-за ограниченного разрешения на уровне приложения PSI не может использоваться в приложениях, которые предназначены для рассылки в общедоступном магазине Office. В этом случае можно использовать только CSOM. 
  
## <a name="what-the-psi-does-not-do"></a>Что делать PSI (en)
<a name="pj14_WhatPSIDoes_DoesNotDo"> </a>

Хотя существует множество элементов, которое можно выполнить PSI, существует несколько действий, которые не PSI. Ниже приведены две вещи PSI не может делать, но можно сделать CSOM.
  
### <a name="project-online-and-remote-event-receivers"></a>Project Online и удаленных приемников событий

Основным ограничением PSI — с Project Online. Приложения, использующие PSI требуют с полным доверием доступ к экземпляру локального сервера Project Server. Например, PSI не могут использоваться в удаленных приемников событий, где установлена приемника событий, как службы в Microsoft Azure.
  
### <a name="workflows-and-claims-authentication"></a>Рабочие процессы и утверждения проверки подлинности

Определение рабочего процесса, который использует Windows Workflow Foundation версии 4 (WF4) требует проверки подлинности утверждений, которое PSI не поддерживается напрямую. Это означает, что PSI нельзя использовать для создания проекта в Project Server 2013, которое имеет тип корпоративного проекта (типа корпоративного проекта) с помощью определения рабочего процесса WF4.
  
PSI можно использовать для создания проектов с EPTs, либо нет рабочего процесса или использовать определение WF3.5 (версия рабочего процесса в Project Server 2010). Создание проекта с помощью типа корпоративного проекта, который имеет определение WF4, используется CSOM.
  
 **Действия, которые требуют Project Professional:**
  
Следующий список, вещей, которые можно выполнять ни PSI, ни CSOM.
  
#### <a name="local-data"></a>Локальные данные

- Работа с данными в локальных проектов (MPP-файлы). Например определение таблицы норм затрат или профили доступности для локальных ресурсов. 
    
- Определение или изменение локальных базовых календарей и календарей ресурсов, включая исключения календарей.
    
- Определение локальных настраиваемых полей. (PSI поддерживает редактирование значения локальных настраиваемых полей для задач, ресурсов и назначений.)
    
#### <a name="enterprise-data"></a>Корпоративные данные

- Извлечение или редактирования глобальный корпоративный шаблон. Глобальных данных предприятия в Project Server 2013 — это набор двоичных данных таблиц в базе данных Project, не шаблон проекта как и в Office Project Server 2007 и более ранних версий.
    
- Определение или изменение корпоративные календари. Методы [календаря](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) для управления только исключения календарей. 
    
#### <a name="master-projects-and-cross-project-links"></a>Главные проекты и перекрестных связей между проектами

- Создание главных проектов и вставка подпроекты.
    
- Планирование критический путь между главный проект. 
    
- Создание связей между проектами.
    
#### <a name="resources"></a>Resources

- Для запроса или выполнения выравнивание загрузки ресурсов.
    
- Изменение ресурса по назначению. (PSI можно использовать для удаления назначения и создайте новый.)
    
- Удаление или замена ресурс, который содержит фактические трудозатраты принят (фактические данные).
    
- Изменение типа ресурсов между работой, материалов и затраты.
    
- Создание или редактирование календарей ресурсов.
    
- При добавлении ресурса задаче, PSI не распространять автоматически работают так, как Project Professional. Это разработчик должен выбрать и явно задать распределение работы для назначений.
    
#### <a name="cost-resources"></a>Затратные ресурсы

- Изменение, создание или удаление ресурсов и назначений с помощью методов [проекта](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) . Методы [ресурсов](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) можно создать ресурсов, но не могут изменять их. 
    
#### <a name="work-contours"></a>Профили загрузки

- Изменение повременных данных.
    
    > [!NOTE]
    > После того как руководитель проекта обновляется и публикует данные назначения [UpdateStatus](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.UpdateStatus.aspx) метода в веб-службы **состояний** можно изменить повременные фактические данные для назначений. 
  
- Задание или изменение назначения составить профиль типа (например, плоский загрузки или профилем).
    
#### <a name="baselines-and-earned-value"></a>Исходных значений и освоенного объема

- Сохранение базового плана или изменении базовые данные. 
    
- Установка даты хода выполнения.
    
- Подсчет отклонение и освоенного объема. 
    
#### <a name="interactive-scheduling"></a>Интерактивные планирования

- Поддержка интерактивного планирования. (Так как Project Server обрабатывает взаимодействия асинхронно, интерактивных планирования должны выполняться с Project профессиональный.)
    
    > [!NOTE]
    > Чтобы избежать изменения программный поведения, PSI методов, которые добавлены прямого из Project Server 2010 действовать так же, как в Project Server 2013. Например [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) по-прежнему действуют те же ограничения и использует старые механизм планирования на сервере. Новый метод [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) удаляет многие из этих ограничений и использует новый Project Server 2013 на сервере механизм планирования, который является же механизм планирования в Project Professional 2013. 
  
#### <a name="wbs"></a>WBS

- Определение маски кода структуры (WBS) декомпозиции работы. 
    
#### <a name="tasks"></a>Задачи

- Изменение типа задачи (фиксированные трудозатраты, длительность и единицы).
    
- Изменение задачи фиксированный объем работ.
    
- Изменение начисления фиксированные затраты для задачи.
    
- Изменение содержимого в поле [TASK_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NOTES.aspx) . PSI могут читать только часть текста заметок задачи, которые являются .rtf двоичных данных. Однако можно изменить заметки назначения ( [ASSN_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.AssignmentRow.ASSN_NOTES.aspx) ), которые являются текстовые данные. База данных отчетов не включает заметки задачи или назначения. 
    
- Создание или редактирование повторяющиеся задачи.
    
- Назначение или изменение календаря задачи на существующие задачи.
    
- Создание новой задачи с помощью календаря задачи.
    
- При изменении значения поля [TASK_IGNORES_RES_CAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IGNORES_RES_CAL.aspx) (задача игнорирует календаря ресурса). 
    
- Изменение активных состояние задачи с помощью [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) , если были внесены дополнительные изменения в одном вызове. Для получения дополнительных сведений обратитесь к разделу *Планирование проектов на сервере* с возможностями [программирования Project Server](project-server-programmability.md).
    
#### <a name="summary-tasks"></a>Суммарные задачи

- Создание или изменение назначений на суммарные задачи.
    
    > [!NOTE]
    > Рекомендуется не вносить назначений на суммарные задачи с помощью Project Professional или другим способом. Для получения дополнительных сведений обратитесь к разделу *Планирование проектов на сервере* с возможностями [программирования Project Server](project-server-programmability.md). 
  
- Изменение поля суммарной задачи, которые обычно суммируются из подзадач. Проекты на сервере всегда выполнять сведение Сводная информация, а не данные параметров для суммарной задачи и передача вниз до подзадачи. Можно изменить только следующие поля в суммарной задачи:
    
  - Зависимости задач
    
  - Формула не настраиваемые поля
    
  - [TASK_NAME](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NAME.aspx)
    
  - [TASK_OUTLINE_LEVEL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_OUTLINE_LEVEL.aspx)
    
  - [TASK_IS_MARKED](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IS_MARKED.aspx)
    
  - [ПОЛЕ TASK_CONSTRAINT_TYPE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_TYPE.aspx)
    
  - [TASK_CONSTRAINT_DATE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_DATE.aspx)
    
  - [TASK_PRIORITY](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_PRIORITY.aspx)
    
  - [TASK_DEADLINE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_DEADLINE.aspx)
    
  - [TASK_FIXED_COST](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST.aspx)
    
  - [TASK_FIXED_COST_ACCRUAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST_ACCRUAL.aspx) (присвоено значение только при создании задания) 
    
  - [TASK_WBS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_WBS.aspx)
    
Для суммарной задачи проекта ограничения PSI совпадают с требованиями для Project Professional. PSI можно изменить назначения бюджета — включая бюджетов затрат.
  
#### <a name="project-level-calculation-options"></a>Параметры расчета на уровне проекта

- Изменение типа проекта между расписания из запуск (SFS) и расписание из Готово (SFF). (Можно создать проект, как SFS или SFF PSI, но после создания его можно изменить только в Project Professional.)
    
- Изменение базового календаря проекта ([CAL_UID](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.CAL_UID.aspx) ) после создания проекта. 
    
- Изменение параметров для вычисления. Чтобы задать следующие параметры расчета при создании проекта, но для изменения параметров необходимо Project Professional можно использовать PSI. (В представлении Backstage, выберите пункт **Параметры**и затем откройте вкладку **расписание** в диалоговом окне **Параметры проекта** .) 
    
  - [PROJ_OPT_CALC_ACT_COSTS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_CALC_ACT_COSTS.aspx)
    
  - [PROJ_OPT_CRITICAL_SLACK_LIMIT](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_CRITICAL_SLACK_LIMIT.aspx)
    
  - [PROJ_OPT_HONOR_CONSTRAINTS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_HONOR_CONSTRAINTS.aspx)
    
  - [PROJ_OPT_MOVE_ACTUAL_IF_LATER](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_ACTUAL_IF_LATER.aspx)
    
  - [PROJ_OPT_MOVE_ACTUAL_TO_STATUS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_ACTUAL_TO_STATUS.aspx)
    
  - [PROJ_OPT_MOVE_REMAINING_IF_EARLIER](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_REMAINING_IF_EARLIER.aspx)
    
  - [PROJ_OPT_MOVE_REMAINING_TO_STATUS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MOVE_REMAINING_TO_STATUS.aspx)
    
  - [PROJ_OPT_MULT_CRITICAL_PATHS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_MULT_CRITICAL_PATHS.aspx)
    
  - [PROJ_OPT_SPLIT_IN_PROGRESS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPLIT_IN_PROGRESS.aspx)
    
  - [PROJ_OPT_SPREAD_ACT_COSTS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPREAD_ACT_COSTS.aspx)
    
  - [PROJ_OPT_SPREAD_PCT_COMP](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_SPREAD_PCT_COMP.aspx)
    
  - [PROJ_OPT_TASK_UPDATES_RES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.PROJ_OPT_TASK_UPDATES_RES.aspx)
    
## <a name="see-also"></a>См. также

- [Какие задачи CSOM выполняет, а какие — нет](what-the-csom-does-and-does-not-do.md)  
- [Возможности программирования для Project Server](project-server-programmability.md)   
- [Удаленная проверка подлинности в SharePoint Online с использованием проверки подлинности на основе утверждений](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx)  
- [Надстройки Office](https://docs.microsoft.com/office/dev/add-ins/overview/office-add-ins) 
    

