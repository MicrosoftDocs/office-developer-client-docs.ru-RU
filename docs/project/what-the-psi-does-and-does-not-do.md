---
title: Какие задачи PSI выполняет, а какие — нет
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eac6be6a-9a20-4bc0-8da2-b2fd93aab04f
description: Интерфейс Project Server (PSI) может помочь автоматизировать многие серверные процессы в локальной установке Project Server 2013. Однако некоторые функции требуют использования Microsoft Project профессиональный 2013.
ms.openlocfilehash: b93c3535ca6693a84d11370de17bc18375f168ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346531"
---
# <a name="what-the-psi-does-and-does-not-do"></a>Какие задачи PSI выполняет, а какие — нет

Интерфейс Project Server (PSI) может помочь автоматизировать многие серверные процессы в локальной установке Project Server 2013. Однако некоторые функции требуют использования Microsoft Project профессиональный 2013.
  
|||
|:-----|:-----|
|||
   
PSI разработан в дополнение к возможностям Project профессиональный 2013, а не предоставляет серверную альтернативу для всех функций Project профессиональный. Сторонние разработчики могут использовать PSI для создания веб-части для локальных установок рабочих пространств Project Web App и проектов, создания пользовательских приложений Для Windows и веб-приложений, взаимодействующих с локальными данными Project Server, разработки логики рабочих процессов для управления портфелями проектов, разработки локальных обработчиков событий с полным доверием и интеграции Project Server с другими приложениями. PSI нельзя использовать для разработки приложений для Магазина Office, мобильных устройств или планшетов; для этого можно использовать клиентскую объектную модель (CSOM).
  
> [!NOTE]
> PSI предоставляет более комплексный программный интерфейс для Project Server 2013, чем CSOM. Но если CSOM не предоставляет требуемую функциональность, рекомендуется использовать CSOM для разработки новых приложений. Дополнительные сведения см. в сведениях о том, что [CSOM делает, а какие нет.](what-the-csom-does-and-does-not-do.md) 
  
## <a name="usage-scenarios-for-the-psi"></a>Сценарии использования для PSI
<a name="pj14_WhatPSIDoes_UsageScenarios"> </a>

Ниже примеры некоторых приложений, поддерживаемые PSI для проектов и вычислений на стороне сервера.
  
- **Автоматизация создания или управления сущностями в Project Server** Хотя Project профессиональный 2013 и Project Web App вместе предназначены для управления и создания сущностями, такими как проекты, корпоративные ресурсы и настраиваемые поля, в некоторых случаях настраиваемые приложения могут сэкономить время с помощью массовых или повторяющихся заданий. PSI может автоматизировать несколько видов заданий, которые CSOM не делает, например, с помощью кубов OLAP, анализа портфеля проектов, бизнес-драйверов, уведомлений, поставщиков ссылок на объекты, безопасности и обеспечения связи SharePoint. 
    
- **Получить данные в опубликованных или архивных таблицах базы данных Project** Поскольку прямой доступ к базам данных к таблицам черновиков, опубликованных и архивных таблиц не поддерживается, PSI можно использовать для чтения данных, недоступных в таблицах или представлениях отчетов. Например, получите сведения о версиях проекта, датах и изменениях, хранимых в архивных таблицах, а затем заполните сведениями в веб-части с помощью сетки JS. 
    
- **Проверка данных о состоянии и времени** Используйте PSI в локальных обработчиках перед событиями для проверки состояния назначения или данных о времени, которые вводит пользователь, перед тем как данные будут сохранены в Project Web App. 
    
- **Проекты по обслуживанию** Создайте проекты-заполнители для использования с планами ресурсов. Зарезервируйте время и ресурсы для работ по обслуживанию или основного бизнеса. В проектах по обслуживанию задачи обычно не используются. 
    
- **Создание финансовых проектов.** Создавайте проекты для резервирования времени с помощью расписаний для последующей интеграции с финансовыми системами. Создавайте иерархию финансовых кодов, отражающих структуру детализации затрат финансовой системы. Для финансовых проектов не требуется выполнять планирование или обновлять состояния. 
    
