---
title: Какие задачи PSI выполняет, а какие — нет
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eac6be6a-9a20-4bc0-8da2-b2fd93aab04f
description: Интерфейс Project сервера (PSI) может помочь автоматизировать многие серверные процессы в локальной установке Project Server 2013. Но некоторые функции требуют использования Microsoft Project профессиональный 2013.
ms.openlocfilehash: b93c3535ca6693a84d11370de17bc18375f168ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346531"
---
# <a name="what-the-psi-does-and-does-not-do"></a>Какие задачи PSI выполняет, а какие — нет

Интерфейс Project сервера (PSI) может помочь автоматизировать многие серверные процессы в локальной установке Project Server 2013. Но некоторые функции требуют использования Microsoft Project профессиональный 2013.
  
|||
|:-----|:-----|
|||
   
PSI предназначен для дополнения возможностей Project профессиональный 2013 г., а не для предоставления серверной альтернативы для всех Project профессиональный функций. Сторонние разработчики могут использовать PSI для создания веб-части для локальных установок рабочих пространств Project Web App и проекта, создания настраиваемого Windows приложений и веб-приложений, взаимодействующих с локальными данными Project Server, разработки логики рабочих процессов для управления портфелями проектов, разработки локальных обработчиков событий с полным доверием и интеграции Project Server с другими приложениями. PSI нельзя использовать для разработки приложений для Office Store, мобильных устройств или планшетов; для этого можно использовать клиентскую объектную модель (CSOM).
  
> [!NOTE]
> PSI предоставляет более полный программный интерфейс для Project Server 2013, чем CSOM. Но, если CSOM не предоставляет необходимые функции, рекомендуется использовать CSOM для разработки новых приложений. Дополнительные сведения см. [в дополнительных сведениях о том, что делает и не делает CSOM.](what-the-csom-does-and-does-not-do.md) 
  
## <a name="usage-scenarios-for-the-psi"></a>Сценарии использования для PSI
<a name="pj14_WhatPSIDoes_UsageScenarios"> </a>

Ниже приводится пример некоторых приложений, поддерживаемых PSI для серверных проектов и вычислений:
  
- **Автоматизация создания или управления сущностями в Project Server** Хотя Project профессиональный 2013 и Project Web App вместе предназначены для обработки управления и создания сущностях, таких как проекты, корпоративные ресурсы и настраиваемые поля, часто бывают случаи, когда настраиваемые приложения могут сэкономить время с помощью массовых или повторяющихся заданий. PSI может автоматизировать несколько видов заданий, которые CSOM не делает, например, с кубами OLAP, анализом портфеля проектов, драйверами бизнеса, уведомлениями, поставщиками ссылок на объекты, безопасностью и SharePoint работой. 
    
- **Получать данные в опубликованных или архивных таблицах Project базы данных** Так как прямой доступ к таблицам черновиков, опубликованных и архивных таблиц не поддерживается, можно использовать PSI для чтения данных, недоступных в таблицах отчетов или представлениях. Например, получите сведения о версиях проекта, датах и изменениях, хранимых в таблицах архива, а затем заполнять управление JS Grid в веб-части информацией. 
    
- **Проверка данных о состоянии и времени** Используйте PSI в локальных обработчиках предварительного события, чтобы проверить состояние назначения или данные таблицы, которые введите пользователи, прежде чем данные будут сохранены в Project Web App. 
    
- **Проекты по обслуживанию** Создайте проекты-заполнители для использования с планами ресурсов. Зарезервируйте время и ресурсы для работ по обслуживанию или основного бизнеса. В проектах по обслуживанию задачи обычно не используются. 
    
- **Создание финансовых проектов.** Создавайте проекты для резервирования времени с помощью расписаний для последующей интеграции с финансовыми системами. Создавайте иерархию финансовых кодов, отражающих структуру детализации затрат финансовой системы. Для финансовых проектов не требуется выполнять планирование или обновлять состояния. 
    
