---
title: Коды ошибок Project Server
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- error codes
- errors
- Project Server errors
- PSErrorID
- PSI errors
keywords:
- psi, коды ошибок, Коды ошибок, Project Server, PSErrorID, интерфейс Project Server, коды ошибок, Project Server, коды ошибок
ms.assetid: db78a09c-ebef-47cc-8623-40abe117aa08
description: Эта статья содержит таблицы кодов ошибок для интерфейса Project Server (PSI) в Project Server 2013. Таблицы упорядочены по функциональным областям и по диапазонам кодов ошибок.
localization_priority: Priority
ms.openlocfilehash: c61821bcb85fa3bd83601659850577eaa93eda61
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705598"
---
# <a name="project-server-error-codes"></a>Коды ошибок Project Server

Эта статья содержит таблицы кодов ошибок для интерфейса Project Server (PSI) в Project Server 2013. Таблицы упорядочены по функциональным областям и по диапазонам кодов ошибок.
   
Процессы Project Server 2013 и методы интерфейса Project Server имеют номера кодов ошибок, упорядоченные, как правило, по функциональной области. Перечисление [Microsoft.Office.Project.Server.Library.PSErrorID](https://msdn.microsoft.com/library/microsoft.office.project.server.library.pserrorid_di_pj14mref(v=office.14).aspx) дублируется в [WebSvcProject.PSErrorID](https://msdn.microsoft.com/library/office/websvcproject.pserrorid_di_pj14mref.aspx); здесь коды ошибок перечисляются в алфавитном порядке по имени. В этой статье перечислены коды ошибок в таблицах, упорядоченные по классу интерфейса Project Server или функциональной области, а также по номеру идентификатора ошибки. 
  
> [!NOTE]
>  Многие коды ошибок являются общими и могут иметь несколько возможных причин. Для получения дополнительной информации об ошибках можно выполнить указанные ниже действия. 
> - Для ASMX-приложений используйте **System.Web.Services.Protocols.SoapException** с объектом **PSClientError**, чтобы отобразить иерархию ошибок в вызове метода PSI. См. [пример кода ошибки для ASMX](#pj15_ErrorCodes_ASMXExample). 
> - Для WCF-приложений вы можете использовать **System.ServiceModel.FaultException**, чтобы получить объект **PSClientError** и дополнительные сведения об ошибке. См. [пример кода ошибки для WCF](#pj15_ErrorCodes_WCFExample). 
> - Используйте журнал событий приложения на компьютере Project Server.
> - Используйте журналы трассировки единой службы ведения журналов (ULS). Объяснения приводятся в разделе *Проверка ошибок* в статье [Начало разработки для Project 2010](https://msdn.microsoft.com/library/gg607685.aspx). 
> - Для получения дополнительных сведений об использовании журналов ULS см. статью [Project Server 2010: чего следует ожидать от непредвиденного](https://blogs.msdn.com/b/brismith/archive/2010/03/24/project-server-2010-what-to-expect-when-you-get-the-unexpected.aspx) или выполните поиск в блоге по словам "reading ULS logs". 
> - Чтобы облегчить поиск проблем в данных ULS, воспользуйтесь [средством просмотра ULS Viewer](https://www.codeproject.com/Articles/458052/ULS-Log-Viewer). 
> - Используйте приложение Microsoft SQL Server Profiler для перехвата или отслеживания ошибок базы данных. Дополнительные сведения см. в статье [Приложение SQL Server Profiler](https://msdn.microsoft.com/library/3ad5f33d-559e-41a4-bde6-bb98792f7f1a.aspx). 
> - Многие коды ошибок предназначены только для внутреннего использования. Например, поскольку веб-службы **ExchangeSync** и **PWA** недоступны для сторонней разработки, вы вряд ли столкнетесь с кодами ошибок из методов, относящихся к данной области, таких как **Rules** и **StatusReports**. Однако для полноты информации в таблицы данной статьи занесены все коды ошибок Project Server. 
  
## <a name="table-1-error-code-functional-areas-and-related-number-ranges"></a>Табл. 1. Функциональные области кодов ошибок и связанные диапазоны номеров

|Функциональная область Project Server|Диапазоны номеров кодов ошибок|
|:-----|:-----|
|[Табл. 3. Коды общих ошибок](#pj15_ErrorCodes_General) <br/> |0–99, 500–999, 9131, 10000–10099, 20000–20099, 26000–26099  <br/> |
|[Табл. 4. Активный кэш](#pj15_ErrorCodes_ActiveCache) <br/> |12000–12099  <br/> |
|[Табл. 5. Синхронизация Active Directory](#pj15_ErrorCodes_ActiveDirectory) <br/> |27000–27999  <br/> |
|[Табл. 6. Веб-служба администрирования](#pj15_ErrorCodes_Admin) <br/> |16600–16699; 19011, 19012, 19032; 20003; 25000–25099  <br/> |
|[Табл. 7. Архивирование (резервное копирование и восстановление)](#pj15_ErrorCodes_Archive) <br/> |25000–25999 и 29000–29099  <br/> |
|[Табл. 8. Назначения](#pj15_ErrorCodes_Assignments) <br/> |120–199  <br/> |
|[Табл. 9. Календарь](#pj15_ErrorCodes_Calendar) <br/> |77 и 13000–13999  <br/> |
|[Табл. 10. Служба построения куба (CBS)](#pj15_ErrorCodes_CBS) <br/> |17000–17999  <br/> |
|[Табл. 11. Возвращение — извлечение](#pj15_ErrorCodes_CICO) <br/> |10100–10199  <br/> |
|[Табл. 12. Настраиваемые поля](#pj15_ErrorCodes_CustomFields) <br/> |11500–11999  <br/> |
|[Табл. 13. Таблицы подстановки](#pj15_ErrorCodes_LookupTables) <br/> |11000–11499  <br/> |
|[Табл. 14. Прочие](#pj15_ErrorCodes_Miscellaneous) <br/> |11000–11499  <br/> |
|[Табл. 15. Уведомления](#pj15_ErrorCodes_Notifications) <br/> |16000–16599  <br/> |
|[Табл. 16. Оптимизатор](#pj15_ErrorCodes_Optimizer) (анализ портфеля проектов)  <br/> |29000–29999  <br/> |
|[Табл. 17. Планировщик](#pj15_ErrorCodes_Planner) (анализ портфеля проектов)  <br/> |28000–28999  <br/> |
|[Табл. 18. Проекты](#pj15_ErrorCodes_Projects) <br/> |100–499, 1000–1199, 9100–9199 и 23000–23999  <br/> |
|[Табл. 19. Служба отчетных данных](#pj15_ErrorCodes_RDS) (RDS)  <br/> |24000–24999  <br/> |
|[Табл. 20. Ресурсы](#pj15_ErrorCodes_Resources) <br/> |2000–2999  <br/> |
|[Табл. 21. Планы использования ресурсов](#pj15_ErrorCodes_ResourcePlans) <br/> |30000–30999  <br/> |
|[Табл. 22. Правила](#pj15_ErrorCodes_Rules) <br/> |21000–21099  <br/> |
|[Табл. 23. Безопасность](#pj15_ErrorCodes_Security) <br/> |19000–19099  <br/> |
|[Табл. 24. События сервера](#pj15_ErrorCodes_Events) <br/> |19033 и 22000–22999  <br/> |
|[Табл. 25. Определение состояния](#pj15_ErrorCodes_Statusing) <br/> |3100–3199  <br/> |
|[Табл. 26. Отчеты о состоянии](#pj15_ErrorCodes_StatusReports) <br/> |12100–12299  <br/> |
|[Табл. 27. Задачи](#pj15_ErrorCodes_Tasks) <br/> |7000–7099  <br/> |
|[Табл. 28. Расписания](#pj15_ErrorCodes_Timesheets) <br/> |3200–3299  <br/> |
|[Табл. 29. Делегирование пользователей](#pj15_ErrorCodes_UserDelegation) <br/> |43000–43500  <br/> |
|[Табл. 30. Рабочий процесс](#pj15_ErrorCodes_Workflow) <br/> |35000–35999: рабочий процесс  <br/> |
|[Табл. 31. WssInterop и ObjectLinkProvider (интеграция с SharePoint)](#pj15_ErrorCodes_WSS) <br/> |16400–16499: интеграция с SharePoint и рабочие области проектов  <br/> 18000–18099: поставщик связей с объектами и импорт проектов SharePoint  <br/> |
   
## <a name="table-2-error-code-table-by-number-range"></a>Табл. 2. Таблица кодов ошибок по диапазону номеров

|Диапазон кодов ошибок|Таблица кодов ошибок|
|:-----|:-----|
|0–99  <br/> |[Табл. 3. Общие коды ошибок](#pj15_ErrorCodes_General), за исключением 77 — в [Табл. 9. Календарь](#pj15_ErrorCodes_Calendar) <br/> |
|100–119  <br/> |[Табл. 18. Проекты](#pj15_ErrorCodes_Projects) <br/> |
|120–199  <br/> |[Табл. 8. Назначения](#pj15_ErrorCodes_Assignments) <br/> |
|500–999  <br/> |[Табл. 3. Коды общих ошибок](#pj15_ErrorCodes_General) <br/> |
|1000–1199  <br/> |[Табл. 18. Проекты](#pj15_ErrorCodes_Projects) <br/> |
|2000–2999  <br/> |[Табл. 20. Ресурсы](#pj15_ErrorCodes_Resources) <br/> |
|3100–3199  <br/> |[Табл. 25. Определение состояния](#pj15_ErrorCodes_Statusing) <br/> |
|3200–3299  <br/> |[Табл. 28. Расписания](#pj15_ErrorCodes_Timesheets) <br/> |
|7000–7099  <br/> |[Табл. 27. Задачи](#pj15_ErrorCodes_Tasks) <br/> |
|9100–9199  <br/> |[Табл. 18. Проекты](#pj15_ErrorCodes_Projects), за исключением 9131 — в [Табл. 3. Коды общих ошибок](#pj15_ErrorCodes_General) <br/> |
|10000–10099  <br/> |[Табл. 3. Коды общих ошибок](#pj15_ErrorCodes_General) <br/> |
|10100–10199  <br/> |[Табл. 11. Возвращение — извлечение](#pj15_ErrorCodes_CICO) <br/> |
|11000–11499  <br/> |[Табл. 13. Таблицы подстановки](#pj15_ErrorCodes_LookupTables) <br/> |
|11500–11999  <br/> |[Табл. 12. Настраиваемые поля](#pj15_ErrorCodes_CustomFields) <br/> |
|12000–12099  <br/> |[Табл. 4. Активный кэш](#pj15_ErrorCodes_ActiveCache) <br/> |
|12100–12299  <br/> |[Табл. 26. Отчеты о состоянии](#pj15_ErrorCodes_StatusReports) <br/> |
|13000–13999  <br/> |[Табл. 9. Календарь](#pj15_ErrorCodes_Calendar) <br/> |
|16000–16399  <br/> |[Табл. 15. Уведомления](#pj15_ErrorCodes_Notifications) <br/> |
|16400–16499  <br/> |[Табл. 31. WssInterop и Object Link Provider (интеграция с SharePoint)](#pj15_ErrorCodes_WSS) <br/> |
|16600–16699  <br/> |[Табл. 6. Веб-служба администрирования](#pj15_ErrorCodes_Admin) <br/> |
|17000–17999  <br/> |[Табл. 10. Служба построения куба (CBS)](#pj15_ErrorCodes_CBS) <br/> |
|18000–18099  <br/> |[Табл. 31. Интеграция с SharePoint](#pj15_ErrorCodes_WSS) <br/> |
|19000–19099  <br/> |[Табл. 23. Безопасность](#pj15_ErrorCodes_Security), за исключением 19011, 19012 и 19032 (кодов, связанных с безопасностью) — в [Табл. 6. Веб-служба администрирования](#pj15_ErrorCodes_Admin) <br/> |
|20000–20099  <br/> |[Табл. 3. Коды общих ошибок](#pj15_ErrorCodes_General), за исключением 20003 — в [Табл. 6. Веб-служба администрирования](#pj15_ErrorCodes_Admin) <br/> |
|21000–21099  <br/> |[Табл. 22. Правила](#pj15_ErrorCodes_Rules) <br/> |
|22000–22999  <br/> |[Табл. 24. События сервера](#pj15_ErrorCodes_Events) <br/> |
|23000–23999  <br/> |[Табл. 18. Проекты](#pj15_ErrorCodes_Projects) <br/> |
|24000–24999  <br/> |[Табл. 19. Служба отчетных данных](#pj15_ErrorCodes_RDS) (RDS)  <br/> |
|25000–25999  <br/> |[Табл. 7: Архивирование (резервное копирование и восстановление)](#pj15_ErrorCodes_Archive), за исключением 25004, 25006 — в [Табл. 6. Веб-служба администрирования](#pj15_ErrorCodes_Admin) <br/> |
|26000–26099  <br/> |[Табл. 3. Коды общих ошибок](#pj15_ErrorCodes_General) <br/> |
|27000–27999  <br/> |[Табл. 5. Синхронизация Active Directory](#pj15_ErrorCodes_ActiveDirectory) <br/> |
|28000–28999  <br/> |[Табл. 17. Планировщик](#pj15_ErrorCodes_Planner) (анализ портфеля проектов)  <br/> |
|29000–29999  <br/> |[Табл. 16. Оптимизатор](#pj15_ErrorCodes_Optimizer) (анализ портфеля проектов), за исключением 29021 — в [Табл. 7. Архивирование](#pj15_ErrorCodes_Archive) <br/> |
|30000–30999  <br/> |[Табл. 21. Планы использования ресурсов](#pj15_ErrorCodes_ResourcePlans) <br/> |
|31000–31999  <br/> 32000–32100  <br/> |[Табл. 14. Прочие](#pj15_ErrorCodes_Miscellaneous) (аудит; не используется)  <br/> Страницы сведений о проекте  <br/> |
|35000–35999  <br/> 40000–40499  <br/> |[Табл. 30. Рабочий процесс](#pj15_ErrorCodes_Workflow) <br/> |
|40500–40999  <br/> 42000–42999  <br/> |[Табл. 14. Прочие](#pj15_ErrorCodes_Miscellaneous) (**ExchangeSync**; внутреннее использование)  <br/> Временная шкала Project Web App  <br/> |
|43000–43500  <br/> |[Табл. 29. Делегирование пользователей](#pj15_ErrorCodes_UserDelegation) <br/> |
|50000–51999  <br/> |[Табл. 14. Прочие](#pj15_ErrorCodes_Miscellaneous) (ошибки базы данных)  <br/> |

<a name="pj15_ErrorCodes_General"></a>

## <a name="table-3-general-error-codes"></a>Табл. 3. Коды общих ошибок

|Код общей ошибки|Описание|
|:-----|:-----|
|NoError = 0; Success = 0  <br/> |Отсутствие ошибки или успешное выполнение операции.  <br/> |
|GeneralRequestInvalidParameter = 6  <br/> |Один из параметров или узлов запроса недопустим либо не является допустимым в контексте данного запроса.  <br/> |
|GeneralInvalidValue = 11  <br/> |Недопустимое значение запроса, например, в качестве GUID указан 0.  <br/> |
|GeneralStartDateGTorEQFinishDate = 26  <br/> |Указан недопустимый диапазон дат.  <br/> |
|GeneralQueueOperationInProcess = 29  <br/> |общая ошибка для операции, которая все еще обрабатывается в очереди.  <br/> |
|GeneralUnhandledException = 42  <br/> |Возникло необработанное исключение.  <br/> |
|GeneralDuplicateGUIDSpecified = 66  <br/> |В запросе используется повторяющийся GUID.  <br/> |
|GeneralDateNotValid = 69  <br/> |Даты должны находиться в диапазоне от 1/1/1984 до 12/12/2049.  <br/> |
|GeneralCostInvalid = 70  <br/> |Недопустимый параметр затрат.  <br/> |
|GeneralWorkInvalid = 71  <br/> |Недопустимый параметр трудозатрат.  <br/> |
|GeneralDurationInvalid = 72  <br/> |Недопустимый параметр длительности.  <br/> |
|GeneralUnitsInvalid = 73  <br/> |Указана недопустимая единица измерения.  <br/> |
|GeneralOnlyInsertsAllowed = 74  <br/> |Разрешены только вставки.  <br/> |
|GeneralOnlyUpdatesAllowed = 75  <br/> |Разрешены только обновления.  <br/> |
|GeneralSessionInvalid = 76  <br/> |Недопустимый параметр сеанса.  <br/> |
|GeneralDependencyUidInvalid = 78  <br/> |Недопустимый GUID зависимости.  <br/> |
|GeneralNumberInvalid = 79  <br/> |Недопустимое число.  <br/> |
|GeneralInvalidDataStore = 80  <br/> |Указанная база данных не существует. Используйте базу данных в [DataStoreEnum](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.DataStoreEnum.aspx).  <br/> |
|GeneralDurationOrWorkFormatInvalid = 513  <br/> |Недопустимая длительность или формат трудозатрат.  <br/> |
|GeneralRateFormatInvalid = 518  <br/> |Недопустимый формат ставки.  <br/> |
|GeneralQueueException = 9131  <br/> |Исключение. В службе очередей возникла общая ошибка.  <br/> |
|GeneralItemDoesNotExist = 10000  <br/> |Указанный элемент не существует.  <br/> |
|GeneralLCIDInvalid = 10001  <br/> |Недопустимый код (или идентификатор) языка.  <br/> |
|GeneralRowDoesNotExist = 10002  <br/> |Строки, указанной в **DataTable**, не существует.  <br/> |
|GeneralInvalidColumnValue = 20000  <br/> |Значение столбца в **DataTable** является недопустимым.  <br/> |
|GeneralInvalidDataRowState = 20001  <br/> |Состояние **DataRow** является недопустимым.  <br/> |
|GeneralDuplicatedNames = 20004  <br/> |Имеется повторяющееся имя. Имена должны быть уникальными.  <br/> |
|GeneralReadOnlyColumn = 20005  <br/> |Этот столбец доступен только для чтения.  <br/> |
|GeneralReadOnlyRow = 20006  <br/> |Эта строка доступна только для чтения.  <br/> |
|GeneralNotNullColumn = 20007  <br/> |Столбец не может иметь значение NULL.  <br/> |
|GeneralObjectAlreadyExists = 20008  <br/> |Объект уже существует.  <br/> |
|GeneralInvalidObject = 20009  <br/> |Недопустимый объект.  <br/> |
|GeneralSecurityAccessDenied = 20010  <br/> |Отказ в доступе из-за разрешений безопасности.  <br/> |
|GeneralInvalidOperation = 20011  <br/> |Недопустимая операция.  <br/> |
|GeneralInvalidCharacters = 20012  <br/> |Некоторые символы являются недопустимыми. Кроме символа табуляции, в имени проекта нельзя использовать следующие символы: `\ / " : ; < > | , . ' ? * #` <br/> |
|GeneralNameTooLong = 20013  <br/> |Слишком длинное имя.  <br/> |
|GeneralNameCannotBeBlank = 20014  <br/> |Имя не может быть пустым. Не используйте значение NULL или пустую строку.  <br/> |
|GeneralInvalidOperationOnReadOnlyValue = 20016  <br/> |Запрошенная операция со значением, доступным только для чтения, не является допустимой.  <br/> |
|GeneralInvalidDateOverlap = 20018  <br/> |Запрос содержит перекрывающиеся даты.  <br/> |
|GeneralParameterCannotBeNull = 20020  <br/> |Параметр не может иметь значение NULL.  <br/> |
|GeneralDescTooLong = 20021  <br/> |Слишком длинное описание.  <br/> |
|GeneralCategoryPermissionDenied = 20022  <br/> |В разрешении категории отказано.  <br/> |
|GeneralNotLicensed = 20024  <br/> |Пользователь не имеет лицензии на Project Server.  <br/> |
|GeneralGlobalPermissionDenied = 20023  <br/> |В глобальном разрешении отказано.  <br/> |
|GeneralActionCanceledByEventHandler = 22000  <br/> |Обработчик событий отменил это действие.  <br/> |
|GeneralActionCanceledBecauseServerEventServiceNotFound = 22001  <br/> |Отсутствует служба событий Project Server.  <br/> |
|GeneralActionCanceledBecauseServerEventServiceProblem = 22002  <br/> |Возникла проблема в службе событий Project Server.  <br/> |
|GeneralQueueJobFailed = 26000  <br/> |Сбой задания в очереди.  <br/> |
|GeneralQueueInvalidJobUID = 26001  <br/> |Недопустимый GUID задания для очереди.  <br/> |
|GeneralQueueInvalidTrackingUID = 26002  <br/> |Недопустимый GUID отслеживания для очереди.  <br/> |
|GeneralQueueInvalidJobInfoUID = 26003  <br/> |Недопустимый GUID сведений о задании для очереди.  <br/> |
|GeneralQueueInvalidCorrelationUID = 26004  <br/> |Недопустимый GUID корреляции очереди.  <br/> |
|GeneralQueueCorrelationBlocked = 26005  <br/> |Корреляция очереди заблокирована.  <br/> |
|GeneralQueueInvalidMessageType = 26006  <br/> |Недопустимый тип сообщения очереди.  <br/> |
|GeneralQueueInvalidJobState = 26007  <br/> |Недопустимое состояние задания в очереди.  <br/> |
|GeneralQueueInvalidGroupState = 26008  <br/> |Недопустимое состояние группы в очереди.  <br/> |
|GeneralQueueInvalidGroupPriority = 26009  <br/> |Недопустимый приоритет группы в очереди.  <br/> |
|GeneralQueueInvalidCorrelationPriority = 26010  <br/> |Недопустимый приоритет корреляции в очереди.  <br/> |
|GeneralQueueInvalidQueueID = 26011  <br/> |Недопустимый идентификационный номер очереди.  <br/> |
|GeneralQueueInvalidAdminAction = 26012  <br/> |Действие **Admin** является недопустимым для очереди.  <br/> |
|GeneralQueueInvalidStatType = 26013  <br/> |Недопустимый тип состояния очереди.  <br/> |
|GeneralQueueInvalidBlockPolicy = 26014  <br/> |Недопустимая политика блокировки очереди.  <br/> |
|GeneralQueueCannotRetryJob = 26015  <br/> |Очереди не удается повторить попытку выполнения задания.  <br/> |
|GeneralQueueInvalidSetting = 26016  <br/> |Недопустимый параметр для очереди.  <br/> |
|GeneralQueueInvalidRendezvousUID = 26017  <br/> |Недопустимый встречный GUID очереди.  <br/> |
|GeneralDalErrorGettingConnectionStrings = 26018  <br/> |Ошибка при получении строк подключения для уровня доступа к данным (DAL).  <br/> |
|GeneralDalErrorConnectingToDatabase = 26019  <br/> |Ошибка при подключении к базе данных на уровне доступа к данным.  <br/> |
|GeneralDalInvalidArgumentCountCreatingFilter = 26020  <br/> |Недопустимое число аргументов для создания фильтра.  <br/> |
|GeneralDataTableCannotBeNull = 26024  <br/> |Таблица данных **DataTable** не может быть **null**.  <br/> |
|GeneralDatasetConstraints = 26025  <br/> |Ошибка в ограничениях **DataSet**.  <br/> |
|GeneralInvalidDataSetStructure = 26027  <br/> |Структура **DataSet** является недопустимой.  <br/> |
|GeneralDalNoRowsUpdated = 26028  <br/> |Обновленные строки на уровне доступа к данным (DAL) отсутствуют.  <br/> |
|GeneralDataTableCannotBeEmpty = 26029  <br/> |Таблица данных **DataTable** не может быть пустой.  <br/> |
|GeneralWSSContentDBNotWritable = 26030  <br/> |Не удается выполнить запись базу данных контента SharePoint. Эта база данных контента доступна только для чтения, либо действует блокировка на уровне семейства веб-сайтов.  <br/> |
|GeneralSPValidateFormDigestError = 26031  <br/> |Ошибка проверки сводки формы в обратном вызове Project Web App, обычно это вызвано истечением времени ожидания.  <br/> |
|GeneralDelegationActiveForCurrentUser = 26032  <br/> |Текущий пользователь имеет активное делегирование. Такая ошибка создается веб-методами в службе **WinProj** для Project профессиональный.  <br/> |

<a name="pj15_ErrorCodes_ActiveCache"></a>

## <a name="table-4-active-cache"></a>Табл. 4. Активный кэш

|Код ошибки для активного кэша|Описание|
|:-----|:-----|
|ActiveCacheInvalidDataFormat = 12000  <br/> |Недопустимый формат данных.  <br/> |
|ActiveCacheUnsupportedDataFormatVersion = 12001  <br/> |Неподдерживаемая версия формата данных.  <br/> |
|ActiveCacheInvalidQueuedMessageType = 12003  <br/> |Недопустимый тип сообщения в очереди.  <br/> |
|ActiveCacheNullQueuedMessage = 12004  <br/> |Сообщение в очереди имеет значение NULL.  <br/> |
|ActiveCacheQueuedMessageExecutionError = 12005  <br/> |Возникла ошибка выполнения для сообщения в очереди.  <br/> |
|ActiveCacheInvalidDataSize = 12006  <br/> |Недопустимый размер данных.  <br/> |
|ActiveCacheQueueJobAlreadyStarted = 12007  <br/> |Задание в очереди уже запущено.  <br/> |
|ActiveCacheInvalidQueuedMessageFormat = 12008  <br/> |Недопустимый формат сообщения в очереди.  <br/> |
|ActiveCacheUnsupportedQueuedMessageVersion = 12009  <br/> |Недопустимая версия сообщения в очереди.  <br/> |
|ActiveCacheUnsupportedQueueDataType = 12011  <br/> |Неподдерживаемый тип данных в очереди.  <br/> |
|ActiveCacheInvalidVersionStampForSave = 12012  <br/> |Недопустимый штамп версии для операции сохранения.  <br/> |
|ActiveCacheProjectTypeMismatch = 12013  <br/> |Тип проекта не совпадает с ожидаемым типом.  <br/> |
|ActiveCacheDataValidationFailed = 12014  <br/> |Сбой проверки данных.  <br/> |
|ActiveCacheUnsupportedProjectProfessionalVersion = 12015  <br/> |Версия Project профессиональный не поддерживается.  <br/> |
|ActiveCacheGeneralSQLException = 12016  <br/> |Возникла общая ошибка SQL.  <br/> |

<a name="pj15_ErrorCodes_ActiveDirectory"></a>

## <a name="table-5-active-directory-synchronization"></a>Табл. 5. Синхронизация Active Directory

|Код ошибки для синхронизации Active Directory|Описание|
|:-----|:-----|
|AdSyncUpdateTimerJobFailed = 27002  <br/> |Сбой задания обновления таймера при синхронизации со службами каталогов Active Directory.  <br/> |
|AdSyncDeleteTimerJobFailed = 27003  <br/> |Сбой задания удаления таймера при синхронизации со службами каталогов Active Directory.  <br/> |
|AdSyncAdConnectFail = 27006  <br/> |Не удается подключиться к Active Directory.  <br/> |
|AdMaximumGroupsCountExceeded = 27007  <br/> |Было превышено максимальное число групп.  <br/> |
|SRAInvalidVersion = 27300  <br/> |Недопустимая версия SRA.  <br/> |
|SRADelayedUpgradeFailed = 27301  <br/> |Сбой действия по асинхронному обновлению SRA.  <br/> |
|(27000–27999)  <br/> |Другие ошибки синхронизации для службы Active Directory не перечисляются на сервере Project Server.  <br/> |

<a name="pj15_ErrorCodes_Admin"></a>

## <a name="table-6-admin-web-service"></a>Табл. 6. Веб-служба администрирования

|Код ошибки веб-службы администрирования|Описание|
|:-----|:-----|
|AdminViewNameAlreadyExists = 16600  <br/> |Это имя представления уже существует. Имена должны быть уникальными.  <br/> |
|AdminViewInvalidDividerPosition = 16601  <br/> |Недопустимое положение разделителя.  <br/> |
|AdminViewDataWasTampered = 16602  <br/> |Данные были изменены.  <br/> |
|AdminViewMaxDisplayedFieldsNumberExceeded = 16603  <br/> |Превышено максимальное число полей на экране.  <br/> |
|AdminViewCannotDeleteDefaultView = 16604  <br/> |Не удается удалить представление по умолчанию.  <br/> |
|AdminViewCannotCopyDefaultView = 16605  <br/> |Не удается скопировать представление по умолчанию.  <br/> |
|AdminLocalCustomFieldInvalid = 19011  <br/> |Недопустимое локальное настраиваемое поле.  <br/> |
|AdminEnterpriseCustomFieldInvalid = 19012  <br/> |Недопустимое корпоративное настраиваемое поле.  <br/> |
|AdminNTAccountNotFound = 19032  <br/> |Отсутствует учетная запись Windows (NTLM).  <br/> |
|AdminUnableToMerge = 20003  <br/> |Не удается объединить данные.  <br/> |
|AdminDeleteArchivedProjectsFailed = 25004  <br/> |Сбой операции удаления для архивных проектов.  <br/> |
|AdminUpdateArchiveScheduleFailed = 25006  <br/> |Не удалось обновить расписание архивирования.  <br/> |
|AdminArchiveScheduleFailed = 28018  <br/> |Сбой расписания архивирования.  <br/> |
|AdminReadArchivedProjectsListFailed = 28019  <br/> |Не удалось считать список архивных проектов.  <br/> |
|AdminReadArchiveScheduleFailed = 28020  <br/> |Не удалось считать расписание архивирования.  <br/> |
|AdminUserAccountNameNull = 28021  <br/> |Имя учетной записи пользователя имеет значение NULL.  <br/> |
|AdminIsWindowsUserNull = 28022  <br/> |Учетная запись пользователя Windows (NTLM) имеет значение NULL.  <br/> |
|AdminInvalidTimePeriodState = 28023  <br/> |Недопустимое состояние периода времени.  <br/> |
|AdminGlobalUpdateFailed = 28024  <br/> |Во время вызова **SetServerCurrency** произошел сбой глобального корпоративного обновления.  <br/> |
|AdminGlobalCheckedOut = 28025  <br/> |Глобальный корпоративный шаблон уже извлечен во время вызова **SetServerCurrency**.  <br/> |
|AdminInvalidDatabaseTimeout = 28026  <br/> |Истекло время ожидания из-за недопустимой базы данных.  <br/> |
|AdminInvalidDatabaseTimeoutType = 28027  <br/> |Истекло время ожидания из-за недопустимого типа базы данных.  <br/> |
|AdminInvalidEntityType = 28028  <br/> |Тип объекта является недопустимым. См. [EntityCollection](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.EntityCollection.aspx) .  <br/> |
|AdminInvalidCompatibilityModeChange = 28029  <br/> |Недопустимое изменение режима совместимости.  <br/> |
|AdminInvalidCompatibilityMode = 28030  <br/> |Недопустимый режим совместимости.  <br/> |
|AdminInvalidProjectProfessionalVersions = 28031  <br/> |Недопустимый набор версий Project профессиональный.  <br/> |
|AdminInvalidProjectProfessionalVersion = 28032  <br/> |Недопустимая версия Project профессиональный.  <br/> |
|AdminTooManyProjectProfessionalVersions = 28033  <br/> |Указано слишком много версий Project профессиональный.  <br/> |
|AdminDuplicateProjectProfessionalMajorVersions = 28034  <br/> |В основных номерах версий Project профессиональный присутствуют повторения. Вы можете указать только одну версию для каждого основного выпуска, начиная с Project Профессиональный 2007.  <br/> |
|AdminInvalidServerFlags = 28035  <br/> |Один или несколько флагов в параметрах Project Server не являются допустимыми.  <br/> |
|AdminNullProjectProfessionalVersions = 28036  <br/> |Одна или несколько версий Project профессиональный являются пустыми.  <br/> |

<a name="pj15_ErrorCodes_Archive"></a>

## <a name="table-7-archive-web-service"></a>Табл. 7. Веб-служба архивации

|Код ошибки веб-службы архивации (резервное копирование и восстановление)|Описание|
|:-----|:-----|
|ArchiveProjectFailure = 25000  <br/> |Сбой операции архивирования проекта.  <br/> |
|ArchiveProjectsFailed = 25001  <br/> |Не удается сохранить проекты в архивной базе данных.  <br/> |
|ArchiveProjectFailed = 25002  <br/> |Не удается сохранить архив проекта.  <br/> |
|RestoreProjectFailed = 25003  <br/> |Не удается восстановить проект.  <br/> |
|ArchiveResourcesFailed = 25007  <br/> |Не удается сохранить архив ресурсов.  <br/> |
|ArchiveCustomFieldsFailed = 25008  <br/> |Не удается сохранить архив настраиваемых полей.  <br/> |
|RestoreCustomFieldsFailed = 25009  <br/> |Не удается восстановить настраиваемые поля.  <br/> |
|ArchiveSystemSettingsFailed = 25010  <br/> |Не удается сохранить архив параметров системы.  <br/> |
|RestoreSystemSettingsFailed = 25011  <br/> |Не удается восстановить параметры системы.  <br/> |
|ArchiveCategoriesFailed = 25012  <br/> |Не удается сохранить архив категорий безопасности.  <br/> |
|RestoreCategoriesFailed = 25013  <br/> |Не удается восстановить категории безопасности.  <br/> |
|ArchiveViewsFailed = 25014  <br/> |Не удается сохранить архив представлений.  <br/> |
|RestoreViewsFailed = 25015  <br/> |Не удается восстановить представления.  <br/> |
|ArchiveGlobalProjectFailed = 25016  <br/> |Не удается сохранить глобальный корпоративный архив.  <br/> |
|RestoreGlobalProjectFailed = 25017  <br/> |Не удается восстановить глобальный корпоративный шаблон.  <br/> |
|ArchiveInvalidRetentionPolicyValue = 25018  <br/> |Недопустимое значение политики хранения архива.  <br/> |
|ArchiveCustomFieldsFailure = 25019  <br/> |Не удается считать архив настраиваемых полей.  <br/> |
|ArchiveGlobalProjectFailure = 25020  <br/> |Не удается считать глобальный корпоративный архив.  <br/> |
|ArchiveResourcesFailure = 25021  <br/> |Не удается считать архив ресурсов.  <br/> |
|ArchiveSystemSettingsFailure = 25022  <br/> |Не удается считать архив параметров системы.  <br/> |
|ArchiveViewsFailure = 25023  <br/> |Не удается считать архив представлений.  <br/> |
|ArchiveCategoriesFailure = 25024  <br/> |Не удается считать архив категорий безопасности.  <br/> |
|ResourcePlanPublishFailure = 25025  <br/> |Не удается опубликовать план использования ресурсов.  <br/> |
|RestoreCategoriesFailure = 25026  <br/> |Не удается восстановить категории безопасности из архива.  <br/> |
|RestoreCustomFieldsFailure = 25027  <br/> |Не удается восстановить настраиваемые поля из архива.  <br/> |
|RestoreGlobalProjectFailure = 25028  <br/> |Не удается восстановить глобальный корпоративный шаблон из архива.  <br/> |
|RestoreProjectFailure = 25029  <br/> |Не удается восстановить проект из архива.  <br/> |
|RestoreResourcesFailure = 25030  <br/> |Не удается восстановить ресурсы из архива.  <br/> |
|RestoreSystemSettingsFailure = 25031  <br/> |Не удается восстановить параметры системы из архива.  <br/> |
|RestoreViewsFailure = 25032  <br/> |Не удается восстановить представление из архива.  <br/> |
|ArchiveReadProjectArchiveRetentionSettingFailed = 25033  <br/> |Не удалось считать параметры хранения архива проекта.  <br/> |
|RestoreResourcesFailed = 29021  <br/> |Не удается восстановить ресурсы.  <br/> |

<a name="pj15_ErrorCodes_Assignments"></a>

## <a name="table-8-assignment"></a>Табл. 8. Назначение

|Код ошибки назначения|Описание|
|:-----|:-----|
|AssignmentNotFound = 120  <br/> |Назначение не найдено.  <br/> |
|AssignmentWrongTrackingMethod = 122  <br/> |Назначение имеет неправильный метод отслеживания.  <br/> |
|AssignmentWorkTypeInvalid = 127  <br/> |Недопустимый тип трудозатрат назначения.  <br/> |
|AssignmentRateTableInvalid = 130  <br/> |Недопустимая таблица ставок для назначения.  <br/> |
|AssignmentAlreadyExists = 131  <br/> |Это назначение уже существует.  <br/> |
|AssignmentDuplicateSpecified = 132  <br/> |Имеется повторяющееся назначение.  <br/> |
|AssignmentUidInvalid = 133  <br/> |Недопустимый GUID назначения.  <br/> |
|AssignmentDelayInvalid = 134  <br/> |Недопустимая задержка назначения.  <br/> |
|AssignmentCannotEditSummaryTask = 135  <br/> |Для назначений суммарную задачу нельзя изменить.  <br/> |
|AssignmentInvalid = 136  <br/> |Недопустимое назначение.  <br/> |
|AssignmentFieldsInvalidForBudget = 137  <br/> |Поля назначений не являются допустимыми для бюджета.  <br/> |
|AssignmentAlreadyAssignedToResource = 138  <br/> |Этот ресурс уже имеет назначение.  <br/> |
|AssignmentInvalidOwner = 139  <br/> |Владелец назначения является недопустимым.  <br/> |

<a name="pj15_ErrorCodes_Calendar"></a>

## <a name="table-9-calendar"></a>Табл. 9. Календарь

|Код ошибки календаря|Описание|
|:-----|:-----|
|CalendarUidInvalid = 77  <br/> |Недопустимый GUID календаря.  <br/> |
|CalendarOnlyOneShiftIsNull = 13000  <br/> |Значение NULL имеет только одна смена.  <br/> |
|CalendarRecurrenceDaysShouldBeNull = 13001  <br/> |Дни повторения должны иметь значение NULL.  <br/> |
|CalendarRecurrenceMonthDayShouldBeNull = 13002  <br/> |Месяц и день повторения должны иметь значение NULL.  <br/> |
|CalendarRecurrenceMonthShouldBeNull = 13003  <br/> |Месяц повторения должен иметь значение NULL.  <br/> |
|CalendarRecurrenceMonthShouldNotBeNull = 13004  <br/> |Месяц повторения должен иметь значение, отличное от NULL.  <br/> |
|CalendarRecurrencePositionShouldBeNull = 13005  <br/> |Положение повторения должно иметь значение NULL.  <br/> |
|CalendarRecurrencePositionShouldNotBeNull = 13006  <br/> |Положение повторения должно иметь значение, отличное от NULL.  <br/> |
|CalendarRecurrenceDaysShouldNotBeNull = 13007  <br/> |Дни повторения должны иметь значение, отличное от NULL.  <br/> |
|CalendarInvalidRecurrenceFrequency = 13008  <br/> |Недопустимая частота повторения.  <br/> |
|CalendarInvalidRecurrenceType = 13009  <br/> |Недопустимый тип повторения.  <br/> |
|CalendarInvalidRecurrenceDays = 13010  <br/> |Недопустимые дни повторения.  <br/> |
|CalendarInvalidCombinationOfMonthDayAndPosition = 13011  <br/> |Недопустимое сочетание месяца, для и положения.  <br/> |
|CalendarInvalidRecurrencePosition = 13012  <br/> |Недопустимое положение повторения.  <br/> |
|CalendarCannotModifyExceptionsForCalendarBeingDeleted = 13013  <br/> |Исключения календаря нельзя изменить во время его удаления.  <br/> |
|CalendarExceptionConflict = 13014  <br/> |Конфликт в исключениях календаря.  <br/> |
|CalendarBadDateValue = 13015  <br/> |Недопустимая дата.  <br/> |
|CalendarNotFound = 13021  <br/> |Календарь не найден.  <br/> |
|CalendarAlreadyExists = 13022  <br/> |Календарь уже существует.  <br/> |
|CalendarNameShouldNotBeNull = 13023  <br/> |Имя календаря имеет значение NULL.  <br/> |
|CalendarInternalError = 13025  <br/> |Внутренняя ошибка в операции календаря.  <br/> |
|CalendarNameTooLong = 13027  <br/> |Слишком длинное имя календаря.  <br/> |
|CalendarInvalidCalendarName = 13028  <br/> |Недопустимое имя календаря.  <br/> |
|CalendarStandardCalendarNotFound = 13031  <br/> |Стандартный календарь не найден.  <br/> |
|CalendarInvalidShifts = 13032  <br/> |Недопустимые смены.  <br/> |
|CalendarCannotDeleteCalendarUsedByProject = 13033  <br/> |Не удается удалить календарь, используемый в проекте.  <br/> |
|CalCalendarUniqueIdToDuplicateShouldBeNull = 13035  <br/> |Для дублирования календаря GUID должен иметь значение NULL.  <br/> |
|CalendarInvalidBaseCalendarUniqueId = 13037  <br/> |Недопустимый GUID базового календаря.  <br/> |
|CalendarInvalidUniqueIdToDuplicate = 13038  <br/> |Недопустимый GUID для дублирования календаря.  <br/> |
|CalendarUnusedCalendarException = 13039  <br/> |Исключение календаря не имеет соответствующего календаря. Это происходит, если метод **UpdateResources** используется тогда, когда в таблице **ResourceDataSet.CalendarExceptions** есть запись, однако нет **BaseCalendarUniqueId** для этого ресурса в таблице **Resources**.<br/> |
|CalendarCannotDeleteStandardCalendar = 13040  <br/> |Стандартный календарь нельзя удалить.  <br/> |
|CalendarCannotRenameStandardCalendar = 13041  <br/> |Стандартный календарь нельзя переименовать.  <br/> |
|CalendarCannotDeleteCalendarUsedByEnterpriseResource = 13042  <br/> |Этот календарь используется корпоративным ресурсом и не может быть удален.  <br/> |
|CalendarFilterInvalid = 13043  <br/> |Фильтр для календаря является недопустимым.  <br/> |

<a name="pj15_ErrorCodes_CBS"></a>

## <a name="table-10-cubeadmin-and-cube-build-service"></a>Табл. 10. CubeAdmin и служба построения куба

|Код ошибки CubeAdmin и службы построения куба (CBS)|Описание|
|:-----|:-----|
|CBSGeneralFailure = 17001  <br/> |Сбой в службе построения куба (CBS). Это код общей ошибки, который может быть вызван множеством разных причин.  <br/> |
|CBSDsoNotInstalled = 17002  <br/> |Службе CBS требуется установленный компонент объектов поддержки принятия решений (DSO) для служб Analysis Services.  <br/> |
|CBSASConnectionFailure = 17003  <br/> |Службе CBS не удалось подключиться к серверу служб Analysis Services.  <br/> |
|CBSOlapProcessingFailure = 17004  <br/> |Сбой обработки куба OLAP.  <br/> |
|CBSMetadataProcessingFailure = 17005  <br/> |Сбой обработки метаданных куба.  <br/> |
|CBSASServerLockTimeOut = 17006  <br/> |Истекло время ожидания для блокировки сервера служб Analysis Services.  <br/> |
|CBSOlapDatabaseSetupFailure = 17007  <br/> |Сбой настройки базы данных кубов OLAP.  <br/> |
|CBSASEntityLimitation = 17008  <br/> |Превышено число сущностей, которое могут использовать службы Analysis Services.  <br/> |
|CBSRequestInvalidArguments = 17009  <br/> |Один или несколько аргументов в запросе CBS не являются допустимыми.  <br/> |
|CBSQueueingRequestFailed = 17010  <br/> |Службе CBS не удалось отправить задание в очередь.  <br/> |
|CBSUpdateCubeCalculatedMeasureDefintionError = 17011  <br/> |Ошибка в вычисляемом элементе куба.  <br/> |
|CBSAttemptToOverwrite = 17013  <br/> |Не удается перезаписать данные в кубе.  <br/> |
|CBSCustomFieldCannotBeAddedAsDimension = 17014  <br/> |Настраиваемое поле не может быть измерением куба.  <br/> |
|CBSCustomFieldFailedToBeAddedAsDimension = 17015  <br/> |Не удалось добавить настраиваемое поле в качестве измерения в куб.  <br/> |
|CBSCustomFieldCannotBeAddedAsMeasure = 17016  <br/> |Настраиваемое поле не может быть показателем куба.  <br/> |
|CBSCustomFieldFailedToBeAddedAsMeasure = 17017  <br/> |Не удалось добавить настраиваемое поле в качестве показателя в куб.  <br/> |
|CBSDsoTranslatorNotFound = 17018  <br/> |Не найден транслятор объектов поддержки принятия решений (DSO).  <br/> |
|CBSUpdateOlapDBOperationFailure = 17019  <br/> |Не удалось обновить базу данных OLAP.  <br/> |
|CBSOlapDBInvalidArguments = 17020  <br/> |Один или несколько аргументов для базы данных OLAP не являются допустимыми.  <br/> |
|CBSOlapDatabaseReadSettingListFailed = 17021  <br/> |Не удалось считать список параметров базы данных OLAP.  <br/> |
|CBSOlapDatabaseReadSettingFailed = 17022  <br/> |Не удалось считать параметр базы данных OLAP.  <br/> |
|CBSDeleteOlapDatabaseSetting = 17023  <br/> |Ошибка при удалении параметра базы данных OLAP.  <br/> |
|CBSSetDefaultOlapDatabase = 17024  <br/> |Ошибка при настройке базы данных OLAP по умолчанию.  <br/> |
|CBSSetOlapDatabaseEnabled = 17025  <br/> |Ошибка при включении базы данных OLAP.  <br/> |
|CBSGetDefaultOlapDatabase = 17026  <br/> |Ошибка при получении базы данных OLAP по умолчанию.  <br/> |
|CBSCustomFieldFailedToBeAddedAsDimensionOrMeasure = 17027  <br/> |Не удается добавить настраиваемое поле в качестве измерения или показателя.  <br/> |
|CBSOlapDatabaseAssocFieldsSettings = 17028  <br/> |Ошибка в параметрах полей, сопоставленных с базой данных OLAP.  <br/> |
|CBSUpdateOlapDBOperationDuplicateOrFailure = 17029  <br/> |Сбой или повторение операции обновления базы данных OLAP.  <br/> |
|CBSErrorReadingDefaultDatabase = 17030  <br/> |Ошибка при считывании базы данных OLAP по умолчанию.  <br/> |
|CBSCreateOlapDBOperationFailure = 17031  <br/> |Не удалось создать операцию базы данных OLAP.  <br/> |
|CBSSetCubeFieldsSettingsFromListForGroupMeasureFailed = 17032  <br/> |Не удалось задать список для параметров групповых показателей полей куба.  <br/> |
|CBSErrorReadingCubeDepartments = 17033  <br/> |Ошибка при считывании отделов в кубе OLAP.  <br/> |
|CBSErrorMaxOlapDatabaseCountReached = 17034  <br/> |Достигнуто максимальное число баз данных OLAP.  <br/> |
|CBSErrorReadingCubeFieldsSettings = 17035  <br/> |Ошибка чтения параметров полей куба.  <br/> |

<a name="pj15_ErrorCodes_CICO"></a>

## <a name="table-11-check-in-and-check-out"></a>Табл. 11. Возвращение и извлечение

|Код ошибки возвращения — извлечения|Описание|
|:-----|:-----|
|CICOCheckedOutToOtherUser = 10100  <br/> |Извлечено другому пользователю.  <br/> |
|CICOAlreadyCheckedOutToYou = 10101  <br/> |Уже извлечено вам.  <br/> |
|CICONotCheckedOut = 10102  <br/> |Не извлечено.  <br/> |
|CICOCheckedOutInOtherSession = 10103  <br/> |Извлечено в другом сеансе.  <br/> |
|CICOInvalidSessionGuid = 10104  <br/> |Недопустимый GUID сеанса.  <br/> |
|CICOAlreadyCheckedOutInSameSession = 10105  <br/> |Уже извлечено в том же сеансе.  <br/> |
|CICOCannotCheckOutVisibilityModeProjectWithMppInDocLib = 10106  <br/> |Невозможно извлечь проект в режиме видимости, если MPP-файл находится в библиотеке документов.  <br/> |

<a name="pj15_ErrorCodes_CustomFields"></a>

## <a name="table-12-custom-field"></a>Табл. 12 Настраиваемое поле

|Код ошибки настраиваемого поля|Описание|
|:-----|:-----|
|CustomFieldInvalidPropertyType = 11500  <br/> |Недопустимый тип свойства.  <br/> |
|CustomFieldInvalidScope = 11503  <br/> |Недопустимая область настраиваемого поля.  <br/> |
|CustomFieldScopesMustBeIdentical = 11504  <br/> |Области должны быть идентичны друг другу.  <br/> |
|CustomFieldInvalidEntityUID = 11505  <br/> |Недопустимый GUID сущности настраиваемого поля.  <br/> |
|CustomFieldHasInvalidPropertiesForNonLookupTableCF = 11506  <br/> |Недопустимые свойства для настраиваемого поля, не имеющего таблицу подстановки.  <br/> |
|CustomFieldNonExistentWeightsTableUID = 11507  <br/> |GUID таблицы весовых коэффициентов не существует.  <br/> |
|CustomFieldInvalidName = 11508  <br/> |Недопустимое имя настраиваемого поля.  <br/> |
|CustomFieldInvalidDefault = 11510  <br/> |Недопустимое значение по умолчанию для настраиваемого поля.  <br/> |
|CustomFieldInvalidLookupTableUID = 11511  <br/> |Недопустимый GUID таблицы подстановки.  <br/> |
|CustomFieldTypeDoesNotMatchLookupTableMask = 11512  <br/> |Тип настраиваемого поля не соответствует маске таблицы подстановки.  <br/> |
|CustomFieldCannotHaveNonLeafNodeDefault = 11513  <br/> |Значение по умолчанию настраиваемого поля должно быть листовым узлом.  <br/> |
|CustomFieldMatchingOnlyAvailableForResources = 11514  <br/> |Соответствующее настраиваемое поле доступно только для ресурсов.  <br/> |
|CustomFieldUIDCannotMatchLookupTableUID = 11516  <br/> |GUID не совпадает с GUID таблицы подстановки.  <br/> |
|CustomFieldUIDAlreadyExists = 11517  <br/> |GUID настраиваемого поля уже существует.  <br/> |
|CustomFieldIDAlreadyExists = 11518  <br/> |Идентификационный номер настраиваемого поля уже существует.  <br/> |
|CustomFieldNameAlreadyExists = 11519  <br/> |Имя настраиваемого поля уже существует.  <br/> |
|CustomFieldInvalidEntity = 11520  <br/> |Недопустимая сущность для настраиваемого поля.  <br/> |
|CustomFieldMaskDoesNotMatchEntityType = 11521  <br/> |Маска кода не совпадает с типом сущности.  <br/> |
|CustomFieldLowerOrderBitsOutOfRange = 11522  <br/> |Младшие биты находятся вне диапазона.  <br/> |
|CustomFieldInvalidMaxValues = 11523  <br/> |Одно или несколько максимальных значений не являются допустимыми.  <br/> |
|CustomFieldCannotModifyCertainValuesOnceDefined = 11524  <br/> |Некоторые значения нельзя изменить после их определения.  <br/> |
|CustomFieldNonExistentPID = 11526  <br/> |Идентификационный номер свойства настраиваемого поля не существует.  <br/> |
|CustomFieldCannotChangeBuiltInFields = 11527  <br/> |Не удается изменить встроенные поля Project Server, такие как "Тип затрат", "Состояние" и "СДРес".  <br/> |
|CustomFieldSecondaryUidCannotEqualUid = 11528  <br/> |Дополнительный GUID не может быть идентичен основному GUID.  <br/> |
|CustomFieldCannotHaveSecondaryUIDorIDForThisEntityType = 11529  <br/> |Настраиваемое поле не может иметь дополнительный GUID или GUID для этого типа сущности.  <br/> |
|CustomFieldNameMatchesIntrinsicField = 11530  <br/> |Имя настраиваемого поля соответствует встроенному полю.  <br/> |
|CustomFieldInvalidAggregationType = 11531  <br/> |Недопустимый тип объединения.  <br/> |
|CustomFieldProjectFormulaFieldsMustUseFormulaAggregation = 11532  <br/> |Поля формул в проекте должны использовать объединение формул.  <br/> |
|CustomFieldMustSpecifyEitherIDorUID = 11700  <br/> |Следует указать идентификационный номер или GUID настраиваемого поля.  <br/> |
|CustomFieldInvalidID = 11701  <br/> |Недопустимый идентификационный номер настраиваемого поля.  <br/> |
|CustomFieldInvalidUID = 11702  <br/> |Недопустимый GUID настраиваемого поля.  <br/> |
|CustomFieldInvalidType = 11703  <br/> |Недопустимый тип настраиваемого поля.  <br/> |
|CustomFieldInvalidTypeColumnFilledIn = 11704  <br/> |Значение столбца типа настраиваемого поля является недопустимым. См. [пример кода ошибки для WCF](#pj15_ErrorCodes_WCFExample).  <br/> |
|CustomFieldCodeValueDoesNotMatchLookupTable = 11706  <br/> |Значение кода не совпадает с таблицей подстановки.  <br/> |
|CustomFieldCodeValueIsNotLeafNode = 11707  <br/> |Значение кода не является листовым узлом таблицы подстановки.  <br/> |
|CustomFieldRowAlreadyExists = 11708  <br/> |Эта строка настраиваемого поля уже существует.  <br/> |
|CustomFieldRowDoesNotMatchCorrespondingDefinitionInDB = 11710  <br/> |Строка настраиваемого поля не соответствует определению базы данных.  <br/> |
|CustomFieldCodeValueAlreadyUsed = 11711  <br/> |Это значение кода уже используется.  <br/> |
|CustomFieldMaxValuesExceeded = 11712  <br/> |Превышено максимальное число значение настраиваемых полей.  <br/> |
|CustomFieldRequiredValueNotProvided = 11713  <br/> |Необходимое значение настраиваемого поля не предоставлено. См. [пример кода ошибки для WCF](#pj15_ErrorCodes_WCFExample).  <br/> |
|CustomFieldCannotChangeLookupTable = 11715  <br/> |Не удается изменить таблицу подстановки настраиваемого поля.  <br/> |
|CustomFieldFilterInvalid = 11716  <br/> |Недопустимый фильтр настраиваемого поля.  <br/> |
|CustomFieldRolldownInvalidOnFormulaFields = 11717  <br/> |Не удается выполнить развертывание в настраиваемом поле формул.  <br/> |
|CustomFieldFormulaFieldCannotBeRequired = 11718  <br/> |Поле формул не может быть обязательным.  <br/> |
|CustomFieldFormulaFieldCannotBeWorkflowControlled = 11719  <br/> |Поле формул не может управляться рабочим процессом.  <br/> |
|CustomFieldCannotSetValueOnFormulaFields = 11720  <br/> |Не удается установить значение для полей формул.  <br/> |
|CustomFieldNewPerRequestLimitExcedeed = 11721  <br/> |Превышено ограничение запроса для новых настраиваемых полей. Ограничение составляет [NEW_CF_PER_REQUEST_LIMIT](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.CustomField.NEW_CF_PER_REQUEST_LIMIT.aspx) в одном запросе.  <br/> |
|CustomFieldNameIsReservedName = 11722  <br/> |Имя настраиваемого поля не может быть зарезервированным именем.  <br/> |
|CustomFieldNameInvalidForOlapMeasure = 11723  <br/> |Имя настраиваемого поля не является допустимым для показателя куба OLAP.  <br/> |
|CustomFieldNameInvalidForOlapDimension = 11724  <br/> |Имя настраиваемого поля не является допустимым для измерения куба OLAP.  <br/> |
|CustomFieldSettingsInvalidForOlapMeasure = 11725  <br/> |Параметры настраиваемого поля не являются допустимыми для показателя куба OLAP.  <br/> |
|CustomFieldSettingsInvalidForOlapDimension = 11726  <br/> |Параметры настраиваемого поля не являются допустимыми для измерения куба OLAP.  <br/> |
|CustomFieldCannotAddRelativeImportanceField = 11727  <br/> |Не удается добавить поле относительной важности.  <br/> |
|CustomFieldCannotAddProjectImpactField = 11728  <br/> |Не удается добавить поле влияния проекта.  <br/> |
|CustomFieldInvalidDepartmentUid = 11731  <br/> |Недопустимый GUID отдела для настраиваемого поля.  <br/> |
|CustomFieldCannotModifyDepartmentUidOnBuiltinFields = 11732  <br/> |GUID отдела нельзя изменить во встроенных настраиваемых полях.  <br/> |
|CustomFieldCannotHaveBothLookupTableAndMultilineText = 11733  <br/> |Настраиваемое поле не может включать в себя как таблицу подстановки, так и многострочный текст.  <br/> |
|CustomFieldCannotHaveBothFormulaAndMultilineText = 11734  <br/> |Настраиваемое поле не может включать в себя как формулу, так и многострочный текст.  <br/> |
|CustomFieldDescriptionExceedsLimit = 11735  <br/> |Слишком большое описание настраиваемого поля. Максимальная длина свойства **MD_PROP_DESCRIPTION** — 1000 знаков.  <br/> |
|CustomFieldOnlyTextFieldsCanHaveMultilineText = 11736  <br/> |Многострочный текст могут содержать только текстовые настраиваемые поля.  <br/> |
|CustomFieldOnlyProjectFieldsCanHaveMultilineText = 11737  <br/> |Многострочный текст могут содержать только настраиваемые поля проекта.  <br/> |
|CustomFieldCannotChangeWorkflowControlledBehaviorForNonProjectCustomFields = 11738  <br/> |Настраиваемое поле не может изменить режим работы настраиваемых полей вне проекта, управляемых рабочим процессом.  <br/> |
|CustomFieldIsWorkflowControlledAndCannotBeChanged = 11739  <br/> |Настраиваемое поле управляется рабочим процессом и не может быть изменено.  <br/> |
|CustomFieldCannotHaveRequiredFlagWhenWorkflowControlledFlagIsSet = 11740  <br/> |Настраиваемое поле не может быть обязательным, когда оно управляется рабочим процессом.  <br/> |
|CustomFieldFormulaCreatesCircularReference = 11742  <br/> |Формула настраиваемого поля создает циклическую ссылку.  <br/> |
|CustomFieldFormulaContainsInvalidFieldReference = 11743  <br/> |Формула настраиваемого поля содержит недопустимую ссылку на поле.  <br/> |
|CustomFieldFormulaContainsErrors = 11744  <br/> |Формула настраиваемого поля содержит одну или несколько ошибок.  <br/> |
|CustomFieldLocalCustomFieldNotDefined = 11745  <br/> |Локальное настраиваемое поле не определено.  <br/> |
|CustomFieldGraphicalIndicatorContainsErrors = 11746  <br/> |Графический индикатор настраиваемого поля содержит ошибки.  <br/> |
|CustomFieldGraphicalIndicatorContainsInvalidFieldReference = 11747  <br/> |Графический индикатор настраиваемого поля содержит недопустимую ссылку на поле.  <br/> |
|CustomFieldGraphicalIndicatorTypeMismatch = 11748  <br/> |Для графического индикатора настраиваемого поля имеет место несоответствие типов.  <br/> |
|CustomFieldFormulaFieldCannotReferenceWorkflowControlledField = 11749  <br/> |Поле в формуле не может ссылаться на поле, управляемое рабочим процессом.  <br/> |
|CustomFieldWorkflowCustomFieldBeingReferencedByFormula = 11750  <br/> |Формула пытается сослаться на настраиваемое поле рабочего процесса.  <br/> |

<a name="pj15_ErrorCodes_LookupTables"></a>

## <a name="table-13-lookup-table"></a>Табл. 13. Таблица подстановки

|Код ошибки таблицы подстановки|Описание|
|:-----|:-----|
|LookupTableMaskNotDefined = 11000  <br/> |Маска кода таблицы подстановки не определена.  <br/> |
|LookupTableMaskHasTooManyValues = 11001  <br/> |Маска кода таблицы подстановки имеет слишком много значений.  <br/> |
|LookupTableMaskHasGaps = 11002  <br/> |Маска кода таблицы подстановки имеет пробелы.  <br/> |
|LookupTableMaskSequenceTypeLimitedToOneLevelDeep = 11003  <br/> |Тип последовательности маски кода ограничен одним уровнем.  <br/> |
|LookupTableMaskSequenceTypeInvalid = 11004  <br/> |Недопустимый тип последовательности маски кода.  <br/> |
|LookupTableMaskSequenceRequiresAnyLength = 11005  <br/> |Для последовательности маски кода требуется длина _Any_.  <br/> |
|LookupTableMaskSeparatorTooLong = 11006  <br/> |Разделитель маски кода содержит слишком много символов.  <br/> |
|LookupTableMaskLevelMustBeBlankAcrossLCIDs = 11007  <br/> |Уровень маски кода должен быть пустым для всех кодов (или идентификаторов) языка.  <br/> |
|LookupTableMaskSeparatorInvalid = 11008  <br/> |Недопустимый знак разделителя маски кода.  <br/> |
|LookupTableMaskBlankSeparatorInvalidAfterAnyLengthSequence = 11009  <br/> |Пустой знак разделителя является недопустимым после длины последовательности _Any_.  <br/> |
|LookupTableMaskSequenceLengthInvalid = 11010  <br/> |Недопустимая длина последовательности маски кода.  <br/> |
|LookupTableMaskLevelMustBeOneOrMore = 11011  <br/> |Маска кода должна относиться к 1 или более высокому уровню.  <br/> |
|LookupTableItemDoesNotFitMask = 11050  <br/> |Элемент таблицы подстановки не соответствует определению маски кода.  <br/> |
|LookupTableItemContainsSeparator = 11051  <br/> |Элемент таблицы подстановки содержит знак разделителя.  <br/> |
|LookupTableItemFullValueTooLong = 11052  <br/> |Слишком длинное полное значение элемента таблицы подстановки.  <br/> |
|LookupTableDuplicateSiblingsDisallowed = 11053  <br/> |Дублирование элементов того же уровня в таблице подстановки запрещено.  <br/> |
|LookupTableSortOrderIndexInvalid = 11054  <br/> |Недопустимый индекс для порядка сортировки таблицы подстановки.  <br/> |
|LookupTableSortOrderIndexDuplicate = 11055  <br/> |Повторяющийся индекс для порядка сортировки таблицы подстановки.  <br/> |
|LookupTableSortOrderTypeInvalid = 11056  <br/> |Недопустимый тип порядка сортировки таблицы подстановки.  <br/> |
|LookupTableSortOrderMustComeAfterParentSortOrder = 11057  <br/> |Порядок сортировки должен следовать за родительским порядком сортировки.  <br/> |
|LookupTableSortOrderMustComeBeforeParentNextSiblingSortOrder = 11058  <br/> |Порядок сортировки должен предшествовать родительскому элементу порядка сортировки следующего элемента того же уровня.  <br/> |
|LookupTableInvalidCookieLength = 11060  <br/> |Недопустимая длина файла cookie для таблицы подстановки.  <br/> |
|LookupTableMustHaveValuesForPrimaryLCIDorJustOneValue = 11061  <br/> |Таблица подстановки должна иметь значения для основного кода (или идентификатора) языка либо всего одно значение. Например, при создании многоязыковой таблицы подстановки добавьте только одно значение маски для каждого уровня или сначала добавьте значение основного кода языка.  <br/> |
|LookupTableLCIDNotSupportedInLookupTableLanguages = 11062  <br/> |Код (или идентификатор) языка не включен в языки таблицы подстановки.  <br/> |
|LookupTableInvalidDescriptionLength = 11063  <br/> |Недопустимая длина описания для элемента таблицы подстановки.  <br/> |
|LookupTableCannotChangeBuiltInTables = 11064  <br/> |Не удается изменить встроенные таблицы подстановки.  <br/> |
|LookupTableCannotChangeTypeOnceCreated = 11065  <br/> |Не удается изменить тип таблицы подстановки после ее создания.  <br/> |
|LookupTableCannotDeleteLTWithDependantCustomField = 11066  <br/> |Не удается удалить таблицу подстановки, используемую в настраиваемом поле.  <br/> |
|LookupTableAllLevelsNotFilled = 11067  <br/> |Должны быть заполнены все уровни таблицы подстановки.  <br/> |
|LookupTableDuplicateName = 11068  <br/> |Имена таблиц подстановки должны быть уникальными.  <br/> |
|LookupTableInvalidName = 11069  <br/> |Недопустимое имя таблицы подстановки.  <br/> |
|LookupTableDuplicateSiblingPhoneticsDisallowed = 11071  <br/> |Наличие повторяющихся фонетических названий элемента того же уровня в таблице подстановки запрещено.  <br/> |
|LookupTableItemInvalidLookupTable = 11073  <br/> |Недопустимый элемент в таблице подстановки.  <br/> |
|LookupTableInvalidPhoneticsLength = 11074  <br/> |Недопустимая длина фонетического названия настраиваемого поля.  <br/> |
|LookupTableAlreadyExists = 11076  <br/> |Таблица подстановки уже существует.  <br/> |
|LookupTableInvalidUID = 11078  <br/> |Недопустимый GUID таблицы подстановки.  <br/> |
|LookupTableFilterInvalid = 11079  <br/> |Недопустимый фильтр таблицы подстановки.  <br/> |
|LookupTableLanguageParameterInvalidWithXmlFilter = 11080  <br/> |Параметр языка является недопустимым при использовании параметра _xmlFilter_ таблицы подстановки.  <br/> |
|LookupTableInvalidParentStructUid = 11081  <br/> |Недопустимый GUID для родительской структуры таблицы подстановки.  <br/> |
|LookupTableItemContainsListSeparator = 11082  <br/> |Элемент таблицы подстановки содержит разделитель элементов списка.  <br/> |
   
Коды ошибок в таблице 14 включают в себя элементы для страниц сведений о проекте (PDP), синхронизации Exchange, временной шкалы Project Web App и ошибок баз данных. Многие из кодов прочих ошибок в таблице 14 предназначены для внутреннего использования.
  
> [!NOTE]
> Коды ошибок аудита в Project Server 2013 не используются. 

<a name="pj15_ErrorCodes_Miscellaneous"></a>

## <a name="table-14-miscellaneous-error-codes"></a>Табл. 14. Коды прочих ошибок

|Код прочих ошибок|Описание|
|:-----|:-----|
|AuditingUpdateFailure = 31000  <br/> |Не используется.  <br/> |
|AuditingCannotDeleteFeature = 31001  <br/> |Не используется.  <br/> |
|AuditingCannotAddFeature = 31002  <br/> |Не используется.  <br/> |
|AuditingFeatureIsNoLongerAudited = 31003  <br/> |Не используется.  <br/> |
|AuditingItemIsNotYetAvailable = 31004  <br/> |Не используется.  <br/> |
|AuditingInvalidFeatureUid = 31005  <br/> |Не используется.  <br/> |
|AuditingInvalidStoreForSelectedFeature = 31006  <br/> |Не используется.  <br/> |
|AuditingInvalidStore = 31007  <br/> |Не используется.  <br/> |
|AuditingVersionNameTooLong = 31008  <br/> |Не используется.  <br/> |
|AuditingBeginVersionFailure = 31009  <br/> |Не используется.  <br/> |
|AuditingEndVersionFailure = 31010  <br/> |Не используется.  <br/> |
|ProjectDetailPagesStrategicImpactRatingRequired = 32000  <br/> |Для страницы сведений о проекте требуется оценка стратегического влияния.  <br/> |
|ProjectDetailPagesMissingPDPLinks = 32001  <br/> |Отсутствуют ссылки на страницы со сведениями о проекте.  <br/> |
|ProjectDetailPagesUnavailableWorker = 32002  <br/> |Сбой загрузки детализации проекта. Нет доступных работников.  <br/> |
|ProjectDetailPagesFailedToLoadProjectInWorker = 32003  <br/> |Сбой при загрузке работника.  <br/> |
|AppPermissionInvalidAppPermissionId = 32300  <br/> |Проблема с идентификатором разрешения приложения.  <br/> |
|InvariantValidationPSIFailed = 40000  <br/> |Возвращается методами **PWA**, если любой из частных методов возвращает **ValidationMethodFailed**. Для внутреннего использования.  <br/> |
|ValidationMethodFailed = 40001  <br/> |Возвращается частными методами **PWA** при обнаружении ими несоответствий базы данных. Для внутреннего использования.  <br/> |
|GeneralExchangeSyncError = 40500  <br/> |Общая ошибка при синхронизации Microsoft Exchange. Для внутреннего использования.  <br/> |
|ExchangeSyncRootFolderCreationFailed = 40501  <br/> |Не удалось создать корневую папку при синхронизации Microsoft Exchange.  <br/> |
|ExchangeSyncTaskFolderCreationFailed = 40502  <br/> |Не удалось создать папку задач.  <br/> |
|ExchangeSyncCouldNotGetRootFolder = 40503  <br/> |Не удалось получить корневую папку.  <br/> |
|ExchangeSyncCouldNotLoadTaskObject = 40504  <br/> |Не удалось загрузить объект задачи.  <br/> |
|ExchangeSyncNewExchangeTaskCreationFailed = 40505  <br/> |Сбой создания новой задачи при синхронизации Exchange.  <br/> |
|ExchangeSyncFailedToUpdateCacheForUser = 40506  <br/> |Не удалось обновить кэш синхронизации Exchange для пользователя.  <br/> |
|ExchangeSyncFailedToUpdateExchangeTask = 40507  <br/> |Не удалось обновить задачу в Microsoft Exchange.  <br/> |
|ExchangeSyncSubscriptionUpdateFailed = 40508  <br/> |Не удалось обновить подписку на синхронизацию Exchange.  <br/> |
|ExchangeSyncEWSUrlFailed = 40509  <br/> |Сбой URL-адреса веб-службы Microsoft Exchange.  <br/> |
|ExchangeSyncExchangeUrlRefreshFailed = 40510  <br/> |Не удалось обновить URL-адрес Exchange.  <br/> |
|ExchangeSyncExchangeSubscriptionUpdateForUserFailed = 40511  <br/> |Не удалось обновить подписку Exchange для пользователя.  <br/> |
|ExchangeSyncGeneralProcessingFailure = 40512  <br/> |Общий сбой обработки при синхронизации Microsoft Exchange.  <br/> |
|ExchangeSyncDeletionOfTasksInExchangeFailure = 40513  <br/> |Не удалось удалить задачи при синхронизации Exchange.  <br/> |
|ExchangeSyncAttemptedSyncOfInvalidConfiguredResource = 40514  <br/> |Предпринята попытка синхронизации ресурса с недопустимой конфигурацией.  <br/> |
|ExchangeSyncRetrievalOfEWSUrlCausedException = 40515  <br/> |Во время извлечения веб-службы Exchange возникло исключение.  <br/> |
|TimelineViewDataDoesNotExist = 42000  <br/> |Данные не существуют в представлении временной шкалы в Project Web App.  <br/> |
|DatabaseUndefinedError = 50000  <br/> |База данных не определена.  <br/> |
|DatabaseCannotInsertDuplicateKeyError = 50001  <br/> |Базе данных не удается вставить дублируемый ключ.  <br/> |

<a name="pj15_ErrorCodes_Notifications"></a>

## <a name="table-15-notification"></a>Табл. 15. Уведомление

|Код ошибки уведомления|Описание|
|:-----|:-----|
|NotificationReminderUnknown = 16050  <br/> |Неизвестное уведомление с напоминанием.  <br/> |
|NotificationReminderParentNotSubscribed = 16051  <br/> |Отсутствует подписка на родительский элемент уведомления с напоминанием.  <br/> |
|NotificationReminderParentNotFound = 16052  <br/> |Родительский элемент уведомления с напоминанием не найден.  <br/> |
|NotificationReminderChildStillSubscribed = 16053  <br/> |Все еще присутствует подписка на дочерний элемент уведомления с напоминанием.  <br/> |
|NotificationReminderChildNotFound = 16054  <br/> |Дочерний элемент уведомления с напоминанием не найден.  <br/> |
|NotificationEMailDeliveryFailed = 16080  <br/> |Сбой доставки сообщения электронной почты с уведомлением.  <br/> |
|NotificationQueueMessageFailed = 16082  <br/> |Сбой сообщения в очереди уведомлений.  <br/> |
|NotificationXSLTTransformationError = 16084  <br/> |Ошибка в преобразовании XSLT уведомления.  <br/> |
   
Все коды ошибок в таблице 16 предназначены для оптимизатора, который является компонентом, используемым в анализе портфеля проектов.

<a name="pj15_ErrorCodes_Optimizer"></a>

## <a name="table-16-optimizer-project-portfolio-analysis"></a>Табл. 16. Оптимизатор (анализ портфеля проектов)

|Код ошибки оптимизатора|Описание|
|:-----|:-----|
|OptimizerDepInvalidDepType = 29000  <br/> |Значение оптимизатора **DEPENDENCY_TYPE** в [OptimizerDependencyDataSet.OptimizerDependenciesRow](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.OptimizerDependencyDataSet.OptimizerDependenciesRow.aspx) является недопустимым. См. статью [Optimizer.DependencyTypes](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Optimizer.DependencyTypes.aspx) .  <br/> |
|OptimizerDepInvalidEntityType = 29001  <br/> |Тип объекта является недопустимым. См. свойство [Entities](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.EntityCollection.Entities.aspx).  <br/> |
|OptimizerDepInvalidPosition = 29003  <br/> |Значение [POSITION](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.OptimizerDependencyDataSet.OptimizerDependencyDetailsRow.POSITION.aspx) является недопустимым.  <br/> |
|OptimizerDepDuplicateDependentProjects = 29004  <br/> |В [OptimizerDependencyDataSet.OptimizerDependencyDetailsDataTable](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.OptimizerDependencyDataSet.OptimizerDependencyDetailsDataTable.aspx) имеются повторяющиеся проекты.  <br/> |
|OptimizerDepInvalidDependency = 29005  <br/> |Недопустимая зависимость оптимизатора.  <br/> |
|OptimizerDepCircularDependency = 29006  <br/> |Имеется циклическая зависимость.  <br/> |
|OptimizerCannotDeleteDependency = 29007  <br/> |Не удается удалить зависимость.  <br/> |
|OptimizerCannotCreateDependency = 29008  <br/> |Не удается создать зависимость.  <br/> |
|OptimizerCannotUpdateDependency = 29009  <br/> |Не удается обновить зависимость.  <br/> |
|OptimizerCannotCreateMultipleDependencies = 29010  <br/> |Не удается создать несколько зависимостей.  <br/> |
|OptimizerCannotUpdateMultipleDependencies = 29011  <br/> |Не удается обновить несколько зависимостей.  <br/> |
|OptimizerEngineMatrixNotFilled = 29100  <br/> |Оптимизатору недостаточно данных для выполнения расчета.  <br/> |
|OptimizerEngineCustomFieldIsNotAConstraint = 29101  <br/> |Настраиваемое поле не является ограничением для оптимизатора.  <br/> |
|OptimizerCouldNotCalculatePrioritiesFromCustomFields = 29102  <br/> |Не удается рассчитать приоритеты по указанным настраиваемым полям.  <br/> |
|OptimizerEngineBinaryInfeasibleSolution = 29103  <br/> |Результаты расчета оптимизатора в недопустимом решении.  <br/> |
|OptimizerEngineBinaryNumericalError = 29104  <br/> |Математическая ошибка в расчете оптимизатора.  <br/> |
|OptimizerEngineBinaryTimedOut = 29105  <br/> |Истекло время ожидания расчета оптимизатора.  <br/> |
|OptimizerEngineBinaryMaxedIterations = 29106  <br/> |Для расчета оптимизатора выполнено максимальное число итераций.  <br/> |
|OptimizerEngineBinarySubOptimal = 29107  <br/> |Неоптимальные результаты расчета оптимизатора.  <br/> |
|OptimizerEngineBinaryInternalError = 29108  <br/> |Внутренняя ошибка в расчете оптимизатора.  <br/> |
|OptimizerInvalidRange = 29200  <br/> |Недопустимый диапазон данных для оптимизатора.  <br/> |
|OptimizerNonNormalizedWeights = 29201  <br/> |Значения **WEIGHT** в [AnalysisDataSet.AnalysisPriorityDataDataTable](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.AnalysisDataSet.AnalysisPriorityDataDataTable.aspx) не нормализованы.  <br/> |
|OptimizerCannotEditPrioritization = 29300  <br/> |Не удается изменить определение приоритетов целей.  <br/> |
|OptimizerCannotDeletePrioritization = 29301  <br/> |Не удается удалить определение приоритетов целей.  <br/> |
|OptimizerCannotCreatePrioritization = 29302  <br/> |Не удается создать определение приоритетов целей.  <br/> |
|OptimizerCannotUpdatePrioritization = 29303  <br/> |Не удается обновить определение приоритетов целей.  <br/> |
|OptimizerCannotCalculateDriverPriorities = 29304  <br/> |Не удается вычислить приоритеты целей.  <br/> |
|OptimizerCannotCreateMultiplePrioritizations = 29305  <br/> |Не удается создать несколько определений приоритетов целей.  <br/> |
|OptimizerCannotUpdateMultiplePrioritizations = 29306  <br/> |Не удается обновить несколько определений приоритетов целей.  <br/> |
|OptimizerDriverRelationsNotFilled = 29307  <br/> |Данные DriverRelationsRow являются неполными.  <br/> |
|OptimizerDriversNotFilled = 29308  <br/> |В целях проекта недостаточно информации для выработки решения.  <br/> |
|OptimizerDriverRelationsInvalidInversedValue = 29309  <br/> |В [DriverPrioritizationDataSet.DriverRelationsRow](https://msdn.microsoft.com/library/WebSvcDriver.DriverPrioritizationDataSet.DriverRelationsRow.aspx) имеются обратные значения.  <br/> |
|OptimizerCannotCreatePrioritizationUsingInactiveDrivers = 29310  <br/> |В [DriverPrioritizationDataSet.DriverRelationsRow](https://msdn.microsoft.com/library/WebSvcDriver.DriverPrioritizationDataSet.DriverRelationsRow.aspx) указан неактивный драйвер. Проверьте свойства **DRIVER1_UID** и **DRIVER2_UID**.  <br/> |
|OptimizerCannotChangePrioritizationType = 29311  <br/> |Не удается изменить тип определения приоритетов.  <br/> |
|OptimizerCannotSpecifyPriorityValuesForCalculatedPrioritizations = 29312  <br/> |В случае расчета приоритета для него нельзя указать значение.  <br/> |
|OptimizerCannotNormalizePriorityValues = 29313  <br/> |Значения приоритета нельзя нормализовать.  <br/> |
|OptimizerTooManyDriversInPrioritization = 29314  <br/> |Слишком много бизнес-целей в определении приоритетов.  <br/> |
|OptimizerInvalidProjectImpactValue = 29400  <br/> |Недопустимое значение влияния проекта.  <br/> |
|OptimizerCannotDeleteDriver = 29401  <br/> |Эту цель проекта нельзя удалить.  <br/> |
|OptimizerCannotCreateDriver = 29402  <br/> |Эту цель проекта нельзя создать.  <br/> |
|OptimizerCannotUpdateDriver = 29403  <br/> |Эту цель проекта нельзя обновить.  <br/> |
|OptimizerCannotEditDriver = 29404  <br/> |Эту цель проекта нельзя изменить.  <br/> |
|OptimizerCannotCreateMultipleDrivers = 29405  <br/> |Не удается создать несколько целей.  <br/> |
|OptimizerCannotUpdateMultipleDrivers = 29406  <br/> |Не удается обновить несколько целей.  <br/> |
|OptimizerInvalidRelativeImportanceValue = 29407  <br/> |Недопустимое значение относительной важности.  <br/> |
|OptimizerInvalidDriverUid = 29500  <br/> |Недопустимый GUID цели.  <br/> |
|OptimizerInvalidEntityType = 29501  <br/> |Недопустимый тип сущности для оптимизатора.  <br/> |
|OptimizerInvalidProjectUid = 29502  <br/> |Недопустимый GUID проекта.  <br/> |
|OptimizerInvalidCustomFieldUid = 29503  <br/> |Недопустимый GUID настраиваемого поля для оптимизатора.  <br/> |
|OptimizerInvalidHardConstraintUid = 29504  <br/> |Недопустимый GUID строгого ограничения.  <br/> |
|OptimizerInvalidAnalysisUid = 29505  <br/> |Недопустимый GUID анализа.  <br/> |
|OptimizerDriverFilterInvalid = 29506  <br/> |Недопустимый фильтр целей.  <br/> |
|OptimizerPrioritizationFilterInvalid = 29507  <br/> |Недопустимый фильтр определения приоритетов.  <br/> |
|OptimizerCannotLoadOptimizationEngine = 29508  <br/> |Не удается загрузить модуль расчета оптимизатора.  <br/> |
|OptimizerAnalysisFilterInvalid = 29509  <br/> |Недопустимый фильтр анализа.  <br/> |
|OptimizerSolutionFilterInvalid = 29510  <br/> |Недопустимый фильтр решений для оптимизатора.  <br/> |
|OptimizerDependenciesFilterInvalid = 29511  <br/> |Недопустимый фильтр зависимостей для оптимизатора.  <br/> |
|OptimizerInvalidSolutionUid = 29512  <br/> |Недопустимый GUID решения для оптимизатора.  <br/> |
|OptimizerInvalidViewUid = 29513  <br/> |Недопустимый GUID представления для оптимизатора.  <br/> |
|OptimizerInvalidAnalysisType = 29600  <br/> |Недопустимый тип анализа портфеля.  <br/> |
|OptimizerInvalidPrioritizationType = 29601  <br/> |Недопустимый тип определения приоритетов для оптимизатора.  <br/> |
|OptimizerCannotDeleteAnalysis = 29602  <br/> |Не удается удалить анализ портфеля.  <br/> |
|OptimizerCannotCreateAnalysis = 29603  <br/> |Не удается создать анализ портфеля.  <br/> |
|OptimizerCannotUpdateAnalysis = 29604  <br/> |Не удается обновить анализ портфеля.  <br/> |
|OptimizerInvalidPrioritizationUid = 29607  <br/> |Недопустимый GUID определения приоритетов.  <br/> |
|OptimizerCannotCreateMultipleAnalyses = 29608  <br/> |Не удается создать несколько анализов портфеля.  <br/> |
|OptimizerCannotUpdateMultipleAnalyses = 29609  <br/> |Не удается обновить несколько анализов портфеля.  <br/> |
|OptimizerCannotCalculateProjectPriorities = 29610  <br/> |Оптимизатор не может вычислить приоритеты проектов.  <br/> |
|OptimizerCannotDeleteAnalysisProjectImpact = 29611  <br/> |Не удается удалить влияние проекта в анализе портфеля.  <br/> |
|OptimizerCannotChangeAnalysisProjects = 29612  <br/> |Не удается изменить проекты в анализе портфеля.  <br/> |
|OptimizerCannotChangePriorityData = 29613  <br/> |Не удается изменить данные о приоритетах.  <br/> |
|OptimizerCannotEditAnalysis = 29614  <br/> |Не удается изменить анализ портфеля.  <br/> |
|OptimizerInvalidPlannerData = 29615  <br/> |Недопустимые данные планировщика для оптимизатора.  <br/> |
|OptimizerCannotChangeImpactData = 29616  <br/> |Не удается изменить данные о влиянии проекта.  <br/> |
|OptimizerInvalidProjectsNumber = 29617  <br/> |Недопустимое число проектов.  <br/> |
|OptimizerCannotAddImpactCFUIDToCFAnalysis = 29618  <br/> |Не удается добавить GUID настраиваемого поля влияния проекта ([PROJECT_IMPACT_CF_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.AnalysisDataSet.AnalysisRow.PROJECT_IMPACT_CF_UID.aspx) ) для анализа портфеля.  <br/> |
|OptimizerInvalidDepartmentUid = 29619  <br/> |Значение [DEPARTMENT_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.AnalysisDataSet.AnalysisRow.DEPARTMENT_UID.aspx) является недопустимым.  <br/> |
|OptimizerTooManyProjectsInAnalysis = 29620  <br/> |Слишком много проектов в анализе.  <br/> |
|QueueAnalysisCannotDeleteAnalysis = 29680  <br/> |Метод [QueueDeleteAnalyses](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueDeleteAnalyses.aspx) не может удалить анализ.  <br/> |
|QueueAnalysisCannotCreateAnalysis = 29681  <br/> |Метод [QueueCreateAnalysis](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueCreateAnalysis.aspx) не может создать анализ.  <br/> |
|QueueAnalysisCannotUpdateAnalysis = 29682  <br/> |Метод [QueueUpdateAnalysis](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueUpdateAnalysis.aspx) не может обновить анализ.  <br/> |
|AnalysisMismatchedJobList = 29690  <br/> |Несоответствие списка заданий анализа.  <br/> |
|OptimizerInvalidForceInLookupTableUid = 29691  <br/> |GUID таблицы подстановки нельзя включить принудительно.  <br/> |
|OptimizerInvalidForceOutLookupTableUid = 29692  <br/> |GUID таблицы подстановки нельзя исключить принудительно.  <br/> |
|OptimizerDuplicateForceLookupTableUids = 29693  <br/> |Повторяющиеся принудительные GUID таблицы подстановки.  <br/> |
|OptimizerInvalidDecisionResult = 29701  <br/> |Недопустимый результат по решению.  <br/> |
|OptimizerInvalidForcedStatus = 29702  <br/> |Недопустимое принудительное состояние.  <br/> |
|OptimizerCannotDeleteSolution = 29703  <br/> |Метод [QueueDeleteOptimizerSolutions](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueDeleteOptimizerSolutions.aspx) не может удалить решение оптимизатора.  <br/> |
|OptimizerCannotCreateSolution = 29704  <br/> |Метод [QueueCreateOptimizerSolution](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueCreateOptimizerSolution.aspx) не может создать решение оптимизатора.  <br/> |
|OptimizerCannotUpdateSolution = 29705  <br/> |Метод [QueueUpdateAnalysis](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.QueueUpdateAnalysis.aspx) не может обновить решение оптимизатора.  <br/> |
|OptimizerCannotCalculateSolutionStrategicAlignment = 29706  <br/> |Оптимизатор не может вычислить решение для стратегического выравнивания.  <br/> |
|OptimizerCannotCreateMultipleSolutions = 29707  <br/> |Оптимизатор не может создать несколько решений.  <br/> |
|OptimizerCannotUpdateMultipleSolutions = 29708  <br/> |Оптимизатор не может обновить несколько решений.  <br/> |
|OptimizerCannotAddPrioritizationToCFAnalysis = 29709  <br/> |Оптимизатор не может добавить определение приоритетов в настраиваемое поле для анализа.  <br/> |
|OptimizerTableIsReadOnly = 29710  <br/> |Эта таблица оптимизатора доступна только для чтения.  <br/> |
|OptimizerSolutionCreateMessageFailed = 29711  <br/> |Оптимизатору не удалось сформировать сообщение о создании решения.  <br/> |
|OptimizerSolutionDeleteMessageFailed = 29712  <br/> |Оптимизатору не удалось сформировать сообщение об удалении решения.  <br/> |
|OptimizerCannotCalculateEfficientFrontier = 29714  <br/> |Оптимизатор не может вычислить эффективную границу для анализа.  <br/> |
|OptimizerCannotUpdateSolutionProperties = 29715  <br/> |Не удается обновить свойства решения.  <br/> |
|OptimizerInvalidConstraintPosition = 29716  <br/> |Недопустимое положение ограничения в оптимизаторе.  <br/> |
|OptimizerInvalidHardConstraintPosition = 29717  <br/> |Недопустимое положение строгого ограничения в оптимизаторе.  <br/> |
|OptimizerInvalidConstraintLimit = 29718  <br/> |Недопустимый предел ограничения в оптимизаторе.  <br/> |
|OptimizerInvalidConstraintValue = 29719  <br/> |Недопустимое значение ограничения.  <br/> |
|OptimizerInvalidSolutionProjectsSet = 29720  <br/> |Недопустимый набор проектов в решении.  <br/> |
|OptimizerCannotCommitSolution = 29721  <br/> |Метод [CommitOptimizerSolution](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PortfolioAnalyses.CommitOptimizerSolution.aspx) не может зафиксировать решение.  <br/> |
|OptimizerInvalidInputData = 29723  <br/> |Недопустимые входные данные для оптимизатора.  <br/> |
|OptimizerInvalidConstraintSet = 29724  <br/> |Недопустимый набор ограничений для оптимизатора.  <br/> |
|OptimizerCannotUpdateAnalysisMetrics = 29725  <br/> |Не удается обновить метрики анализа.  <br/> |
|OptimizerSolutionMismatchedJobList = 29726  <br/> |Несоответствие списка заданий в решении.  <br/> |
|OptimizerInvalidForceLookupTableValue = 29727  <br/> |Недопустимое принудительное значение таблицы подстановки.  <br/> |
|OptimizerCannotCreateSolutionWhileAnalysisUpdateIsPending = 29728  <br/> |Не удается создать решение оптимизатора при наличии ожидающего обновления анализа.  <br/> |
|OptimizerProjectSelectorAtLeastOne = 29800  <br/> |Для оптимизатора следует выбрать хотя бы один проект.  <br/> |
   
Коды ошибок в таблице 17 предназначены для планировщика, который является компонентом, используемым в анализе портфеля проектов.

<a name="pj15_ErrorCodes_Planner"></a>

## <a name="table-17-planner-project-portfolio-analysis"></a>Табл. 17. Планировщик (анализ портфеля проектов)

|Код ошибки планировщика|Описание|
|:-----|:-----|
|PlannerSolutionMessageDeleteFailed = 28000  <br/> |Ошибка очереди: сбой сообщения для удаления решения планировщика.  <br/> |
|PlannerSolutionMessageCreateFailed = 28001  <br/> |Ошибка очереди: сбой сообщения для создания решения планировщика.  <br/> |
|PlannerInvalidRBSValueUid = 28002  <br/> |Недопустимый GUID для значения структурной декомпозиции ресурсов в данных планировщика.  <br/> |
|PlannerInvalidCustomFieldUid = 28003  <br/> |Недопустимый GUID для настраиваемого поля.  <br/> |
|PlannerHorizonInvalid = 28004  <br/> |Недопустимый временной горизонт планировщика. Временной горизонт — это период, указанный для планирования емкости.  <br/> |
|PlannerHorizonTooBig = 28005  <br/> |Временной горизонт относится к слишком далекому будущему.  <br/> |
|PlannerInvalidBookingType = 28006  <br/> |Недопустимый тип резервирования ресурсов.  <br/> |
|PlannerInvalidTimeScale = 28007  <br/> |Недопустимая шкала времени.  <br/> |
|PlannerInvalidProjectSNET = 28008  <br/> |Недопустимая дата "Начало не ранее" для проекта.  <br/> |
|PlannerInvalidProjectFNLT = 28009  <br/> |Недопустимая дата "Окончание не позднее" для проекта.  <br/> |
|PlannerInvalidAnalysisStartDate = 28010  <br/> |Дата [START_DATE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionProjectRequirementsByRoleRow.START_DATE.aspx) для проекта является недопустимой.  <br/> |
|PlannerInvalidAnalysisDuration = 28011  <br/> |Длительность [DURATION](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionProjectsRow.DURATION.aspx) для анализа портфеля является недопустимой.  <br/> |
|PlannerInvalidHorizonStartDate = 28012  <br/> |Недопустимая дата начала для временного горизонта.  <br/> |
|PlannerInvalidHorizonEndDate = 28013  <br/> |Недопустимая дата окончания для временного горизонта.  <br/> |
|PlannerInvalidHorizonTimeScale = 28014  <br/> |Недопустимая шкала времени для временного горизонта.  <br/> |
|PlannerInvalidAnalysisType = 28015  <br/> |Недопустимый тип анализа портфеля.  <br/> |
|PlannerHorizonStartDateDoesNotMatchTimeScale = 28016  <br/> |Дата начала для временного горизонта не соответствует шкале времени.  <br/> |
|PlannerHorizonEndDateDoesNotMatchTimeScale = 28017  <br/> |Дата окончания для временного горизонта не соответствует шкале времени.  <br/> |
|PlannerAnalysisNoCapacityData = 28037  <br/> |Отсутствуют данные о емкости ресурсов для анализа портфеля.  <br/> |
|PlannerInvalidSolutionUid = 28100  <br/> |Недопустимый GUID решения анализа.  <br/> |
|PlannerInvalidOptimizerSolutionUid = 28101  <br/> |Недопустимый GUID решения оптимизатора.  <br/> |
|PlannerInvalidLookupTableValueUid = 28102  <br/> |Недопустимый GUID значения таблицы подстановки.  <br/> |
|PlannerInvalidEfficientFrontierUid = 28103  <br/> |Значение [FRONTIER_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionEfficientFrontierRow.FRONTIER_UID.aspx) является недопустимым.  <br/> |
|PlannerInvalidProjectUid = 28104  <br/> |Недопустимый GUID проекта.  <br/> |
|PlannerInvalidAllocationThreshold = 28105  <br/> |Недопустимый порог выделения.  <br/> |
|PlannerInvalidHiringType = 28109  <br/> |Значение [HIRING_TYPE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.HIRING_TYPE.aspx) является недопустимым. См. статью [Planner.PlannerHiringType](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Planner.PlannerHiringType.aspx).  <br/> |
|PlannerInvalidConstraintType = 28110  <br/> |Значение [CONSTRAINT_TYPE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.CONSTRAINT_TYPE.aspx) является недопустимым. См. статью [Planner.ConstraintType](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Planner.ConstraintType.aspx).  <br/> |
|PlannerInvalidConstraintValue = 28111  <br/> |Значение [CONSTRAINT_VALUE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.CONSTRAINT_VALUE.aspx) является недопустимым.  <br/> |
|PlannerInvalidRateTable = 28112  <br/> |Значение [RATE_TABLE](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.RATE_TABLE.aspx) является недопустимым.  <br/> |
|PlannerInvalidSolutionForConstraint = 28113  <br/> |Недопустимое решение планировщика для ограничения. Слишком много принудительных включений проектов во время первого прохода планировщика.  <br/> |
|PlannerInvalidSolutionForDependencies = 28114  <br/> |Решение планировщика не является допустимым из-за слишком большого числа проектов для анализа бизнес-зависимостей или конфликтов. Эта ошибка возникает при втором проходе.  <br/> |
|PlannerInvalidSolutionForScheduling = 28115  <br/> |Решение планировщика не является допустимым для планирования из-за наличия циклических зависимостей.  <br/> |
|PlannerInvalidAnalysisUid = 28116  <br/> |Значение [ANALYSIS_UID](https://msdn.microsoft.com/library/WebSvcPortfolioAnalyses.PlannerSolutionDataSet.SolutionsRow.ANALYSIS_UID.aspx) является недопустимым.  <br/> |
|PlannerInvalidProjectStartDate = 28200  <br/> |Недопустимая дата начала проекта.  <br/> |
|PlannerInvalidProjectEndDate = 28201  <br/> |Недопустимая дата окончания проекта.  <br/> |
|PlannerInvalidProjectDuration = 28202  <br/> |Недопустимая длительность проекта.  <br/> |
|PlannerInvalidProjectFNLTDate = 28203  <br/> |Недопустимая дата "Окончание не позднее" для проекта.  <br/> |
|PlannerInvalidProjectSNETDate = 28204  <br/> |Недопустимая дата "Начало не ранее" для проекта.  <br/> |
|PlannerCannotCreateSolution = 28900  <br/> |Планировщик не может создать решение.  <br/> |
|PlannerCannotUpdateSolution = 28901  <br/> |Планировщик не может обновить решение.  <br/> |
|PlannerCannotDeleteSolution = 28902  <br/> |Планировщик не может удалить решение.  <br/> |
|PlannerCannotCreateMultipleSolutions = 28903  <br/> |Планировщик не может создать несколько решений.  <br/> |
|PlannerCannotUpdateMultipleSolutions = 28904  <br/> |Планировщик не может обновить несколько решений.  <br/> |
|PlannerTableIsReadOnly = 28907  <br/> |Таблица **DataTable** доступна только для чтения.  <br/> |
|PlannerCannotCommitSolution = 28908  <br/> |Планировщик не может зафиксировать решение в базе данных.  <br/> |
|PlannerFieldIsReadOnly = 28909  <br/> |Это поле доступно только для чтения.  <br/> |
|PlannerProjectNotInParentSolution = 28910  <br/> |Проект находится не в родительском решении.  <br/> |
|PlannerProjectNotSelectedInParentSolution = 28911  <br/> |Проект не выбран в родительском решении.  <br/> |
|PlannerProjectNotInParentAnalysis = 28912  <br/> |Проект находится не в родительском анализе портфеля.  <br/> |
|PlannerProjectBeyondHorizon = 28913  <br/> |Проект выходит за пределы временного горизонта.  <br/> |
|PlannerResourceAllocationInternalError = 28915  <br/> |Внутренняя ошибка в выделении ресурсов.  <br/> |
|PlannerResourceAllocationInfeasibleSolution = 28916  <br/> |Выделение ресурсов является недопустимым решением.  <br/> |
|PlannerProjectEndDateViolatesDependency = 28917  <br/> |Дата окончания проекта нарушает зависимость.  <br/> |
|PlannerInvalidProjectsSet = 28919  <br/> |Недопустимый набор проектов.  <br/> |
|PlannerInvalidInputData = 28920  <br/> |Недопустимые входные данные планировщика.  <br/> |
|PlannerDecimalOverflowError = 28921  <br/> |Ошибка переполнения десятичных разрядов в планировщике.  <br/> |
|PlannerSolutionMismatchedJobList = 28922  <br/> |Это решение содержит несоответствующий список заданий.  <br/> |
|PlannerInvalidForceLookupTableValue = 28923  <br/> |Недопустимое принудительное значение в таблице подстановки.  <br/> |
|PlannerNoHiredResource = 28924  <br/> |Отсутствует ресурс, нанятый для предложения.  <br/> |

<a name="pj15_ErrorCodes_Projects"></a>

## <a name="table-18-project"></a>Табл. 18. Проект

|Код ошибки проекта|Описание|
|:-----|:-----|
|ProjectGlobalNotFound = 100  <br/> |Не удается найти глобальный корпоративный шаблон.  <br/> |
|ProjectGlobalCannotBeDeleted = 101  <br/> |Не удается удалить глобальный корпоративный шаблон.  <br/> |
|ProjectNotFound = 1000  <br/> |Проект не найден.  <br/> |
|ProjectAlreadyExists = 1001  <br/> |Проект уже существует.  <br/> |
|ProjectCheckedoutToOtherUser = 1002  <br/> |Проект извлечен другому пользователю.  <br/> |
|ProjectTypeInvalidForCreate = 1003  <br/> |Недопустимый тип проекта для операции создания.  <br/> |
|ProjectParametersInvalid = 1004  <br/> |Один или несколько параметров проекта не являются допустимыми.  <br/> |
|ProjectNotCheckedoutToUser = 1006  <br/> |Проект не извлечен пользователю.  <br/> |
|ProjectCheckedout = 1007  <br/> |Проект извлечен.  <br/> |
|ProjectTypeInvalid = 1008  <br/> |Недопустимый тип проекта.  <br/> |
|ProjectIDInvalid = 1009  <br/> |Недопустимый идентификационный номер проекта.  <br/> |
|ProjectNameTooLong = 1014  <br/> |Слишком длинное имя проекта.  <br/> |
|ProjectManagerNameTooLong = 1015  <br/> |Слишком длинное имя диспетчера проектов.  <br/> |
|ProjectNameInvalid = 1016  <br/> |Недопустимое имя проекта.  <br/> |
|ProjectStartDateMissing = 1025  <br/> |Отсутствует дата начала проекта.  <br/> |
|ProjectNameMissing = 1026  <br/> |Отсутствует имя проекта.  <br/> |
|ProjectVersionMissing = 1027  <br/> |Отсутствует версия проекта.  <br/> |
|ProjectDoesNotExist = 1028  <br/> |Проект не существует.  <br/> |
|ProjectMultipleProjectsInvalid = 1029  <br/> |Несколько недопустимых проектов.  <br/> |
|ProjectHasWriteLock = 1030  <br/> |Проект имеет блокировку записи в базе данных.  <br/> |
|ProjectHasPendingWriteLock = 1031  <br/> |Проект имеет ожидающую блокировку записи.  <br/> |
|ProjectHasNoReadLock = 1032  <br/> |У проекта нет блокировки чтения.  <br/> |
|ProjectHasReadLock = 1033  <br/> |Проект имеет блокировку чтения.  <br/> |
|ProjectNameAlreadyExists = 1034  <br/> |Имя проекта уже существует.  <br/> |
|ProjectOptCriticalSlackLimitInvalid = 1035  <br/> |Критический предел необязательного резерва времени не является допустимым.  <br/> |
|ProjectOptCurrencyPositionInvalid = 1036  <br/> |Положение необязательной денежной единицы не является допустимым.  <br/> |
|ProjectOptCurrencyDigitsInvalid = 1037  <br/> |Число цифр необязательной денежной единицы не является допустимым.  <br/> |
|ProjectOptCurrencySymbolTooLong = 1038  <br/> |Слишком длинное обозначение необязательной денежной единицы.  <br/> |
|ProjectCannotDelete = 1039  <br/> |Не удается удалить проект. Удалить можно только обычные проекты и шаблоны проектов, находящиеся на стороне сервера.  <br/> |
|ProjectCannotAdd = 1040  <br/> |Невозможно использовать метод **AddToProject** в проекте на стороне сервера.  <br/> |
|ProjectOptCurrencySymbolInvalid = 1041  <br/> |Обозначение необязательной денежной единицы не является допустимым.  <br/> |
|ProjectHasNoWriteLock = 1042  <br/> |У проекта нет блокировки записи.  <br/> |
|ProjectFilterInvalid = 1043  <br/> |Недопустимый фильтр проектов.  <br/> |
|ProjectTooLarge = 1044  <br/> |Слишком большая проектная инициатива.  <br/> |
|ProjectOptCurrencyCodeNot3Chars = 1045  <br/> |Код необязательной валюты отличается от трехзначного.  <br/> |
|ProjectOptCurrencyCodeInvalid = 1046  <br/> |Недопустимый код валюты в параметрах проекта.  <br/> |
|ProjectActualsAreProtected = 1047  <br/> |Фактические данные проекта защищены.  <br/> |
|ProjectTemplateNotFound = 1048  <br/> |Шаблон проекта не найден.  <br/> |
|ProjectCurrencyCodeInvalid = 1049  <br/> |Недопустимый код валюты.  <br/> |
|ProjectCannotEditCostResource = 1050  <br/> |Не удается изменить затратный ресурс.  <br/> |
|ProjectIsNotPublished = 1051  <br/> |Проект не опубликован.  <br/> |
|ProjectExceededLWPTaskLimit = 1052  <br/> |Превышено ограничение задачи для предложения проекта (простой проект).  <br/> |
|ProjectOptFinishDateInvalid = 1053  <br/> |Недопустимая дата окончания в параметрах проекта.  <br/> |
|ProjectExceededItemsLimit = 1054  <br/> |Превышен предел по обрабатываемым элементам. Приложение службы Project Server не может использовать **ProjectDataSet** для добавления или обновления более 1000 элементов совокупно во всех таблицах. Чтобы обработать более 1000 элементов, используйте несколько вызовов, например, в **QueueUpdateProject**.<br/> |
|ProjectColumnNotReadOnly = 1055  <br/> |Этот столбец доступен не только для чтения.  <br/> |
|ProjectInvalidOwner = 1056  <br/> |Недопустимый владелец проекта.  <br/> |
|ProjectCantEditPctWrkCompForNonWrkRscs = 1057  <br/> |Не удается изменить **PctWorkComplete** для задачи, которая не имеет реальных назначенных трудозатрат.  <br/> |
|ProjectCannotEditMaterialResource = 1058  <br/> |Не удается изменить материальный ресурс.  <br/> |
|ProjectCannotEditFieldWhenTaskHasNoWorkAssignment = 1059  <br/> |Не удается изменить поле, так как задача не имеет назначенных трудозатрат.  <br/> |
|ProjectSubProjectNotFound = 1070  <br/> |. Подпроекты не найдены.  <br/> |
|ProjectResourceNotFound = 1100  <br/> |Ресурс не найден.  <br/> |
|ProjectResourceAlreadyExists = 1101  <br/> |Ресурс уже существует.  <br/> |
|ProjectCannotReplaceResourceWithSelf = 1106  <br/> |Не удается заменить ресурс на тот же самый объект.  <br/> |
|ProjectCannotChangeLockedTrackingMethod = 1107  <br/> |Не удается выполнить изменение из-за заблокированного метода отслеживания.  <br/> |
|ProjectInvalidColumnForCompatibilityMode = 1108  <br/> |Недопустимый столбец для режима совместимости.  <br/> |
|ProjectUpdateInvalidUpdateSequenceNumber = 1151  <br/> |Недопустимый порядковый номер в обновлении проекта.  <br/> |
|ProjectUpdateDuplicateUpdateSequenceNumber = 1152  <br/> |Повторяющийся порядковый номер в обновлении проекта.  <br/> |
|ProjectUpdateNullUpdateSequenceNumber = 1153  <br/> |Порядковый номер со значением NULL в обновлении проекта.  <br/> |
|ProjectUpdateNullUpdateColumnNames = 1154  <br/> |Имена столбцов со значением NULL в обновлении проекта.  <br/> |
|ProjectUpdateInvalidProjectUID = 1155  <br/> |Недопустимый GUID проекта в этом обновлении проекта.  <br/> |
|ProjectUpdateInvalidColumnForUpdate = 1156  <br/> |Недопустимый столбец для этого обновления проекта.  <br/> |
|ProjectUpdateCannotEditColumn = 1157  <br/> |Не удается изменить столбец в обновлении проекта.  <br/> |
|ProjectUpdateNoChangesToValidateAndSchedule = 1158  <br/> |Обновление проекта не содержит изменений, который можно проверить и запланировать.  <br/> |
|LinkNotFound = 1159  <br/> |Ссылка не найдена.  <br/> |
|ProjectUpdateInvalidColumnValue = 1160  <br/> |Недопустимое значение столбца для этого обновления проекта.  <br/> |
|ProjectCannotDeleteItem = 1161  <br/> |Не удается удалить элемент проекта.  <br/> |
|ProjectUpdateCannotComputeOptIndex = 1162  <br/> |Не удается вычислить индекс оптимизации в обновлении проекта.  <br/> |
|ProjectCannotUpdateDueToVisibilityMode = 1163  <br/> |Не удается выполнить обновление, так как проект находится в режиме видимости.  <br/> |
|ProjectNodeConsistencyException = 9132  <br/> |Исключение: узел не согласован.  <br/> |
|ProjectSchedulingEngineException = 9133  <br/> |Исключение в модуле планирования.  <br/> |
|ProjectFormulaCalculationException = 9134  <br/> |Исключение при расчете формулы.  <br/> |
|ProjectUpdateDatabaseException = 9135  <br/> |Исключение при обновлении базы данных.  <br/> |
|ProjectDeleteException = 9136  <br/> |Исключение при удалении проекта.  <br/> |
|ProjectOperationException = 9137  <br/> |Исключение в операции проекта.  <br/> |
|ProjectCannotComunicateWithPCS = 9138  <br/> |Не удалось связаться с работником PCS.  <br/> |
|ProjectPCSSessionInvalid = 9139  <br/> |Не удалось открыть проект в сеансе модуля.  <br/> |
|ProjectPublishFailure = 23000  <br/> |Сбой в очереди при публикации проекта.  <br/> |
|ProjectCurrencyConflict = 23001  <br/> |Конфликт, связанный с указанной валютой.  <br/> |
|ProjectPublishFailed = 23002  <br/> |Произошел сбой публикации проекта на этапе помещения в очередь.  <br/> |
|ProjectReversePublishFailed = 23003  <br/> |Произошел сбой операции публикации проекта на этапе помещения в очередь.  <br/> |
|ProjectReversePublishFailure = 23004  <br/> |Сбой обратной публикации проекта во время обработки очереди.  <br/> |
|ProjectArchiveRetentionDeleteFailure = 23005  <br/> |Сбой удаления проекта из-за хранения архива.  <br/> |
|ProjectDeleteFailure = 23006  <br/> |Сбой удаления проекта.  <br/> |
|ProjectPublishEnqueueFailure = 23007  <br/> |Сбой публикации проекта во время помещения в очередь.  <br/> |
|ProjectCheckinFailure = 23008  <br/> |Сбой возвращения проекта во время обработки очереди.  <br/> |
|ProjectCheckinFailed = 23009  <br/> |Произошел сбой возвращения проекта на этапе помещения в очередь.  <br/> |
|ProjectCheckoutFailed = 23010  <br/> |У пользователя нет разрешения на извлечение проекта.  <br/> |
|ProjectPublishSummaryEnqueueFailure = 23011  <br/> |Сбой публикации сводки во время помещения в очередь.  <br/> |
|ProjectPublishSummaryFailed = 23012  <br/> |Сбой публикации сводки.  <br/> |
|ProjectUpdateScheduledProjectFailure = 26026  <br/> |Сбой обновления планирования проекта во время обработки очереди.  <br/> |
|ProjectSyncProjectEnterpriseEntitiesFailure = 26033  <br/> |Сбой синхронизации корпоративных сущностей проекта во время обработки очереди.  <br/> |
|GeneralDalDatabaseIsReadOnly = 26034  <br/> |Сбой загрузки детализации проекта. База данных доступна только для чтения.  <br/> |
|GeneralDatabaseCommunicationError = 26035  <br/> |Могут быть разные причины, например неполадки сети или проблемы проверки подлинности.  <br/> |

<a name="pj15_ErrorCodes_RDS"></a>

## <a name="table-19-reporting-data-service-rds"></a>Табл. 19. Служба отчетных данных (RDS)

|Код ошибки RDS|Описание|
|:-----|:-----|
|ReportingAttributeCubeSettingsChangedMessageFailed = 24000  <br/> |Сбой сообщения об изменении RDS для атрибута параметров куба.  <br/> |
|ReportingBaseCalendarChangeMessageFailed = 24001  <br/> |Сбой сообщения об изменении RDS для базового календаря.  <br/> |
|ReportingCustomFieldMetadataChangeMessageFailed = 24002  <br/> |Сбой сообщения об изменении RDS для метаданных настраиваемого поля.  <br/> |
|ReportingEntityUserViewChangedMessageFailed = 24003  <br/> |Сбой сообщения об изменении RDS для пользовательского представления сущности.  <br/> |
|ReportingFiscalPeriodChangeMessageFailed = 24004  <br/> |Сбой сообщения об изменении RDS для финансового периода.  <br/> |
|ReportingLookupTableChangeMessageFailed = 24005  <br/> |Сбой сообщения об изменении RDS для таблицы подстановки.  <br/> |
|ReportingProjectChangeMessageFailed = 24006  <br/> |Сбой сообщения об изменении RDS для проекта.  <br/> |
|ReportingResourceCapacityUpdateMessageFailed = 24007  <br/> |Сбой сообщения об обновлении RDS для емкости ресурсов.  <br/> |
|ReportingResourceChangeMessageFailed = 24008  <br/> |Сбой сообщения об изменении RDS для ресурса.  <br/> |
|ReportingTimesheetAdjustMessageFailed = 24009  <br/> |Сбой сообщения о корректировке RDS для расписания.  <br/> |
|ReportingTimesheetClassCreateMessageFailed = 24010  <br/> |Сбой сообщения о создании RDS для класса.  <br/> |
|ReportingTimesheetDeleteMessageFailed = 24011  <br/> |Сбой сообщения об удалении RDS для расписания.  <br/> |
|ReportingTimesheetPeriodDeleteMessageFailed = 24012  <br/> |Сбой сообщения об удалении RDS для периода расписания.  <br/> |
|ReportingTimesheetPeriodMessageFailed = 24013  <br/> |Сбой сообщения RDS для периода расписания.  <br/> |
|ReportingTimesheetSaveMessageFailed = 24014  <br/> |Сбой сообщения о сохранении RDS для расписания.  <br/> |
|ReportingTimesheetStatusChangeMessageFailed = 24015  <br/> |Сбой сообщения об изменении RDS для состояния расписания.  <br/> |
|ReportingWSSSyncMessageFailed = 24016  <br/> |Сбой сообщения RDS для синхронизации с SharePoint.  <br/> |
|ReportingGetSPWebFailed = 24017  <br/> |Службе RDS не удалось получить значение веб-сайта SharePoint.  <br/> |
|ReportingWssSyncListFailed = 24018  <br/> |Службе RDS не удалось синхронизироваться со списком SharePoint.  <br/> |
|ReportingWssTransferLinksFailed = 24019  <br/> |Службе RDS не удалось передать ссылки SharePoint.  <br/> |
|ReportingQueueMessageSubmitFailed = 24020  <br/> |Службе RDS не удалось отправить сообщение в очередь.  <br/> |
|ReportingWssSyncHRefFailed = 24021  <br/> |Службе RDS не удалось синхронизироваться со значением HRef SharePoint.  <br/> |
|ReportingSyncGlobalDataMessageFailed = 24022  <br/> |Сбой сообщения RDS, предназначенного для синхронизации с глобальными корпоративными данными.  <br/> |
|ReportingRDBRefreshMessageFailed = 24023  <br/> |Сбой сообщения RDS, предназначенного для обновления службы RDB.  <br/> |
|ReportingAttributeCubeDepartmentsChangedMessageFailed = 24024  <br/> |Сообщению RDS не удалось изменить атрибут отдела для куба OLAP.  <br/> |
|ReportingTimesheetProjectAggregationMessageFailed = 24025  <br/> |Сообщению RDS не удалось объединить проекты для таблиц расписания в службе RDB.  <br/> |
|ReportingRdbBulkDataSyncMessageFailed = 24026  <br/> |Сбой сообщения RDS для синхронизации массовых данных в службе RDB.  <br/> |
|ReportingWorkflowMetadataSyncMessageFailed = 24027  <br/> |Сообщению RDS не удалось синхронизировать метаданные рабочего процесса.  <br/> |
|ReportingProjectWorkflowInformationSyncMessageFailed = 24028  <br/> |Сообщению RDS не удалось синхронизировать информацию о рабочем процессе проекта.  <br/> |
|ReportingEptSyncMessageFailed = 24029  <br/> |Сообщению RDS не удалось синхронизировать шаблон корпоративного проекта.  <br/> |
|ReportingSummaryProjectPublishMessageFailed = 24030  <br/> |Сообщению RDS не удалось опубликовать сводный проект.  <br/> |
|ReportingSolutionCommitedDecisionChangedMessageFailed = 24031  <br/> |Сообщению RDS не удалось изменить зафиксированное решение по приложению.  <br/> |
|ReportingDelayedUpgradeFailed = 24032  <br/> |Сбой отложенного обновления RDB.  <br/> |

<a name="pj15_ErrorCodes_Resources"></a>

## <a name="table-20-resource"></a>Табл. 20. Ресурс

|Код ошибки ресурса|Описание|
|:-----|:-----|
|ResourceNotFound = 2000  <br/> |Ресурс не найден.  <br/> |
|ResourceAlreadyExists = 2001  <br/> |Ресурс уже существует.  <br/> |
|ResourceCheckedoutToOtherUser = 2002  <br/> |Ресурс извлечен другому пользователю.  <br/> |
|ResourceUIDInvalid = 2011  <br/> |Недопустимый GUID ресурса.  <br/> |
|ResourceNameInvalid = 2016  <br/> |Недопустимое имя ресурса.  <br/> |
|ResourceNameTooLong = 2017  <br/> |Слишком длинное имя ресурса.  <br/> |
|ResourceInitialsTooLong = 2018  <br/> |Слишком длинное краткое название ресурса.  <br/> |
|ResourceCheckedout = 2025  <br/> |Ресурс извлечен.  <br/> |
|ResourceNTAccountInvalid = 2026  <br/> |Недопустимая учетная запись Windows (NTLM) ресурса.  <br/> |
|ResourceNameAlreadyInUse = 2027  <br/> |Имя ресурса уже используется. Имена должны быть уникальными.  <br/> |
|ResourceNTAccountAlreadyInUse = 2028  <br/> |Эта учетная запись NTLM ресурса уже используется.  <br/> |
|ResourceAdGuidAlreadyInUse = 2029  <br/> |Этот GUID ресурса уже используется.  <br/> |
|ResourceHasActuals = 2031  <br/> |Ресурс имеет фактические данные.  <br/> |
|ResourceNTAccountTooLong = 2035  <br/> |Слишком длинная учетная запись NTLM.  <br/> |
|ResourceEMailAddressTooLong = 2036  <br/> |Слишком длинный адрес электронной почты ресурса.  <br/> |
|ResourceCodeTooLong = 2037  <br/> |Слишком длинный код ресурса.  <br/> |
|ResourceGroupTooLong = 2038  <br/> |Слишком длинная группа ресурсов.  <br/> |
|ResourceWorkGroupInvalid = 2039  <br/> |Недопустимая рабочая группа ресурса.  <br/> |
|ResourceTypeInvalid = 2040  <br/> |Недопустимый тип ресурса.  <br/> |
|ResourceNonWorkResourceWithEMailInvalid = 2044  <br/> |Нерабочий ресурс не может иметь адрес электронной почты.  <br/> |
|rsResourceNameHasTrailingOrLeadingWhitespace = 2046  <br/> |В начале или конце имени ресурса присутствует пробел.  <br/> |
|ResourceCannotDeleteCallingUserAccount = 2047  <br/> |Пользователь не может удалить собственную учетную запись.  <br/> |
|ResourceInitialsInvalid = 2048  <br/> |Недопустимое краткое название ресурса.  <br/> |
|ResourceAccrueAtInvalid = 2049  <br/> |Недопустимое значение для начисления.  <br/> |
|ResourceNonMaterialResourceCannotHaveMaterialLabel = 2050  <br/> |Нематериальный ресурс не может иметь единицу измерения материалов.  <br/> |
|ResourceMaterialResourceCannotHaveCertainFields = 2051  <br/> |Материальный ресурс не может иметь определенные поля.  <br/> |
|ResourceAvailFromAvailToOverlap = 2052  <br/> |Наложение дат "доступно с" и "доступно до".  <br/> |
|ResourceInvalidEmailLanguage = 2053  <br/> |Недопустимый язык электронной почты.  <br/> |
|ResourceBookingTypeInvalid = 2055  <br/> |Недопустимый тип резервирования.  <br/> |
|ResourceCannotReplaceMaterialResourceWithNonMaterialResource = 2056  <br/> |Нельзя заменить материальный ресурс нематериальным.  <br/> |
|ResourceCannotUpdateEnterpriseResource = 2057  <br/> |Не удается обновить корпоративный ресурс.  <br/> |
|rsResourceCannotAddLocalWithSameNameAsEnterprise = 2058  <br/> |Не удается добавить локальный ресурс с таким же именем как корпоративный ресурс.  <br/> |
|ResourceCannotSetRateOnCostResource = 2059  <br/> |Не удается задать ставку на затратный ресурс.  <br/> |
|ResourceCannotSetRateOnMaterialResource = 2060  <br/> |Не удается задать ставку на материальный ресурс.  <br/> |
|ResourceCannotSetCanLevelOnNonWorkResource = 2061  <br/> |Не удается задать уровень на нерабочий ресурс.  <br/> |
|ResourceCannotDeleteThisUser = 2062  <br/> |Не удается удалить этого пользователя.  <br/> |
|ResourceCannotDeactivateSelf = 2063  <br/> |Ресурс не может отключить сам себя.  <br/> |
|ResourceAvailabilityDateRangesOverlap = 2064  <br/> |Наложение диапазонов дат доступности ресурса.  <br/> |
|ResourceAvailabilityOutsideTheHireAndTerminationDateRange = 2065  <br/> |Дата доступности ресурса выходит за границы диапазона дат найма и увольнения.  <br/> |
|ResourceFilterInvalid = 2066  <br/> |Недопустимый фильтр для ресурса.  <br/> |
|ResourceSegmentWithThisEffectiveDateDoesNotExist = 2067  <br/> |Нельзя удалить несохраненную ставку ресурса.  <br/> |
|ResourceSegmentWithThisEffectiveDateAlready = 2068  <br/> |Сегмент с такой датой действия уже существует.  <br/> |
|ResourceUserHasItemCheckedOutToItStill = 2069  <br/> |Элемент все еще извлечен для пользователя.  <br/> |
|ResourceInvalidHireDate = 2070  <br/> |Недопустимая дата найма.  <br/> |
|ResourceInvalidTerminationDate = 2071  <br/> |Недопустимая дата увольнения.  <br/> |
|ResourceCannotChangeExistingResourceType = 2072  <br/> |Не удается изменить тип ресурса.  <br/> |
|ResourceCannotSetTimesheetManagerOnSpecifiedResource = 2073  <br/> |Не удается задать управляющего расписаниями для указанного ресурса.  <br/> |
|ResourceInvalidTimesheetManager = 2074  <br/> |Недопустимый управляющий расписаниями.  <br/> |
|ResourceInvalidAssignmentOwner = 2075  <br/> |Недопустимый владелец назначения.  <br/> |
|ResourceCannotCreateCostResource = 2076  <br/> |Не удается создать затратный ресурс.  <br/> |
|ResourceInvalidRbsValue = 2077  <br/> |Недопустимое значение RBS.  <br/> |
|ResourceCannotSetAssignmentOwnerOnSpecifiedResource = 2078  <br/> |Не удается задать владельца назначения для указанного ресурса.  <br/> |
|ResourceFieldsInvalidForBudget = 2079  <br/> |Одно или несколько полей для бюджета не являются допустимыми.  <br/> |
|ResourceHyperlinkInvalid = 2080  <br/> |Недопустимая гиперссылка ресурса.  <br/> |
|ResourceAuthorizationValidOnlyOnWorkResources = 2081  <br/> |Авторизация допустима только для рабочих ресурсов.  <br/> |
|ResourceIsProjectOwner = 2082  <br/> |Не удается удалить ресурс, так как он является владельцем проекта.  <br/> |
|ResourceIsTimesheetManager = 2083  <br/> |Не удается удалить ресурс, так как он является управляющим расписаниями.  <br/> |
|ResourceIsDefaultAssignmentOwner = 2084  <br/> |Не удается удалить ресурс, так как он является владельцем назначения по умолчанию.  <br/> |
|ResourceIsAssignmentOwner = 2085  <br/> |Не удается удалить ресурс, так как он является владельцем назначения.  <br/> |
|ResourceIsUsedInResourcePlan = 2086  <br/> |Не удается удалить ресурс, так как он используется в плане использования ресурсов.  <br/> |
|ResourceCannotDeleteEnterpriseResource = 2087  <br/> |По неизвестной причине не удается удалить корпоративный ресурс.  <br/> |
|ResourceSetResourceAuthorizationFailed = 2088  <br/> |Сбой установки авторизации ресурса.  <br/> |
|ResourceTooManyResourcesSpecifiedToDelete = 2089  <br/> |Не удается удалить указанное число ресурсов.  <br/> |
|ResourceTooManyResourcesReturned = 2090  <br/> |Метод не может обработать это число ресурсов.  <br/> |
|ResourceCannotDeleteWorkflowProxyUser = 2091  <br/> |Пользователя прокси-сервера рабочего процесса нельзя удалить.  <br/> |
|ResourceInvalidEmailWithExchangeSync = 2092  <br/> |Недопустимая электронная почта для синхронизации с Microsoft Exchange Server.  <br/> |
|ResourceInvalidResourceTypeWithExchangeSync = 2093  <br/> |Недопустимый тип ресурса для синхронизации с Exchange Server.  <br/> |
|ResourceInvalidPrincipalNameWithExchangeSync = 2094  <br/> |Недопустимое имя участника-ресурса для синхронизации с Exchange Server.  <br/> |
|ResourceInvalidAuthenticationTypeWithExchangeSync = 2095  <br/> |Недопустимый тип проверки подлинности ресурса для синхронизации с Exchange Server.  <br/> |
|ResourceExchangeSyncFlagAndPrincipalNameMismatch = 2096  <br/> |Несоответствие между флагом синхронизации Exchange Server и именем участника для ресурса.  <br/> |
|ResourceUnsupportedUserUpdateInSharePointSecurityMode = 2097  <br/> |Создание пользователя не поддерживается в режиме безопасности SharePoint.  <br/> |

<a name="pj15_ErrorCodes_ResourcePlans"></a>

## <a name="table-21-resource-plan"></a>Табл. 21. План ресурсов

|Код ошибки плана ресурсов|Описание|
|:-----|:-----|
|ResourcePlanProjectPublishIncomplete = 30000  <br/> |Публикация проекта для плана использования ресурсов не была завершена.  <br/> |
|ResourcePlanInvalidResourceType = 30001  <br/> |Недопустимый тип ресурса в плане использования ресурсов.  <br/> |
|ResourcePlanInactiveResourcesDisallowed = 30002  <br/> |Неактивные ресурсы не могут входить в план использования ресурсов.  <br/> |
|ResourcePlanFilterInvalid = 30003  <br/> |Недопустимый фильтр планов использования ресурсов.  <br/> |
|ResourcePlanSaveFailure = 30004  <br/> |Сбой сохранения плана использования ресурсов.  <br/> |
|ResourcePlanCheckinFailure = 30005  <br/> |Сбой возвращения плана использования ресурсов.  <br/> |
|ResourcePlanDeleteFailure = 30006  <br/> |Сбой удаления плана использования ресурсов.  <br/> |
|ResourcePlanInvalidUtilizationType = 30007  <br/> |Недопустимый тип использования плана использования ресурсов.  <br/> |
|ResourcePlanInvalidTimescale = 30008  <br/> |Недопустимая шкала времени для плана использования ресурсов.  <br/> |
|ResourcePlanMismatchedJobList = 30009  <br/> |Несоответствие в списке заданий плана использования ресурсов.  <br/> |
|ResourcePlanAlreadyExists = 30010  <br/> |План использования ресурсов уже существует.  <br/> |
|ResourcePlanInvalidProjectUID = 30011  <br/> |Недопустимый GUID проекта для плана использования ресурсов.  <br/> |
|ResourcePlanResourceAlreadyExists = 30012  <br/> |Ресурс уже существует в плане ресурсов.  <br/> |
   
Коды ошибок в таблице 22 относятся к методам **Rules** в веб-службе **PWA**. Они предназначены для внутреннего использования. 

<a name="pj15_ErrorCodes_Rules"></a>

## <a name="table-22-rules"></a>Табл. 22. Правила

|Код ошибки правил|Описание|
|:-----|:-----|
|RulesNameTooLong = 21001  <br/> |Слишком длинное имя правила утверждения. Только для внутреннего использования в Project Web App.  <br/> |
|RulesDescriptionTooLong = 21002  <br/> |Слишком длинное описание правила. Только для внутреннего использования в Project Web App.  <br/> |
|RulesInvalidRuleType = 21003  <br/> |Тип правила является недопустимым. Только для внутреннего использования в Project Web App.  <br/> |
|RulesInvalidConditionType = 21004  <br/> |Недопустимый тип условия для правила. Только для внутреннего использования в Project Web App.  <br/> |
|RulesInvalidOperatorType = 21005  <br/> |Тип оператора для правила является недопустимым. Только для внутреннего использования в Project Web App.  <br/> |
|RulesInvalidListItemType = 21007  <br/> |Тип элемента списка для правила является недопустимым. Только для внутреннего использования в Project Web App.  <br/> |
|RulesNameInvalidCharacters = 21008  <br/> |В имени правила присутствует один или несколько недопустимых символов. Только для внутреннего использования в Project Web App.  <br/> |
|RulesDescriptionInvalidCharacters = 21009  <br/> |В описании правила присутствует один или несколько недопустимых символов. Только для внутреннего использования в Project Web App.  <br/> |
|RulesInvalidValueType = 21010  <br/> |Недопустимый тип значения в правиле. Только для внутреннего использования в Project Web App.  <br/> |

<a name="pj15_ErrorCodes_Security"></a>

## <a name="table-23-security"></a>Табл. 23. Безопасность

|Код ошибки безопасности|Описание|
|:-----|:-----|
|SecurityGroupCouldNotBeCreated = 19001  <br/> |Не удается создать группу безопасности.  <br/> |
|SecurityFieldAccessIDInvalid = 19003  <br/> |Недопустимый идентификационный номер кода доступа для поля безопасности.  <br/> |
|SecurityCannotUpdateFacForNonExistentCategory = 19004  <br/> |Категория безопасности не существует; не удается обновить код доступа поля.  <br/> |
|SecurityDuplicateCategoryUid = 19005  <br/> |Повторяющийся GUID категории безопасности.  <br/> |
|SecurityDuplicateGroupUid = 19006  <br/> |Повторяющийся GUID группы безопасности.  <br/> |
|SecurityDuplicateTemplateUid = 19007  <br/> |Повторяющийся GUID шаблона безопасности.  <br/> |
|SecurityInvalidTemplateUidRef = 19008  <br/> |Недопустимый GUID шаблона безопасности.  <br/> |
|SecurityInvalidGlobalPermission = 19009  <br/> |Недопустимое глобальное разрешение безопасности.  <br/> |
|SecurityInvalidCategoryPermission = 19010  <br/> |Недопустимое разрешение категории безопасности.  <br/> |
|SecurityUpdatedGroupNotFound = 19013  <br/> |Обновленная группа безопасности не найдена.  <br/> |
|SecurityUpdatedCategoryNotFound = 19014  <br/> |Обновленная категория безопасности не найдена.  <br/> |
|SecurityUpdatedTemplateNotFound = 19015  <br/> |Обновленный шаблон безопасности не найдена.  <br/> |
|SecurityGroupMemberNotFound = 19016  <br/> |Член группы безопасности не найден.  <br/> |
|SecurityUserNotFound = 19018  <br/> |Пользователь Project Server не найден.  <br/> |
|SecurityNoCategoryRelationForPermission = 19019  <br/> |Для разрешения не найдено отношение категории безопасности.  <br/> |
|SecurityCannotDeleteDefaultGroup = 19020  <br/> |Не удается удалить группу безопасности по умолчанию.  <br/> |
|SecurityCannotDeleteDefaultCategory = 19021  <br/> |Не удается удалить категорию безопасности по умолчанию.  <br/> |
|SecurityCategoryCouldNotBeCreated = 19022  <br/> |Не удается создать категорию безопасности.  <br/> |
|SecurityNoCategoryForPermission = 19023  <br/> |Для разрешения не найдена категория безопасности.  <br/> |
|SecurityNoCategoryForObject = 19024  <br/> |Для объекта не найдена категория безопасности.  <br/> |
|SecurityNoCategoryForRule = 19025  <br/> |Для правила не найдена категория безопасности.  <br/> |
|SecurityNoGroupForPermission = 19026  <br/> |Для разрешения не найдена группа безопасности.  <br/> |
|SecurityCannotSetPermissionForFieldGroup = 19027  <br/> |Не удается задать разрешение для поля группы безопасности.  <br/> |
|SecurityInvalidFieldGroup = 19028  <br/> |Недопустимое поле группы безопасности.  <br/> |
|SecurityCannotSetOrgPermission = 19029  <br/> |Не удается задать разрешение организации безопасности.  <br/> |
|SecurityInvalidOrgPermission = 19030  <br/> |Недопустимое разрешение организации безопасности.  <br/> |
|SecurityInvalidSecurityRule = 19031  <br/> |Недопустимое правило безопасности.  <br/> |
|SecurityTemplateNotFound = 19034  <br/> |Шаблон безопасности не найден.  <br/> |
|SecurityInvalidObjectType = 19035  <br/> |Недопустимый тип объекта безопасности.  <br/> |
|SecurityDuplicateUid = 19036  <br/> |GUID объекта безопасности повторяется.  <br/> |
|SecurityObjectNotFound = 19037  <br/> |Объект безопасности не найден.  <br/> |
|SecurityInvalidCategoryUidRef = 19080  <br/> |Недопустимый GUID категории безопасности.  <br/> |
|SecurityInvalidProjectUidRef = 19081  <br/> |Недопустимый GUID проекта для объекта безопасности.  <br/> |
|SecurityInvalidGroupUidRef = 19082  <br/> |Недопустимый GUID группы безопасности.  <br/> |
|SecurityInvalidUserUidRef = 19083  <br/> |Недопустимый GUID пользователя для объекта безопасности.  <br/> |
|SecurityInvalidCategoryPermissionUidRef = 19084  <br/> |Недопустимый GUID разрешения для категории безопасности.  <br/> |
|SecurityInvalidGlobalPermissionUidRef = 19085  <br/> |Недопустимый GUID глобального разрешения безопасности.  <br/> |
|SecurityInvalidResourceUidRef = 19086  <br/> |Недопустимый GUID ресурса для объекта безопасности.  <br/> |
|SecurityDeleteNotSupportedBySetMethod = 19087  <br/> |Метод не может удалить объект безопасности.  <br/> |
|SecurityInvalidProjectCategoryPermissionUidRef = 19088  <br/> |Недопустимый GUID разрешения категории проекта.  <br/> |
|SecurityCannotModifyCoreProjectCategoryDataInUpdate = 19089  <br/> |Метод обновления безопасности не может изменить основные данные категории проекта.  <br/> |
|SecurityProjectCategoryEntitiesDoNotAllowInPlaceChanges = 19090  <br/> |Сущности категории безопасности нельзя изменить во время обновления.  <br/> |
|SecurityCategoryCannotAddRelationForDeletedCategory = 19091  <br/> |Не удается добавить отношение для удаленной категории безопасности.  <br/> |
|SecurityCategoryCannotAddPermissionForDeletedCategory = 19092  <br/> |Не удается добавить разрешение для удаленной категории безопасности.  <br/> |
|SecurityCategoryCannotAddPermissionForDeletedRelation = 19093  <br/> |Не удается добавить разрешение для отношения удаленной категории безопасности.  <br/> |
|SecurityCategoryCannotDeleteRelationForNewlyAddedCategory = 19094  <br/> |Не удается удалить отношение для добавленной категории безопасности.  <br/> |
|SecurityCategoryCannotDeletePermissionForNewlyAddedCategory = 19095  <br/> |Не удается удалить разрешение для добавленной категории безопасности.  <br/> |
|SecurityCategoryCannotDeletePermissionForNewlyAddedRelation = 19096  <br/> |Не удается удалить разрешение для добавленного отношения в категории безопасности.  <br/> |
|SecurityCategoryCannotHaveDuplicateUserOrGroupUidsForRelation = 19097  <br/> |Нельзя использовать повторяющиеся идентификаторы UID пользователя или группы для отношения категории безопасности.  <br/> |
|SecurityCategoryPermissionMustHaveMatchingRelation = 19098  <br/> |Разрешение категории должно иметь соответствующее отношение категории безопасности.  <br/> |
|SecurityCategoryProjectAlreadyHasSecurityProjectCategory = 19099  <br/> |Список выбранных категорий уже имеет категорию безопасности проекта.  <br/> |

<a name="pj15_ErrorCodes_Events"></a>

## <a name="table-24-project-server-event"></a>Табл. 24. Событие Project Server

|Код ошибки события Project Server|Описание|
|:-----|:-----|
|ServerEventInvalidEventId = 19033  <br/> |Недопустимый идентификационный номер события Project Server.  <br/> |
|ServerEventServiceNotFound = 22003  <br/> |Отсутствует служба событий Project Server. Эта ошибка не используется в коде Project Server, но она связана с необработанным событием единой службы ведения журналов (ULS).  <br/> |
|ServerEventRemoteCouldNotReachProxy = 22005  <br/> |Удаленному приложению Project Web App не удается связаться с диспетчером событий прокси-сервера Project Server. Данная ошибка не используется в коде Project Server, однако она сопоставляется с необработанным событием ULS.  <br/> |
|ServerEventManagerCouldNotReachRemote = 22006  <br/> |Диспетчеру событий Project Server не удается связаться с удаленным приложением Project Web App. Данная ошибка не используется в коде Project Server, однако она сопоставляется с необработанным событием ULS.  <br/> |
|ServerEventHandlerNotSigned = 22007  <br/> |Обработчик событий Project Server не подписан.  <br/> |
|ServerEventHandlerMalformedAssemblyName = 22008  <br/> |Недопустимое имя сборки для обработчика событий Project Server.  <br/> |
|ServerEventHandlerOrderInvalid = 22009  <br/> |Недопустимый порядок для обработчика событий Project Server.  <br/> |
|ServerEventHandlerDuplicateEntry = 22010  <br/> |Повторяющаяся запись для обработчика событий Project Server.  <br/> |
|ServerEventHandlerNotFound = 22011  <br/> |Обработчик событий Project Server не найден.  <br/> |
|ServerEventHandlerDuplicateName = 22012  <br/> |Повторяющееся имя для обработчика событий Project Server.  <br/> |
|ServerEventHandlerNullAssemblyNameAndEndpointUrl = 22013  <br/> |Проверьте, имеется ли URL-адрес конечной точки или имя сборки.  <br/> |

<a name="pj15_ErrorCodes_Statusing"></a>

## <a name="table-25-statusing-web-service"></a>Табл. 25. Веб-служба определения состояния 

|Коды ошибок для веб-службы определения состояния|Описание|
|:-----|:-----|
|StatusingInvalidEntity = 3102  <br/> |Объект для **Statusing** является недопустимым.  <br/> |
|StatusingGetDataForTaskFailed = 3103  <br/> |Не удалось получить данные для состояния задачи.  <br/> |
|StatusingGetTaskOrAssnCntrFailed = 3104  <br/> |Не удалось получить задачу или центр назначений для состояния.  <br/> |
|StatusingInvalidPIDForProjCntr = 3105  <br/> |Идентификационный номер свойства **Statusing** для центра проектов является недопустимым.  <br/> |
|StatusingDeleteAssnFailed = 3106  <br/> |Не удалось удалить назначение в процессе **Statusing**.  <br/> |
|StatusingAssnSaveFailed = 3107  <br/> |Не удалось сохранить назначение в процессе **Statusing**.  <br/> |
|StatusingTaskSaveFailed = 3108  <br/> |Не удалось сохранить задачу в процессе **Statusing**.  <br/> |
|StatusingInvalidPID = 3109  <br/> |Идентификационный номер свойства **Statusing** является недопустимым.  <br/> |
|StatusingSetDataValueInvalid = 3111  <br/> |Значение данных **Statusing** является недопустимым.  <br/> |
|StatusingSetDataFailed = 3112  <br/> |Не удалось задать значение **Statusing**.  <br/> |
|StatusingInvalidDelegationStart = 3113  <br/> |Время начала для назначения в методе **DelegateAssignments** является недопустимым.  <br/> |
|StatusingApprovalUpdateFailed = 3114  <br/> |Не удалось обновить утверждение состояния.  <br/> |
|StatusingInvalidApprovalType = 3115  <br/> |Недопустимый тип утверждения состояния.  <br/> |
|StatusingInternalError = 3116  <br/> |Внутренняя ошибка обработки в методе **Statusing**.  <br/> |
|StatusingInvalidUpdateData = 3117  <br/> |Данные обновления в методе **Statusing** являются недопустимыми.  <br/> |
|StatusingProjectUpdateFailed = 3118  <br/> |Сбой обновления **Statusing** проекта.  <br/> |
|StatusingInvalidPreviewData = 3119  <br/> |Данные предварительного просмотра **Statusing** являются недопустимыми.  <br/> |
|StatusingInvalidTransaction = 3120  <br/> |Транзакция **Statusing** является недопустимой.  <br/> |
|StatusingTooManyResults = 3121  <br/> |Слишком много результатов. При считывании повременных данных о состоянии возвращается более 5000 строк.  <br/> |
|StatusingInvalidInterval = 3122  <br/> |Интервал в методе **Statusing** является недопустимым. Интервал должен быть указан в минутах и быть больше нуля.  <br/> |
|StatusingApplyUpdatesFailed = 3123  <br/> |Не удалось применить обновления **Statusing** при постановке запроса в очередь.  <br/> |
|StatusingApplyUpdatesFailure = 3124  <br/> |Не удалось применить обновления **Statusing** во время обработки очереди.  <br/> |
|StatusingInvalidWorkData = 3125  <br/> |Данные трудозатрат для **Statusing** являются недопустимыми.  <br/> |
|StatusingMissingNameAttribute = 3126  <br/> |Отсутствует атрибут имени для **Statusing**.  <br/> |
|StatusingInvalidNameAttribute = 3127  <br/> |Атрибут имени для **Statusing** является недопустимым.  <br/> |
|StatusingInvalidData = 3128  <br/> |Данные **Statusing** являются недопустимыми.  <br/> |
|StatusingInvalidChangelist = 3130  <br/> |Данные XML являются недопустимыми в параметре _changexml_ метода **UpdateStatus**.  <br/> |
|StatusingInsufficientAssignmentRights = 3131  <br/> |**SetAssignmentWorkData** не удается обновить назначение, так как пользователь не имеет разрешения.  <br/> |
|StatusingInvalidChangeNumber = 3132  <br/> |Номер изменения **Statusing** является недопустимым.  <br/> |
|StatusingPidNotEditable = 3133  <br/> |Идентификационный номер свойства **Statusing** является неизменяемым.  <br/> |
|StatusingCannotSetTimephasedDataInManualTasks = 3134  <br/> |Не удается задать повременные данные в выполняемых вручную задачах для **Statusing**.  <br/> |
|StatusingCannotChangeTaskMode = 3135  <br/> |Не удается изменить режим задачи для **Statusing**.  <br/> |
   
Коды ошибок в таблице 26 относятся к методам **StatusReports** в веб-службе **PWA**. Они предназначены для внутреннего использования в Project Web App. 

<a name="pj15_ErrorCodes_StatusReports"></a>

## <a name="table-26-statusreports"></a>Табл. 26. Отчеты о состоянии 

|Код ошибки отчетов о состоянии|Описание|
|:-----|:-----|
|StatusReportsUnknownError = 12100  <br/> |Неизвестная ошибка в **StatusReports**.  <br/> |
|StatusReportsPeriodUnmatched = 12101  <br/> |Не удается сопоставить период отчета о состоянии.  <br/> |
|StatusReportsPeriodUnavailable = 12102  <br/> |Период отчета о состоянии недоступен.  <br/> |
|StatusReportsInvalidFormInput = 12103  <br/> |Данные в форме отчета о состоянии являются недопустимыми.  <br/> |

<a name="pj15_ErrorCodes_Tasks"></a>

## <a name="table-27-task"></a>Табл. 27. Задачи 

|Код ошибки задач|Описание|
|:-----|:-----|
|TaskIDInvalid = 7001  <br/> |Недопустимый GUID задачи.  <br/> |
|TaskNameTooLong = 7003  <br/> |Слишком длинное имя задачи.  <br/> |
|TaskTypeInvalid = 7005  <br/> |Недопустимый тип задачи.  <br/> |
|TaskPriorityInvalid = 7006  <br/> |Недопустимый приоритет задачи.  <br/> |
|TaskConstraintTypeInvalid = 7007  <br/> |Недопустимый тип ограничения задачи.  <br/> |
|TaskNameInvalid = 7008  <br/> |Недопустимое имя задачи.  <br/> |
|TaskConstraintTypeRequiresConstraint = 7010  <br/> |Задаче требуется тип ограничения.  <br/> |
|TaskConstraintTypeCannotHaveConstraintDate = 7011  <br/> |Нельзя использовать дату ограничения для типа ограничения.  <br/> |
|TaskSummaryTaskCannotBeMilestone = 7013  <br/> |Суммарная задача не может быть вехой.  <br/> |
|TaskFixedCostAccrualInvalid = 7014  <br/> |Недопустимое начисление фиксированных затрат для задачи.  <br/> |
|TaskPercentCompleteInvalid = 7015  <br/> |Недопустимое значение процента завершения для задачи.  <br/> |
|TaskWorkPercentCompleteInvalid = 7016  <br/> |Недопустимое значение процента завершения работ для задачи.  <br/> |
|TaskPhysicalPercentCompleteInvalid = 7017  <br/> |Недопустимое значение физического процента завершения для задачи.  <br/> |
|TaskLinkTypeInvalid = 7018  <br/> |Недопустимый тип связи задачи.  <br/> |
|TaskAlreadyExists = 7019  <br/> |Задача уже существует.  <br/> |
|TaskLinkAlreadyExists = 7020  <br/> |Связь задачи уже существует.  <br/> |
|TaskNotFound = 7021  <br/> |Задача не найдена.  <br/> |
|TaskLinkNotFound = 7022  <br/> |Связь задачи не найдена.  <br/> |
|TaskLinkLagInvalid = 7023  <br/> |Недопустимый интервал задержки для связи задачи.  <br/> |
|TaskUnableToInsert = 7025  <br/> |Не удается вставить задачу.  <br/> |
|TaskAddPositionInvalid = 7026  <br/> |Недопустимое положение добавления для задачи.  <br/> |
|TaskOutlineLevelInvalid = 7027  <br/> |Недопустимый уровень структуры задачи.  <br/> |
|TaskDurationFormatInvalid = 7028  <br/> |Недопустимый формат длительности задачи.  <br/> |
|TaskCannotAddWhereSpecified = 7029  <br/> |Не удается добавить задачу в указанное расположение.  <br/> |
|TaskEarnedValueMethodInvalid = 7030  <br/> |Недопустимый метод для освоенного объема задачи.  <br/> |
|TaskCannotModifyProjectSummary = 7031  <br/> |Не удается изменить суммарную задачу проекта.  <br/> |
|TaskCannotDeleteProjectSummary = 7032  <br/> |Не удается удалить суммарную задачу проекта.  <br/> |
|TaskCannotSetActualCost = 7033  <br/> |Не удается задать фактические затраты для задачи.  <br/> |
|TaskLevelingDelayInvalid = 7034  <br/> |Недопустимая выравнивающая задержка для задачи.  <br/> |
|TaskCannotEditSummary = 7035  <br/> |Не удается изменить суммарную задачу.  <br/> |
|TaskCannotCreateSubTasksUnderTasksWithAssignments = 7036  <br/> |Не удается создать подзадачи в задаче, имеющей назначения.  <br/> |
|TaskCannotDeleteSubProject = 7037  <br/> |Не удается удалить подпроект для задачи.  <br/> |
|TaskCannotEditExternal = 7038  <br/> |Не удается изменить внешнюю задачу.  <br/> |
|TaskCannotDeleteExternal = 7039  <br/> |Не удается удалить внешнюю задачу.  <br/> |
|TaskLinkCannotDeleteExternal = 7040  <br/> |Не удается удалить ссылку на внешнюю задачу.  <br/> |
|TaskCannotModifyNullTask = 7041  <br/> |Не удается изменить неопределенную задачу.  <br/> |
|TaskCannotModifyLeafTaskWithNoAssignment = 7042  <br/> |Не удается изменить листовую задачу, не имеющую назначения.  <br/> |
|TaskCannotModifyExternalTask = 7043  <br/> |Не удается изменить внешнюю задачу.  <br/> |
|TaskStatusManagerInvalid = 7044  <br/> |Недопустимый диспетчер состояния задач.  <br/> |
|TaskLinkCyclicDependency = 7045  <br/> |Связь задачи имеет циклическую зависимость.  <br/> |
|TaskCannotCreateOrModifySubTasksUnderTasksWithAssignments = 7046  <br/> |Не удается создать или изменить подзадачи в суммарной задаче, имеющей назначения.  <br/> |
|TaskLinkCannotEditExternal = 7047  <br/> |Не удается изменить ссылку на внешнюю задачу.  <br/> |

<a name="pj15_ErrorCodes_Timesheets"></a>

## <a name="table-28-timesheet"></a>Табл. 28. Расписание 

|Код ошибки расписания|Описание|
|:-----|:-----|
|TimesheetMaxHourPerDayExceeded = 3201  <br/> |Превышено максимальное число часов в день для расписания.  <br/> |
|TimesheetHoursPerTSLimitExceeded = 3202  <br/> |Превышен лимит для количества часов в расписании.  <br/> |
|TimesheetUnverifiedTSLineNotAllowed = 3203  <br/> |В данном случае нельзя использовать непроверенную строку расписания.  <br/> |
|TimesheetIncorrectMode = 3204  <br/> |Недопустимый режим расписания.  <br/> |
|TimesheetInvalidApprover = 3205  <br/> |Недопустимый утверждающий расписание.  <br/> |
|TimesheetFutureReportingNotAllowed = 3206  <br/> |Для расписания нельзя включать в отчет элементы, относящиеся к будущему.  <br/> |
|TimesheetIncorrectPeriod = 3208  <br/> |Недопустимый период расписания.  <br/> |
|TimesheetPeriodClosed = 3209  <br/> |Период расписания закрыт.  <br/> |
|TimesheetPendingLines = 3210  <br/> |Строки расписания ожидают обработки.  <br/> |
|TimesheetInvalidDateRange = 3211  <br/> |Недопустимый диапазон дат расписания.  <br/> |
|TimesheetLineClassDisabled = 3212  <br/> |Класс строк расписания отключен.  <br/> |
|TimesheetLineHasNonExistentItem = 3213  <br/> |Строка расписания включает в себя несуществующий элемент.  <br/> |
|TimesheetLineInvalidStatus = 3214  <br/> |Состояние строки расписания является недопустимым.  <br/> |

<a name="pj15_ErrorCodes_UserDelegation"></a>

## <a name="table-29-user-delegation"></a>Табл. 29. Делегирование пользователя 

|Код ошибки делегирования пользователя|Описание|
|:-----|:-----|
|UserDelegationExpired = 43000  <br/> |Истек срок действия делегирования пользователя.  <br/> |
|UserDelegationCannotSelfDelegate = 43001  <br/> |Пользователь не может выполнить делегирование самому себе.  <br/> |
|UserDelegationInvalidDelegate = 43002  <br/> |Недопустимый делегат пользователя.  <br/> |
|UserDelegationInvalidUser = 43003  <br/> |Недопустимый пользователь для делегирования.  <br/> |
|UserDelegationInvalidDates = 43004  <br/> |Недопустимые даты делегирования пользователя.  <br/> |
|UserDelegationCannotDoubleDelegate = 43005  <br/> |Не удается создать двух делегатов.  <br/> |
|UserDelegationDelegateCannotLogon = 43006  <br/> |Делегат пользователя не может выполнить вход в Project Server.  <br/> |
|UserDelegationDelegateIsInactive = 43007  <br/> |Неактивный делегат пользователя.  <br/> |
|UserDelegationInvalidFilter = 43008  <br/> |Недопустимый фильтр делегатов пользователей.  <br/> |
|UserDelegationUserCannotLogon = 43010  <br/> |Пользователь не может выполнить вход в Project Server.  <br/> |
|UserDelegationUserIsInactive = 43011  <br/> |Делегирование пользователя неактивно.  <br/> |

<a name="pj15_ErrorCodes_Workflow"></a>

## <a name="table-30-workflow"></a>Табл. 30. Рабочий процесс 

|Код ошибки рабочего процесса|Описание|
|:-----|:-----|
|WorkflowPhasesCannotCreatePhase = 35000  <br/> |Не удается создать этап рабочего процесса.  <br/> |
|WorkflowPhasesCannotUpdatePhase = 35001  <br/> |Не удается обновить этап рабочего процесса.  <br/> |
|WorkflowPhasesCannotDeletePhase = 35002  <br/> |Не удается удалить этап рабочего процесса.  <br/> |
|WorkflowPhaseNameIsRequired = 35003  <br/> |Рабочий процесс [PHASE_NAME](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowPhaseRow.PHASE_NAME.aspx) является обязательным.  <br/> |
|WorkflowStagesCannotCreateStage = 35004  <br/> |Не удается создать стадию рабочего процесса.  <br/> |
|WorkflowStagesCannotUpdateStage = 35005  <br/> |Не удается обновить стадию рабочего процесса.  <br/> |
|WorkflowStagesCannotDeleteStage = 35006  <br/> |Не удается удалить стадию рабочего процесса.  <br/> |
|WorkflowStagesProjectsInStage = 35007  <br/> |В стадии рабочего процесса присутствуют проекты.  <br/> |
|WorkflowCannotAccessPDPLibrary = 35008  <br/> |не удается получить доступ к библиотеке страниц сведений о проекте.  <br/> |
|WorkflowInvalidPDPUid = 35009  <br/> |Недопустимый GUID страницы сведений о проекте.  <br/> |
|WorkflowInvalidCustomFieldUid = 35010  <br/> |Недопустимый GUID настраиваемого поля.  <br/> |
|WorkflowCustomFieldNotWorkflowControlled = 35011  <br/> |Настраиваемое поле не управляется рабочим процессом.  <br/> |
|WorkflowCustomFieldCannotBeRequiredAndReadOnly = 35012  <br/> |Настраиваемое поле рабочего процесса не может быть одновременно обязательным и доступным только для чтения.  <br/> |
|WorkflowInvalidWorkflowPhaseUid = 35013  <br/> |Рабочий процесс [PHASE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowPhaseRow.PHASE_UID.aspx) является недопустимым.  <br/> |
|WorkflowInsertWorkflowPhaseNotAllowed = 35014  <br/> |Не удается вставить этап рабочего процесса.  <br/> |
|WorkflowInvalidWorkflowStageUid = 35015  <br/> |Рабочий процесс [STAGE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowStageRow.STAGE_UID.aspx) является недопустимым.  <br/> |
|WorkflowPhaseHasStages = 35016  <br/> |Этап рабочего процесса содержит стадии.  <br/> |
|WorkflowStageNameIsRequired = 35020  <br/> |Рабочий процесс [STAGE_NAME](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.WorkflowStageRow.STAGE_NAME.aspx) является обязательным.  <br/> |
|WorkflowStageAtLeastOnePDPIsRequired = 35021  <br/> |Для этой стадии рабочего процесса требуется хотя бы одна страница сведений о проекте.  <br/> |
|WorkflowCannotStartWorkflow = 35100  <br/> |Не удается запустить рабочий процесс.  <br/> |
|WorkflowStatusCannotUpdateStatus = 35101  <br/> |Не удается обновить состояние рабочего процесса.  <br/> |
|WorkflowOnlyProjectsHaveWorkflow = 35102  <br/> |Рабочий процесс могут иметь только проекты.  <br/> |
|WorkflowNoWorkflowsDefined = 35103  <br/> |Рабочие процессы не заданы.  <br/> |
|WorkflowInvalidStageForProject = 35104  <br/> |Недопустимая стадия рабочего процесса для проекта.  <br/> |
|WorkflowNoWorkflowForProject = 35105  <br/> |У проекта нет рабочего процесса.  <br/> |
|WorkflowCheckinRequiredAndProjectNotCheckedin = 35106  <br/> |Для функционирования рабочего процесса следует возвратить проект.  <br/> |
|WorkflowWaitingForRequiredData = 35107  <br/> |Рабочий процесс ожидает требуемые данные.  <br/> |
|WorkflowFlagCustomFieldsCannotBeRequired = 35108  <br/> |Настраиваемое поле флага не может являться обязательным в рабочем процессе.  <br/> |
|WorkflowCannotChangeWorkflow = 35109  <br/> |Не удается изменить рабочий процесс.  <br/> |
|WorkflowWorkflowStatusPDPNotAllowed = 35110  <br/> |Запрещено использовать страницу сведений о проекте для состояния рабочего процесса.  <br/> |
|WorkflowInvalidWorkflowStatusPDPUid = 35111  <br/> |Недопустимый GUID страницы сведений о проекте для состояния рабочего процесса.  <br/> |
|WorkflowInvalidStageStatusValue = 35112  <br/> |Значение состояния стадии рабочего процесса является недопустимым. При установке состояния стадии рабочего процесса разрешены только значения **InProgressRequestSent**, **InProgressRunning** и **InProgressWaiting** в [Workflow.StageStatus](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.Workflow.StageStatus.aspx).  <br/> |
|WorkflowCannotCheckinNotify = 35113  <br/> |Не удается уведомить рабочий процесс о том, что проект возвращен.  <br/> |
|WorkflowCannotCommitNotify = 35114  <br/> |Не удается уведомить рабочий процесс о том, что проект зафиксирован в планировщике или оптимизаторе.  <br/> |
|WorkflowExceptionStartingWorkflow = 35115  <br/> |Ошибка при запуске рабочего процесса.  <br/> |
|WorkflowStatusPDPMustBeSupplied = 35116  <br/> |Требуется использовать страницу сведений о проекте для состояния рабочего процесса.  <br/> |
|WorkflowWorkflowProxyAccountNotFound = 35117  <br/> |Учетная запись-посредник для рабочего процесса не найдена.  <br/> |
|WorkflowInvalidCurrentStage = 35118  <br/> |Текущая стадия рабочего процесса не является допустимой.  <br/> |
|WorkflowMultipleStagesInProgress = 35119  <br/> |В рабочем процессе одновременно выполняются несколько стадий.  <br/> |
|WorkflowActivityInvalidArgument = 35120  <br/> |Сообщение, получаемое в случае появления действия рабочего процесса, не является допустимым.  <br/> |
|WorkflowMTWConfigurationError = 35121  <br/> |Ошибка конфигурации рабочего процесса Microsoft Azure.  <br/> |
|EnterpriseProjectTypeInvalidEnterpriseProjectTypeUid = 35200  <br/> |Значение **ENTERPRISE_PROJECT_TYPE_UID** является недопустимым.  <br/> |
|EnterpriseProjectTypeCannotCreateEnterpriseProjectType = 35201  <br/> |Не удается создать тип корпоративного проекта.  <br/> |
|EnterpriseProjectTypeCannotUpdateEnterpriseProjectType = 35202  <br/> |Не удается обновить тип корпоративного проекта.  <br/> |
|EnterpriseProjectTypeCannotDeleteEnterpriseProjectType = 35203  <br/> |Не удается удалить тип корпоративного проекта.  <br/> |
|EnterpriseProjectTypeCannotCreateMultipleEnterpriseProjectTypes = 35204  <br/> |Не удается создать несколько типов корпоративного проекта.  <br/> |
|EnterpriseProjectTypeCannotUpdateMultipleEnterpriseProjectTypes = 35205  <br/> |Не удается обновить несколько типов корпоративного проекта.  <br/> |
|EnterpriseProjectTypeInvalidCreatePDPUid = 35206  <br/> |Шаблон корпоративного проекта (EPT) требует наличия связанной страницы сведений о проекте (PDP) для создания проекта с помощью EPT. Если EPT предназначен для рабочего процесса, такая ошибка возникает во время проверки EPT, когда страница сведений о проекте (PDP) не соответствует типу *Create*. Другие типы PDP: *Normal* — для редактирования проекта; *Workflow Status* — для отображения сведений о проекте, связанном с рабочим процессом.  <br/> |
|EnterpriseProjectTypeInvalidProjectPlanTemplateUid = 35207  <br/> |Значение [ENTERPRISE_PROJECT_PLAN_TEMPLATE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeRow.ENTERPRISE_PROJECT_PLAN_TEMPLATE_UID.aspx) является недопустимым.  <br/> |
|EnterpriseProjectTypeInvalidWorkspaceTemplateName = 35208  <br/> |Значение [ENTERPRISE_PROJECT_WORKSPACE_TEMPLATE_NAME](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeRow.ENTERPRISE_PROJECT_WORKSPACE_TEMPLATE_NAME.aspx) является недопустимым.  <br/> |
|EnterpriseProjectTypeInvalidWorkflowAssociationUid = 35209  <br/> |Значение [WORKFLOW_ASSOCIATION_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeRow.WORKFLOW_ASSOCIATION_UID.aspx) является недопустимым.  <br/> |
|EnterpriseProjectTypeCannotReadWssSettings = 35210  <br/> |Не удается считать параметры SharePoint.  <br/> |
|EnterpriseProjectTypeCannotReadWssLanguagesAndTemplates = 35211  <br/> |Не удается считать языки и шаблоны сайтов SharePoint.  <br/> |
|EnterpriseProjectTypeInvalidDepartmentUid = 35212  <br/> |Значение [DEPARTMENT_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeDepartmentsRow.DEPARTMENT_UID.aspx) является недопустимым.  <br/> |
|EnterpriseProjectTypeInvalidUri = 35213  <br/> |Значение [ENTERPRISE_PROJECT_TYPE_UID](https://msdn.microsoft.com/library/WebSvcWorkflow.WorkflowDataSet.EnterpriseProjectTypeDepartmentsRow.ENTERPRISE_PROJECT_TYPE_UID.aspx) является недопустимым.  <br/> |
|EnterpriseProjectTypeUriRequiresHttp = 35214  <br/> |Для кода URI типа корпоративного проекта требуется протокол HTTP.  <br/> |
|EnterpriseProjectTypeCannotDeleteDefault = 35215  <br/> |Не удается удалить тип корпоративного проекта по умолчанию.  <br/> |
|EnterpriseProjectTypeCannotChangeDefault = 35216  <br/> |Не удается изменить тип корпоративного проекта по умолчанию.  <br/> |
|EnterpriseProjectTypeHasProjectsCannotDelete = 35217  <br/> |Не удается удалить тип корпоративного проекта, содержащий проекты.  <br/> |
|EnterpriseProjectTypeCreatePDPIsRequired = 35218  <br/> |Шаблон корпоративного проекта (EPT) для рабочего процесса требует наличия связанной страницы сведений о проекте (PDP) типа *Create* для создания проекта с использованием EPT. Эта ошибка возникает, когда страница сведений о проекте не включается в определение типа корпоративного проекта. Другие типы PDP: *Normal* — для редактирования проекта; *Workflow Status* — для отображения сведений о проекте, связанном с рабочим процессом.  <br/> |
|EnterpriseProjectTypeOnlyOneCreatePDPAllowed = 35219  <br/> |Определение шаблона корпоративного проекта допускает только одну страницу сведений о проекте типа *Create*.  <br/> |
|EnterpriseProjectTypeHasWorkflowOnlyCreatePDPAllowed = 35220  <br/> |Шаблон корпоративного проекта (EPT) для рабочего процесса требует наличия связанной страницы сведений о проекте (PDP) типа *Create* для создания проекта с использованием EPT. Эта ошибка возникает, когда страница сведений о проекте в определении шаблона корпоративного проекта рабочего процесса соответствует другому типу. Другие типы PDP: *Normal* — для редактирования проекта; *Workflow Status* — для отображения сведений о проекте, связанном с рабочим процессом.  <br/> |
|EnterpriseProjectTypeInvalidData = 35221  <br/> |**WorkflowDataSet** для типа корпоративного проекта содержит данные, являющиеся недопустимыми.  <br/> |
|EnterpriseProjectNoDefaultEnterpriseProjectTypeDefined = 35222  <br/> |Не задан тип корпоративного проекта по умолчанию.  <br/> |
|EnterpriseProjectTypeAtLeastOnePDPIsRequired = 35223  <br/> |Для этого типа корпоративного проекта требуется хотя бы одна страница сведений о проекте.  <br/> |
|EnterpriseProjectTypeWorkflowStatusPDPNotAllowed = 35224  <br/> |Запрещено использовать страницу сведений о проекте для состояния рабочего процесса для данного типа корпоративного проекта.  <br/> |
|EnterpriseProjectTypeCannotChangeWorkflowAssociation = 35225  <br/> |Проект уже имеет тип корпоративного проекта (EPT); нельзя изменить EPT для проекта.  <br/> |

<a name="pj15_ErrorCodes_WSS"></a>

## <a name="table-31-wssinterop-and-objectlinkprovider-sharepoint-integration"></a>Табл. 31. WssInterop и ObjectLinkProvider (интеграция с SharePoint)

|Код ошибки интеграции с SharePoint|Описание|
|:-----|:-----|
|WSSCreateSiteFailure = 16400  <br/> |Не удалось создать сайт SharePoint для рабочей области проекта.  <br/> |
|WSSCannotCreateWebWithBlankName = 16401  <br/> |Не удается создать веб-сайт SharePoint с пустым именем.  <br/> |
|WSSWebAlreadyExists = 16402  <br/> |Этот веб-сайт SharePoint уже существует.  <br/> |
|WSSInvalidProjectUID = 16403  <br/> |Недопустимый GUID проекта для рабочей области проекта SharePoint.  <br/> |
|WSSProjectAlreadyHasSpWeb = 16404  <br/> |Проект уже имеет сайт рабочей области SharePoint.  <br/> |
|WSSWebDoesNotExist = 16405  <br/> |Этот веб-сайт SharePoint не существует.  <br/> |
|WSSSpWebAlreadyLinkedToProject = 16406  <br/> |Этот веб-сайт SharePoint уже связан с проектом.  <br/> |
|WSSWebHierarchyDoesNotExist = 16407  <br/> |Эта иерархия веб-сайтов SharePoint не существует.  <br/> |
|WSSSPWebHasChildren = 16408  <br/> |Этот веб-сайт SharePoint имеет дочерние веб-сайты.  <br/> |
|WSSURIInvalidFormat = 16409  <br/> |Недопустимый формат для кода URI веб-сайта SharePoint.  <br/> |
|WSSSyncReportingDataFailed = 16410  <br/> |Не удалось синхронизировать данные отчетности для SharePoint.  <br/> |
|WSSWorkspaceUrlPathTooLong = 16411  <br/> |Слишком длинный URL-путь для рабочей области проекта SharePoint.  <br/> |
|WSSWorkspaceNameContainsIllegalChars = 16412  <br/> |Один или несколько символов в имени сайта проекта SharePoint являются недопустимыми. Следующие символы в имени проекта являются недопустимыми: / " : \< \> | , . ' ? \* #  <br/> |
|WSSInvalidWssServerUid = 16413  <br/> |Недопустимый GUID сервера SharePoint.  <br/> |
|WSSSyncUsersFailed = 16414  <br/> |Не удалось синхронизировать пользователей Project Server с SharePoint.  <br/> |
|WSSWrongWebTemplateLCID = 16415  <br/> |Недопустимый код (или идентификатор) языка для веб-шаблона SharePoint.  <br/> |
|WSSWrongWebTemplate = 16416  <br/> |Недопустимый веб-шаблон SharePoint.  <br/> |
|WSSWebIsNotProjectWorkspace = 16417  <br/> |Этот веб-сайт SharePoint не является рабочей областью проекта.  <br/> |
|WSSWebCannotStartOrEndOnPeriod = 16418  <br/> |Имя веб-сайта SharePoint не может начинаться с точки или заканчиваться точкой.  <br/> |
|WSSCannotDeleteSiteCollection = 16419  <br/> |Не удается удалить семейство веб-сайтов.  <br/> |
|WSSListUidInvalid = 16420  <br/> |Недопустимый GUID списка SharePoint.  <br/> |
|WSSSyncDataSetListUidMismatch = 16421  <br/> |GUID списка SharePoint не соответствует GUID списка в синхронизируемом **DataSet**.  <br/> |
|WSSSyncDataSetMissingProjectSettingsRow = 16422  <br/> |**DataSet** для синхронизации с SharePoint отсутствует в строке настроек проекта.  <br/> |
|WSSSyncDataSetTaskMappingsNotAllowed = 16423  <br/> |Сопоставления задач не разрешаются в **DataSet** для синхронизации с SharePoint.  <br/> |
|WSSSyncDataSetWssListUidEmpty = 16424  <br/> |GUID списка SharePoint является пустым в **DataSet** для синхронизации с SharePoint.  <br/> |
|WSSSyncDataNotFound = 16425  <br/> |Отсутствуют данные для синхронизации с SharePoint.  <br/> |
|WSSSyncCriticalDataValidationError = 16426  <br/> |Критическая ошибка проверки данных при синхронизации с SharePoint.  <br/> |
|WSSSyncSharePointListNotAccessibleError = 16427  <br/> |Список SharePoint недоступен.  <br/> |
|WSSSyncInvalidEntityUids = 16428  <br/> |Недопустимые GUID сущностей для синхронизации с SharePoint.  <br/> |
|WSSSyncInvalidSyncData = 16429  <br/> |Недопустимые данные в синхронизации с SharePoint.  <br/> |
|WSSSyncSPSummaryTaskAssignedToResourceError = 16430  <br/> |В синхронизации с SharePoint присутствует суммарная задача, назначенная ресурсу.  <br/> |
|WSSSyncInsufficientPermissionsToCreateWinUser = 16431  <br/> |Недостаточно разрешений для создания пользователя Windows при синхронизации с SharePoint.  <br/> |
|WSSSyncNoDefaultValueForCustomField = 16432  <br/> |Настраиваемое поле не имеет значения по умолчанию при синхронизации с SharePoint.  <br/> |
|WSSOLPCreateLinkFailure = 18000  <br/> |Не удалось создать ссылку для поставщика связей с объектами SharePoint.  <br/> |
|WSSOLPDeleteWebObjectLinkError = 18001  <br/> |Ошибка при удалении связи с веб-объектом в поставщике связей с объектами SharePoint.  <br/> |
|WSSInvalidPermissionsToWssList = 18002  <br/> |Недопустимые разрешения для списка SharePoint.  <br/> |
|WSSWebIsNotUnderDefaultCollection = 18003  <br/> |Веб-сайт SharePoint находится не в семействе по умолчанию.  <br/> |
|WSSWorkspaceUrlIsNotUnderPrimaryCollection = 18004  <br/> |Указанный URL-адрес рабочей области не является семейством веб-сайтов, сопоставленным с этим экземпляром сервера проектов. Это необходимо для текущего режима разрешений.  <br/> |
|WSSWorkspacesMustBeRestrictedToDefaultCollection = 18005  <br/> |Рабочие области должны быть ограничены до семейства веб-сайтов по умолчанию в текущем режиме разрешений.  <br/> |

<a name="pj15_ErrorCodes_ASMXExample"> </a>

## <a name="error-code-example-for-asmx"></a>Пример кода ошибки для ASMX

Чтобы получить список ошибок, если вы получаете исключение, когда вызываете метод PSI, передайте объект **SoapException** конструктору класса [Microsoft.Office.Project.Server.Library.PSClientError](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.PSClientError.aspx). Затем вы сможете использовать [GetAllErrors](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.PSClientError.GetAllErrors.aspx) для хранения информации об ошибке в массиве **PSErrorInfo** и перечислять ошибки, как показано в примере ниже. 
  
> [!NOTE]
> Объект **PSErrorInfo** не включает всю информацию, которая вам может потребоваться. Например, если вы используете **Resource.CheckOutResources**, где один из ресурсов уже извлечен, **PSErrorInfo** показывает причину сбоя для каждого ресурса, который не удается извлечь, но не включает имя ресурса или GUID. Для получения дополнительной информации в приложении на основе ASMX см. статью [CheckOutResources](https://msdn.microsoft.com/library/WebSvcResource.Resource.CheckOutResources.aspx) . 
  
```cs
using System;
using System.Collections.Generic;
using System.Text;
using System.Web.Services.Protocols;
using System.Windows.Forms;
using PSLibrary = Microsoft.Office.Project.Server.Library;
. . .
try
{
    /* Call a PSI method. */
}
catch (SoapException ex)
{
    string errAttributeName;
    string errAttribute;
    string errMess = "".PadRight(30, '=') + "\r\n" + "Error: " + "\r\n";
    PSLibrary.PSClientError error = new PSLibrary.PSClientError(ex);
    PSLibrary.PSErrorInfo[] errors = error.GetAllErrors();
    PSLibrary.PSErrorInfo thisError;
    for (int i = 0; i < errors.Length; i++)
    {
        thisError = errors[i];
        errMess += "\n" + ex.Message.ToString() + "\r\n";
        errMess += "".PadRight(30, '=') + "\r\nPSCLientError Output:\r\n \r\n";
        errMess += thisError.ErrId.ToString() + "\n";
        for (int j = 0; j < thisError.ErrorAttributes.Length; j++)
        {
            errAttributeName = thisError.ErrorAttributeNames()[j];
            errAttribute = thisError.ErrorAttributes[j];
            errMess += "\r\n\t" + errAttributeName +
                       ": " + errAttribute;
        }
        errMess += "\r\n".PadRight(30, '=');
    }
    MessageBox.Show(errMess, "Error", MessageBoxButtons.OK,
        MessageBoxIcon.Error);
}
```

<a name="pj15_ErrorCodes_WCFExample"> </a>

## <a name="error-code-example-for-wcf"></a>Пример кода ошибки для WCF

Чтобы получить список ошибок, если вы получили **System.ServiceModel.FaultException** при вызове метода PSI в приложении на основе WCF, можно извлечь объект **PSClientError** из объекта **FaultException**. Затем можно использовать [GetAllErrors](https://msdn.microsoft.com/library/Microsoft.Office.Project.Server.Library.PSClientError.GetAllErrors.aspx) для хранения информации об ошибке в массиве **PSErrorInfo** и перечисления ошибок, как в предыдущем примере для ASMX. 
  
```cs
using System;
using System.Text;
using System.ServiceModel;
using System.Xml;
using PSLibrary = Microsoft.Office.Project.Server.Library;
. . .
try
{
    /* Call a PSI method. */
}
catch(FaultException fault)
{
    // Use the WCF FaultException, because the ASMX SoapException does not 
    // exist in a WCF-based application.
    WriteFaultOutput(fault);
}
// Get a PSClientError object from the WCF FaultException object, and
// then display the exception details and each error in the PSClientError stack.
private static void WriteFaultOutput(FaultException fault)
{
    string errAttributeName;
    string errAttribute;
    string errOut;
    string errMess = "".PadRight(30, '=') + "\r\n"
        + "Error details: " + "\r\n";
    PSLibrary.PSClientError error = GetPSClientError(fault, out errOut);
    errMess += errOut;
    PSLibrary.PSErrorInfo[] errors = error.GetAllErrors();
    PSLibrary.PSErrorInfo thisError;
    for (int i = 0; i < errors.Length; i++)
    {
        thisError = errors[i];
        errMess += "\r\n".PadRight(30, '=') + "\r\nPSClientError output:\r\n";
        errMess += thisError.ErrId.ToString() + "\n";
        for (int j = 0; j < thisError.ErrorAttributes.Length; j++)
        {
            errAttributeName = thisError.ErrorAttributeNames()[j];
            errAttribute = thisError.ErrorAttributes[j];
            errMess += "\r\n\t" + errAttributeName
                + ": " + errAttribute;
        }
    }
    Console.ForegroundColor = ConsoleColor.Red;
    Console.WriteLine(errMess);
    Console.ResetColor();
}
/// <summary>
/// Extract a PSClientError object from the ServiceModel.FaultException,
/// for use in output of the GetPSClientError stack of errors.
/// </summary>
/// <param name="e"></param>
/// <param name="errOut">Shows that FaultException has more information 
/// about the errors than PSClientError has. FaultException can also contain 
/// other types of errors, such as failure to connect to the server.</param>
/// <returns>PSClientError object, for enumerating errors.</returns>
public static PSLibrary.PSClientError GetPSClientError(FaultException e, 
                                                        out string errOut)
{
    const string PREFIX = "GetPSClientError() returns null: ";
    errOut = string.Empty;
    PSLibrary.PSClientError psClientError = null;
    if (e == null)
    {
        errOut = PREFIX + "Null parameter (FaultException e) passed in.";
        psClientError = null;
    }
    else
    {
        // Get a ServiceModel.MessageFault object.
        var messageFault = e.CreateMessageFault();
        if (messageFault.HasDetail)
        {
            using (var xmlReader = messageFault.GetReaderAtDetailContents())
            {
                var xml = new XmlDocument();
                xml.Load(xmlReader);
                var serverExecutionFault = xml["ServerExecutionFault"];
                if (serverExecutionFault != null)
                {
                    var exceptionDetails = serverExecutionFault["ExceptionDetails"];
                    if (exceptionDetails != null)
                    {
                        try
                        {
                            errOut = exceptionDetails.InnerXml + "\r\n";
                            psClientError = 
                                new PSLibrary.PSClientError(exceptionDetails.InnerXml);
                        }
                        catch (InvalidOperationException ex)
                        {
                            errOut = PREFIX + "Unable to convert fault exception info ";
                            errOut += "a valid Project Server error message. Message: \n\t";
                            errOut += ex.Message;
                            psClientError = null;
                        }
                    }
                    else
                    {
                        errOut = PREFIX + "The FaultException e is a ServerExecutionFault, "
                            + "but does not have ExceptionDetails.";
                    }
                }
                else
                {
                    errOut = PREFIX + "The FaultException e is not a ServerExecutionFault.";
                }
            }
        }
        else // No detail in the MessageFault.
        {
            errOut = PREFIX + "The FaultException e does not have any detail.";
        }
    }
    errOut += "\r\n" + e.ToString() + "\r\n";
    return psClientError;
}

```

<br/>

Помимо данных в объекте **PSClientError**, объект **FaultException** может включать другие типы ошибок, например сбой при подключении к Project Server. Параметр _errOut_ метода **GetPSClientError** в предыдущем примере показывает дополнительную информацию. Например, образец кода **CreateProject4Department** в методе [QueueCreateProject](https://msdn.microsoft.com/library/WebSvcProject.Project.QueueCreateProject.aspx) включает комментарии, которые показывают, как создаются ошибки при настройке свойств в таблице **ProjectCustomFields**. Когда приложение запускается, параметр _errOut_ включает элемент **errinfo** и другие данные (форматируемые здесь с вывода консоли). 
  
```XML
==============================
Error details:
<errinfo xmlns="">
  <dataset name="ProjectDataSet">
    <table name="ProjectCustomFields">
      <row CUSTOM_FIELD_UID="976d3bd9-95ff-40a2-a938-960c410b0341">
        <error id="11704" name="CustomFieldInvalidTypeColumnFilledIn" 
               uid="aa8a2fab-9262-422f-b022-ca1cb12bc75f"></error>
        <error id="11713" name="CustomFieldRequiredValueNotProvided" 
               uid="dc2e2156-86e9-4aac-bede-d07dc44dfedc"></error>
      </row>
    </table>
  </dataset>
</errinfo>
System.ServiceModel.FaultException`1[SvcProject.ServerExecutionFault]: 
ProjectServerError(s) LastError=CustomFieldRequiredValueNotProvided Instructions: 
Pass this into PSClientError constructor to access all error information 
(Fault Detail is equal to SvcProject.ServerExecutionFault).
============================
PSClientError output:
CustomFieldInvalidTypeColumnFilledIn
============================
PSClientError output:
CustomFieldRequiredValueNotProvided
```

<a name="pj15_ErrorCodes_AR"> </a>

## <a name="see-also"></a>См. также

- [Общие и практические статьи по проектам](project-conceptual-and-how-to-articles.md)
- [SQL Server Profiler](https://msdn.microsoft.com/library/3ad5f33d-559e-41a4-bde6-bb98792f7f1a.aspx)
- [Project Server 2010: чего следует ожидать от непредвиденного](https://blogs.msdn.com/b/brismith/archive/2010/03/24/project-server-2010-what-to-expect-when-you-get-the-unexpected.aspx)
- [Средство просмотра ULS](https://www.codeproject.com/Articles/458052/ULS-Log-Viewer)
    