- **Интеграция с системами бухгалтерского учета.** Регистрируйте затраты на ресурсы и расходы, связанные с проектами, и передавайте данные в финансовые системы и системы выставления счетов, а также используйте эти данные для целей сравнения с бюджетом. Синхронизируйте задачи, ресурсы и назначения между системами. Отметьте данные расписания в одной системе для передачи в другую (вопрос о том, какое расписание должно использоваться, зависит от потребностей организации или от индивидуальных проектов). 
    
- **Автоматизация обновлений, получаемых от участников рабочих групп.** При работе с проектами, которые не являются активно управляемыми, вы можете автоматически обновлять проекты на сервере по мере прогресса и внесения изменений в проекты участниками рабочих групп. Проекты можно обновлять и повторно публиковать без участия руководителей проектов, проверяющих результаты или корректирующих планы. 
    
- **Оценка данных Project Server в локальных обработчиках** событий с полным доверием Локальный обработец событий для предварительного события **ProjectCreating** может использовать данные Project Server из PSI, чтобы определить, следует ли отменить событие. Например, прежде чем создать проект, можно сравнить предлагаемый проект с существующими проектами. 
    
- **Создание настраиваемой деятельности рабочего процесса для управления запросами** Используйте PSI в локальных действиях рабочего процесса с полным доверием для изменения и обновления предложений проектов на основе шаблонов корпоративных проектов. Используйте настраиваемые поля проекта, чтобы пометить проект сведениями, необходимыми для процесса инициации и утверждения. Добавьте задачи по определению этапов проекта, основных вех и конечных результатов. При одобрении предложений по проекту рабочий процесс может изменить предложения на полномасштабные проекты, управляемые с помощью Project профессиональный. 
    