- **Интеграция с системами бухгалтерского учета.** Регистрируйте затраты на ресурсы и расходы, связанные с проектами, и передавайте данные в финансовые системы и системы выставления счетов, а также используйте эти данные для целей сравнения с бюджетом. Синхронизируйте задачи, ресурсы и назначения между системами. Отметьте данные расписания в одной системе для передачи в другую (вопрос о том, какое расписание должно использоваться, зависит от потребностей организации или от индивидуальных проектов). 
    
- **Автоматизация обновлений, получаемых от участников рабочих групп.** При работе с проектами, которые не являются активно управляемыми, вы можете автоматически обновлять проекты на сервере по мере прогресса и внесения изменений в проекты участниками рабочих групп. Проекты можно обновлять и повторно публиковать без участия руководителей проектов, проверяющих результаты или корректирующих планы. 
    
- **Оценка Project серверов в локальных обработчиках** событий полного доверия Локальный обработник событий для предварительного события **ProjectCreating** может использовать данные Project Server из PSI, чтобы определить, следует ли отменять событие. Например, прежде чем создать проект, можно сравнить предлагаемый проект с существующими проектами. 
    
- **Создание настраиваемой деятельности рабочего процесса для управления запросами** Используйте PSI в локальных действиях рабочего процесса с полным доверием для изменения и обновления предложений проектов на основе шаблонов корпоративных проектов. Используйте настраиваемые поля проекта для тегов проекта с информацией, необходимой для процесса инициации и утверждения. Добавьте задачи по определению этапов проекта, основных вех и конечных результатов. После утверждения предложений по проектам рабочий процесс может изменять их в полнофутбные проекты, управляемые с помощью Project профессиональный. 
    