- **Создание расширений PSI** (**неподготовлено.** Расширения не поддерживаются в Project Server 2013 и не будут поддерживаться в будущих выпусках.) PSI можно расширить с помощью пользовательских служб с помощью интерфейса Windows Communication Foundation (WCF). Расширения PSI работают на компьютере Project Server и могут использовать ту же инфраструктуру безопасности, что и встроенные службы PSI. Расширения могут запрашивать таблицы отчетов, использовать отдельные таблицы баз данных, консолидировать вызовы PSI для экономии пропускной способности и интегрировать их со сторонними приложениями и другими серверными компонентами. Дополнительные сведения [см. в подстройки "Разработка расширений PSI".](https://msdn.microsoft.com/library/1b484623-94fb-47c9-84c1-3e68a9133042%28Office.15%29.aspx)
    
- **Использование обезличения в локальных приложениях** с полным доверием Вызовы интерфейса WCF интерфейса PSI можно использовать для того, чтобы приложение было предполагать разрешения безопасности для этого пользователя. Следует использовать обезличение с осторожностью и осторожностью. Для чтения и обновления сведений о состоянии для других пользователей не требуется подавляция. В новых приложениях, которые требуют применения под себя, вместо PSI следует использовать протоколЫ CSOM и OAuth. Дополнительные сведения о подлияниях с помощью PSI см. в поднаступе [с WCF.](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
    
> [!NOTE]
> В некоторых случаях PSI можно использовать в клиентских приложениях с CSOM и Project Online. При использовании веб-службы PSI на основе ASMX приложение должно включать метод проверки подлинности объекта [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) в CSOM и метод проверки подлинности клиентского объекта **System.Web.Services.Protocols.SoapHttpClientProtocol.** Пример использования веб-службы с CSOM SharePoint см. в примере удаленной проверки подлинности в SharePoint Online с использованием проверки подлинности на основе [утверждений.](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx) > из-за ограниченных разрешений на уровне приложения PSI нельзя использовать в приложениях, предназначенных для распространения в общедоступных Магазинах Office. В этом случае можно использовать только CSOM. 
  
## <a name="what-the-psi-does-not-do"></a>Чего не делает PSI
<a name="pj14_WhatPSIDoes_DoesNotDo"> </a>

Несмотря на то, что PSI может делать много вещей, PSI не делает некоторые из них. Ниже 2 вещи, которые PSI не может сделать, но CSOM может сделать.
  
### <a name="project-online-and-remote-event-receivers"></a>Project Online и удаленные приемники событий

Основное ограничение PSI — Project Online. Приложениям, которые используют PSI, требуется доступ с полным доверием к локальной установке Project Server. Например, PSI нельзя использовать в удаленных приемниках событий, где приемник событий устанавливается как служба в Microsoft Azure.
  
### <a name="workflows-and-claims-authentication"></a>Рабочий процесс и проверка подлинности на утверждениях

Определение рабочего процесса, использующее Windows Workflow Foundation версии 4 (WF4), требует проверки подлинности на основе утверждений, которую PSI не поддерживает напрямую. Это означает, что вы не можете использовать PSI для создания проекта в Project Server 2013 с типом корпоративного проекта (EPT) с определением рабочего процесса WF4.
  
PSI можно использовать для создания проектов с epts, которые либо не имеют рабочего процесса, либо используют устаревшее определение WF3.5 (версия рабочего процесса в Project Server 2010). Чтобы создать проект с EPT с определением WF4, используйте CSOM.
  
 **Действия, для работы с project профессиональный:**
  
Ниже приводится список вещей, которые не могут делать ни PSI, ни CSOM.
  
#### <a name="local-data"></a>Локальные данные

- Управление данными в локальных проектах (MPP-файлы). Например, определение таблиц тарифов или контуров доступности для локальных ресурсов. 
    
- Определение или изменение локальных базовых календарей или календарей ресурсов, включая исключения календаря.
    
- Определение локальных настраиваемые поля. (PSI поддерживает редактирование значений локальных настраиваемых полей для задач, ресурсов и назначений.)
    
#### <a name="enterprise-data"></a>Корпоративные данные

- Проверка или изменение глобального корпоративного шаблона. Глобальные корпоративные данные в Project Server 2013 — это набор таблиц двоичных данных в базе данных Project, а не шаблон проекта, как в Office Project Server 2007 и более ранних версиях.
    
- Определение или изменение корпоративных календарей. Методы [Calendar](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) управляют только исключениями календаря. 
    
#### <a name="master-projects-and-cross-project-links"></a>Master projects and cross-project links

- Создание крупных проектов и вставка подпроектов.
    
- Планирование критического пути в рамках проекта. 
    
- Создание межпроектных ссылок.
    
#### <a name="resources"></a>Ресурсы

- Запрос или выполнение выравнивания ресурсов.
    
- Изменение ресурса в назначении. (С помощью PSI можно удалить назначение и создать новое.)
    
- Удаление или замена ресурса с фактическими принятыми трудоемкими ресурсами (фактическими).
    
- Изменение типа ресурса между работой, материалами и затратами.
    
- Создание или редактирование календарей ресурсов.
    
- При добавлении ресурса в задачу PSI не перераспределяет работу автоматически так же, как Project профессиональный. Разработчик может выбрать и явно настроить распределение работы для назначений.
    
#### <a name="cost-resources"></a>Затратные ресурсы 

- Редактирование, создание или удаление затратных ресурсов и назначений с помощью [методов Project.](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) Методы [Resource](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) могут создавать затратные ресурсы, но не могут изменять их. 
    
#### <a name="work-contours"></a>Контуры работы

- Изменение данных с по времени.
    
    > [!NOTE]
    > Метод [UpdateStatus](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.UpdateStatus.aspx) в  веб-службе состояния может изменять периодичное фактическое время для назначений после обновления и публикации данных назначения руководителем проекта. 
  
- Установка или изменение типа контура назначения (например, плоский, загруженный назад или при передней загрузке).
    
#### <a name="baselines-and-earned-value"></a>Базовые показатели и заработано значение

- Сохранение базовых параметров или изменение базовых данных. 
    
- Установка даты выполнения.
    
- Вычисление дисперсии и значения. 
    
#### <a name="interactive-scheduling"></a>Интерактивное планирование

- Поддержка интерактивного планирования. (Так как Project Server асинхронно обрабатывает взаимодействия, интерактивное планирование следует делать с помощью Project профессиональный.)
    
    > [!NOTE]
    > Чтобы избежать изменения программного поведения, методы PSI, которые были доставлены из Project Server 2010, действуют одинаково в Project Server 2013. Например, [queueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) по-прежнему имеет те же ограничения и использует старый механизм планирования на стороне сервера. Новый метод [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) снимает многие из этих ограничений и использует новый механизм планирования на стороне сервера Project Server 2013, который является тем же механизмом планирования, что и в Project профессиональный 2013. 
  
#### <a name="wbs"></a>СДР

- Определение маски кода структурной разбивки работы (WBS). 
    
#### <a name="tasks"></a>Задачи

- Изменение типа задачи (фиксированной работы, длительности или единиц).
    
- Изменение того, управляется ли задача усилием.
    
- Изменение начисления с фиксированными затратами.
    
- Изменение содержимого [TASK_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NOTES.aspx) поля. PSI может считывать только текстовую часть заметок задачи, которые являются двоичными данными RTF. Но вы можете редактировать заметки о назначениях [(ASSN_NOTES),](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.AssignmentRow.ASSN_NOTES.aspx) которые являются текстовыми данными. База данных отчетов не включает заметки о задачах и назначениях. 
    
- Создание или изменение повторяющихся задач.
    
- Назначение или изменение календаря задач для существующих задач.
    
- Создание новой задачи с календарем задач.
    
- Изменение значения поля [TASK_IGNORES_RES_CAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IGNORES_RES_CAL.aspx) (задача игнорирует календарь ресурсов). 
    
- Изменение активного состояния задачи с помощью [QueueUpdateProject,](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) если в тот же вызов были внесены дополнительные изменения. Дополнительные сведения см. в разделе *"Планирование проектов* на сервере" в разделе ["Программируемость Project Server".](project-server-programmability.md)
    
#### <a name="summary-tasks"></a>Суммарные задачи.

- Создание или изменение назначений для суммарных задач.
    
    > [!NOTE]
    > Не рекомендуется выполнять назначения для суммарных задач с помощью Project профессиональный или другим способом. Дополнительные сведения см. в разделе *"Планирование проектов* на сервере" в разделе ["Программируемость Project Server".](project-server-programmability.md) 
  
- Изменение полей суммарной задачи, которые обычно скапываются из подзадачи. В проектах на стороне сервера всегда сводится сводная информация вместо того, чтобы устанавливать сведения о суммарной задаче и перенагружать ее в подзадачи. В суммарных задачах можно редактировать только следующие поля:
    
  - Зависимости задач
    
  - Настраиваемые поля без формул
    
  - [TASK_NAME](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NAME.aspx)
    
  - [TASK_OUTLINE_LEVEL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_OUTLINE_LEVEL.aspx)
    
  - [TASK_IS_MARKED](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IS_MARKED.aspx)
    
  - [TASK_CONSTRAINT_TYPE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_TYPE.aspx)
    
  - [TASK_CONSTRAINT_DATE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_CONSTRAINT_DATE.aspx)
    
  - [TASK_PRIORITY](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_PRIORITY.aspx)
    
  - [TASK_DEADLINE](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_DEADLINE.aspx)
    
  - [TASK_FIXED_COST](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST.aspx)
    
  - [TASK_FIXED_COST_ACCRUAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_FIXED_COST_ACCRUAL.aspx) (установите значение только при создании задачи) 
    
  - [TASK_WBS](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_WBS.aspx)
    
Для суммарной задачи проекта ограничения PSI такие же, как для Project профессиональный. PSI может изменять назначения бюджета, включая бюджеты затрат.
  
#### <a name="project-level-calculation-options"></a>Параметры вычислений на уровне проекта

- Изменение типа проекта между расписанием с начала (SFS) и расписанием с завершения (SFF). (PSI может создать проект как SFS или SFF, но после создания его можно изменить только в Project профессиональный.)
    
- Изменение базового календаря проекта[(CAL_UID)](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.CAL_UID.aspx) после создания проекта. 
    
- Изменение параметров вычислений. С помощью PSI можно настроить следующие параметры вычислений при создания проекта, но для изменения этих параметров требуется Project профессиональный. (В представлении Backstage выберите **"Параметры"** и выберите вкладку **"Расписание"** в диалоговом окне **"Параметры** проекта".) 
    
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
    