- **Создание расширений PSI** **(Deprecated.** Расширения обесценяются в Project Server 2013 и не будут поддерживаться в будущих выпусках.) PSI можно расширить с помощью настраиваемой службы с помощью интерфейса Windows связи (WCF). Расширения PSI работают на компьютере Project Server и могут использовать ту же инфраструктуру безопасности, что и встроенные службы PSI. Расширения могут запрашивать таблицы отчетов, использовать отдельные таблицы баз данных, консолидировать вызовы PSI для сохранения пропускной способности, а также интегрироваться с сторонними приложениями и другими серверными компонентами. Дополнительные сведения см. в [дополнительных сведениях о разработке расширений PSI.](https://msdn.microsoft.com/library/1b484623-94fb-47c9-84c1-3e68a9133042%28Office.15%29.aspx)
    
- **Использование обезличения в локальных приложениях** с полным доверием Вызовы к интерфейсу WCF PSI можно обезличить, чтобы приложение допускали разрешения безопасности обезличенных пользователей. Обезличение следует использовать с осторожностью и осторожностью. Чтение и обновление сведений о состоянии для других пользователей не требует обезличения. Новые приложения, которые требуют обезличения, должны использовать протокол CSOM и OAuth вместо PSI. Дополнительные сведения о вымыске с PSI см. в см. в этой ссылке [Use Impersonation with WCF.](https://msdn.microsoft.com/library/e3597901-2f02-44a2-8076-d32aae540b38%28Office.15%29.aspx)
    
> [!NOTE]
> В некоторых случаях PSI можно использовать в клиентских приложениях с CSOM и Project Online. Если вы используете веб-службу PSI на основе ASMX, приложение должно включать метод проверки подлинности объекта [Microsoft.ProjectServer.Client.ProjectContext](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectContext.aspx) в CSOM и метод проверки подлинности клиентского объекта **System.Web.Services.Protocols.SoapHttpClientProtocol.** Пример, использующий веб-службу с SharePoint CSOM, см. в SharePoint Online с использованием проверки подлинности на основе [утверждений.](https://msdn.microsoft.com/library/49067f7a-3020-478f-ba97-4b7ce3ea9b87%28Office.15%29.aspx) > из-за ограниченных разрешений на уровне приложений PSI не может использоваться в приложениях, предназначенных для распространения в общедоступных Office Store. В этом случае можно использовать только CSOM. 
  
## <a name="what-the-psi-does-not-do"></a>Что не делает PSI
<a name="pj14_WhatPSIDoes_DoesNotDo"> </a>

Несмотря на то, что PSI может делать много вещей, PSI не делает. Ниже следующую следующую статью: PSI не может сделать, но CSOM может сделать.
  
### <a name="project-online-and-remote-event-receivers"></a>Project Online и удаленные приемники событий

Основное ограничение PSI — это Project Online. Приложения, которые используют PSI, требуют полного доступа к локальной установке Project Server. Например, PSI нельзя использовать в приемниках удаленных событий, где приемник событий устанавливается в качестве службы Microsoft Azure.
  
### <a name="workflows-and-claims-authentication"></a>Проверка подлинности рабочего процесса и утверждений

Определение рабочего процесса, использующее Windows workflow Foundation версии 4 (WF4), требует проверки подлинности утверждений, которую PSI не поддерживает напрямую. Это означает, что вы не можете использовать PSI для создания проекта в Project Server 2013 с типом корпоративного проекта (EPT) с определением рабочего процесса WF4.
  
PSI можно использовать для создания проектов с epTs, которые либо не имеют рабочего процесса, либо используют устаревшее определение WF3.5 (версия рабочего процесса в Project Server 2010). Чтобы создать проект с EPT с определением WF4, используйте CSOM.
  
 **Действия, Project профессиональный:**
  
Следующий список — это вещи, которые не могут сделать ни PSI, ни CSOM.
  
#### <a name="local-data"></a>Локальные данные

- Управление данными в локальных проектах (.mpp files). Например, определение таблиц коэффициента затрат или контуров доступности для локальных ресурсов. 
    
- Определение или редактирование локальных базовых календарей или календарей ресурсов, включая исключения календаря.
    
- Определение локальных пользовательских полей. (PSI поддерживает редактирование локальных пользовательских значений полей для задач, ресурсов и назначений.)
    
#### <a name="enterprise-data"></a>Корпоративные данные

- Проверка или редактирование корпоративного глобального шаблона. Глобальные корпоративные данные в Project Server 2013 — это набор двоичных таблиц данных в базе данных Project, а не шаблон проекта, как в Office Project Server 2007 и более ранних версиях.
    
- Определение или редактирование корпоративных календарей. Методы [Calendar](https://msdn.microsoft.com/library/WebSvcCalendar.Calendar.aspx) управляют только исключениями календаря. 
    
#### <a name="master-projects-and-cross-project-links"></a>Мастер-проекты и межпроектные ссылки

- Создание мастер-проектов и вставка подпроектов.
    
- Планирование критического пути в мастер-проекте. 
    
- Создание межпроектных ссылок.
    
#### <a name="resources"></a>Ресурсы

- Запрос или выполнение выравнивания ресурсов.
    
- Изменение ресурса при назначении. (С помощью PSI можно удалить назначение и создать новое.)
    
- Удаление или замена ресурса, на который фактически принята работа (фактические данные).
    
- Изменение типа ресурса между работой, материалом и стоимостью.
    
- Создание или редактирование календарей ресурсов.
    
- При добавлении ресурса в задачу PSI автоматически не перераспределяет работу так, Project профессиональный делает. От разработчика зависит выбор и явное назначение распределения работ.
    
#### <a name="cost-resources"></a>Затратные ресурсы 

- Редактирование, создание или удаление затратных ресурсов и назначений с помощью [Project](https://msdn.microsoft.com/library/WebSvcProject.Project.aspx) методов. Методы [Ресурса](https://msdn.microsoft.com/library/WebSvcResource.Resource.aspx) могут создавать затратные ресурсы, но не могут изменять их. 
    
#### <a name="work-contours"></a>Контуры работы

- Редактирование данных с периодом времени.
    
    > [!NOTE]
    > Метод [UpdateStatus](https://msdn.microsoft.com/library/WebSvcStatusing.Statusing.UpdateStatus.aspx) в веб-службе **Statusing** Может изменять время выполнения заданий после обновления и публикации данных назначения руководителем проекта. 
  
- Настройка или изменение типа контура назначения (например, плоский, загруженный сзади или фронтальная загрузка).
    
#### <a name="baselines-and-earned-value"></a>Базовые показатели и заработаное значение

- Сохранение базовых данных или редактирование базовых данных. 
    
- Настройка даты выполнения.
    
- Вычисление отклонений и заработанных значений. 
    
#### <a name="interactive-scheduling"></a>Интерактивное планирование

- Поддержка интерактивного планирования. (Поскольку Project Сервер асинхронно обрабатывает взаимодействия, интерактивное планирование должно быть сделано с Project профессиональный.)
    
    > [!NOTE]
    > Чтобы избежать изменения программного поведения, методы PSI, которые выдвигаются из Project Server 2010, действуют так же в Project Server 2013. Например, [QueueUpdateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) по-прежнему имеет те же ограничения и использует более старый серверный движок планирования. Новый метод [QueueUpdateProject2](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject2.aspx) устраняет многие из этих ограничений и использует новый серверный движок Project Server 2013, который является тем же механизмом планирования, что и в Project профессиональный 2013 г. 
  
#### <a name="wbs"></a>СДР

- Определение структуры разбивки по работе (WBS) маски кода. 
    
#### <a name="tasks"></a>Задачи

- Изменение типа задачи (фиксированная работа, продолжительность или единицы).
    
- Изменение того, является ли задача управляемой усилиями.
    
- Изменение начисления с фиксированной стоимостью задачи.
    
- Изменение содержимого [TASK_NOTES](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_NOTES.aspx) поля. PSI может считывать только текстовую часть заметок задачи, которые являются двоичными данными .rtf. Но можно изменить заметки назначения [(ASSN_NOTES), которые](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.AssignmentRow.ASSN_NOTES.aspx) являются текстовыми данными. База данных отчетов не включает заметки о задачах или назначениях. 
    
- Создание или редактирование повторяющихся задач.
    
- Назначение или изменение календаря задач для существующих задач.
    
- Создание новой задачи с календарем задач.
    
- Изменение значения поля [TASK_IGNORES_RES_CAL](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.TaskRow.TASK_IGNORES_RES_CAL.aspx) (задача игнорирует календарь ресурсов). 
    
- Изменение активного состояния задачи с помощью [QueueUpdateProject,](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueUpdateProject.aspx) если в одном вызове будут внесены дополнительные изменения. Дополнительные сведения см. в *Project Scheduling on the Server* в разделе Project [Server.](project-server-programmability.md)
    
#### <a name="summary-tasks"></a>Суммарные задачи.

- Создание или изменение назначений в сводных задачах.
    
    > [!NOTE]
    > Рекомендуется не выполнять назначения по суммарным задачам с помощью Project профессиональный или другим способом. Дополнительные сведения см. в *Project Scheduling on the Server* в разделе Project [Server.](project-server-programmability.md) 
  
- Редактирование сводных полей задач, которые обычно свернуты из подзадачи. Проекты на стороне серверов всегда сверкают сводную информацию, а не настраивают сведения о сводной задаче и передвигают ее в подзадачи. В сводных задачах можно редактировать только следующие поля:
    
  - Зависимости задач
    
  - Неявные настраиваемые поля
    
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
    
Для задачи сводки проекта ограничения PSI такие же, как и для Project профессиональный. PSI может изменять бюджетные назначения, включая бюджеты затрат.
  
#### <a name="project-level-calculation-options"></a>Project вычислений на уровне

- Изменение типа проекта между Расписанием от начала (SFS) и Расписание от завершения (SFF). (PSI может создавать проект как SFS или SFF, но после создания его можно изменить только в Project профессиональный.)
    
- Изменение базового календаря[проекта (CAL_UID)](https://msdn.microsoft.com/library/WebSvcProject.ProjectDataSet.ProjectRow.CAL_UID.aspx) после создания проекта. 
    
- Изменение параметров вычислений. Вы можете использовать PSI для настройки следующих вариантов вычислений при создания проекта, но изменение параметров требует Project профессиональный. (В представлении Закулисье выберите **Параметры,** а затем выберите вкладку **Расписание** в **диалоговом окне Project** Параметры.) 
    
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
    

