---
title: Securing RDS Applications
TOCTitle: Securing RDS Applications
ms:assetid: 15f41cbb-d6e0-aca8-9c3a-97516d82c302
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248922(v=office.15)
ms:contentKeyID: 48543423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d7bc9ff4741ca9a6eccfb6ede3f569c18d0d20e
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606472"
---
# <a name="securing-rds-applications"></a>Securing RDS Applications

**Применимо к**: Access 2013 | Office 2013

## <a name="microsoft-internet-explorer-security-issues"></a>Проблемы безопасности Microsoft Internet Explorer

С помощью улучшения безопасности добавлена Microsoft® Internet Explorer некоторые объекты ADO и RDS ограничены только в среде «безопасный режим». Для этого необходимо принять во внимание следующие, в том числе связанных различными зонами, уровни безопасности, ограничительная поведение, небезопасных операций и настраивать параметры безопасности.

Дополнительные сведения об этих проблем можно ADO и проблем безопасности служб удаленных рабочих СТОЛОВ в Microsoft Internet Explorer в разделе Технические статьи ActiveX Data Objects (ADO).

<<<<<<< HEAD
## <a name="security-and-your-web-server"></a>Безопасность и веб-сервера

<a name="if-you-use-the-rdsserverdatafactorydatafactory-object-rdsservermd-object-on-your-internet-web-server-remember-that-doing-so-creates-a-potential-security-risk-external-users-who-obtain-valid-data-source-name-dsn-user-id-and-password-information-could-write-pages-to-send-any-query-to-that-data-source-if-you-want-more-restricted-access-to-a-data-source-one-option-is-to-unregister-and-delete-the-rdsserverdatafactory-object-msadcfdll-and-instead-use-custom-business-objects-with-hard-coded-queries"></a>При использовании объекта [RDSServer.DataFactory](datafactory-object-rdsserver.md) на сервере Интернета Имейте в виду, что это действие приведет угрозу безопасности. Внешние пользователи, получающие допустимый источник данных (DSN), идентификатор пользователя и пароль можно записать страницы, чтобы отправить запрос к источнику данных. Если необходимо, чтобы более ограниченный доступ к источнику данных, уже для отмены регистрации и удаления объекта **RDSServer.DataFactory** (msadcf.dll), а вместо этого использовать настраиваемые бизнес-объекты с жестко запросов.
=======
## <a name="security-and-your-web-server"></a>Безопасность и веб-сервера

При использовании объекта [RDSServer.DataFactory](datafactory-object-rdsserver.md) веб-сервера Интернета Имейте в виду, что это действие приведет угрозу безопасности. Внешние пользователи, получающие допустимый источник данных (DSN), идентификатор пользователя и пароль можно записать страницы, чтобы отправить запрос к источнику данных. Если необходимо, чтобы более ограниченный доступ к источнику данных, уже для отмены регистрации и удаления объекта **RDSServer.DataFactory** (msadcf.dll), а вместо этого использовать настраиваемые бизнес-объекты с жестко запросов.
>>>>>>> master

Дополнительные сведения о влиянии безопасности с помощью объекта RDSServer.DataFactory можно Microsoft по безопасности MS99-025 на [веб-сайте Microsoft Security](https://www.microsoft.com/en-us/security/default.aspx).

## <a name="client-impersonation-and-security"></a>Олицетворение и безопасность

<<<<<<< HEAD, если свойство **Проверка подлинности пароля** для служб IIS веб-сервер имеет значение для проверки подлинности Windows NT запрос и ответ (для Windows NT 4.0) или встроенная проверка подлинности Windows (для Windows 2000), затем business объекты вызываются в контексте безопасности клиента. Это новая функция в 1,5 служб удаленных рабочих СТОЛОВ, обеспечивающий олицетворение клиента по протоколу HTTP. При работе в этом режиме не анонимного входа на веб-сервер (IIS), но использует идентификатор пользователя и пароль, на котором работает на клиентском компьютере в разделе. Если ODBC DSN настроены для использования доверительное соединение, затем доступа к базам данных, таких как SQL Server, также происходит в контексте безопасности клиента. Однако это работает, только если база данных находится на том же компьютере, что и службы IIS; учетные данные клиента не удается перенесенных на еще один компьютер.

<a name="for-example-a-client-john-doe-with-useridjohnd-and-passwordsecret-is-logged-on-to-a-client-computer-he-runs-a-browser-based-application-that-needs-to-access-the-rdsserverdatafactory-object-to-create-a-recordsetrecordset-object-adomd-by-executing-an-sql-query-on-the-myserver-computer-running-iis-myserver-a-system-running-windows-nt-server-40-is-set-up-to-use-windows-nt-challengeresponse-authentication-its-odbc-dsn-has-use-trusted-connection-selected-and-the-server-also-contains-the-sql-server-data-source-when-a-request-is-received-on-the-web-server-it-asks-the-client-for-the-user-id-and-password-thus-the-request-is-logged-on-myserver-as-coming-from-johndsecret-instead-of-iusermyserver-which-is-the-default-when-anonymous-password-authentication-is-on-similarly-when-logging-on-to-sql-server-johndsecret-is-used"></a>Например, клиент, Иван Петров с userid = «JohnD» и пароль = «секрет» вошел в систему на клиентский компьютер. Он запускает приложение из браузера, которому требуется доступ к объекту **RDSServer.DataFactory** для создания [записей](recordset-object-ado.md) путем выполнения запроса SQL на компьютере «MyServer» под управлением служб IIS. MyServer, системой Windows NT Server 4.0, настроен на использование проверки подлинности Windows NT запрос и ответ, его ODBC DSN имеет «Использовать доверительное соединение» выбран и сервере также содержит источник данных SQL Server. При получении запроса на веб-сервере в ответ на запрос клиента идентификатор пользователя и пароль. Таким образом, запрос вошел в систему MyServer как поступающие от «JohnD» и «Скрытая», а не IUSER\_MyServer (по умолчанию при включенном анонимная проверка подлинности пароля). Аналогично при подключении к SQL Server, «JohnD» / «Секретный» используется.
=======
Если **Проверка подлинности пароля** для веб-сервера IIS свойству для проверки подлинности Windows NT запрос и ответ (для Windows NT 4.0) или встроенная проверка подлинности Windows (для Windows 2000), бизнес-объекты, вызываются в области клиента контекст безопасности. Это новая функция в 1,5 служб удаленных рабочих СТОЛОВ, обеспечивающий олицетворение клиента по протоколу HTTP. При работе в этом режиме не анонимного входа на веб-сервер (IIS), но использует идентификатор пользователя и пароль, на котором работает на клиентском компьютере в разделе. Если ODBC DSN настроены для использования доверительное соединение, затем доступа к базам данных, таких как SQL Server, также происходит в контексте безопасности клиента. Однако это работает, только если база данных находится на том же компьютере, что и службы IIS; учетные данные клиента не удается перенесенных на еще один компьютер.

Например, клиент, Иван Петров с userid = «JohnD» и пароль = «секрет» вошел в систему на клиентский компьютер. Он запускает приложение из браузера, которому требуется доступ к объекту **RDSServer.DataFactory** для создания [записей](recordset-object-ado.md) путем выполнения запроса SQL на компьютере «MyServer» под управлением служб IIS. MyServer, системой Windows NT Server 4.0, настроен на использование проверки подлинности Windows NT запрос и ответ, его ODBC DSN имеет «Использовать доверительное соединение» выбран и сервере также содержит источник данных SQL Server. При получении запроса на веб-сервере в ответ на запрос клиента идентификатор пользователя и пароль. Таким образом, запрос вошел в систему MyServer как поступающие от «JohnD» и «Скрытая», а не IUSER\_MyServer (по умолчанию при включенном анонимная проверка подлинности пароля). Аналогично при подключении к SQL Server, «JohnD» / «Секретный» используется.
>>>>>>> master

Следовательно режим проверки подлинности IIS Windows NT запрос и ответ позволяет HTML-страниц создавать без запроса пользователя явным образом для пользователя идентификатора и пароля информацию, необходимую для входа в базу данных. При использовании обычной проверки подлинности IIS, затем это также будет обязательным.

## <a name="password-authentication"></a>Проверка подлинности пароля

<<<<<<< HEAD служб удаленных рабочих СТОЛОВ обмениваться данными с веб-сервер IIS под управлением в одном из трех режимов проверки подлинности пароля: анонимные, базовая, или проверку подлинности NT запрос и ответ (называемая встроенная проверка подлинности Windows в Windows 2000). Эти параметры определяют, как веб-сервер управляет доступом через него, например запрос, что на клиентский компьютер привилегии явный доступ NT веб-сервера.
=== Служб удаленных рабочих СТОЛОВ обмениваться данными с веб-сервере IIS, выполняющегося в любой из трех режимов проверки подлинности пароля: анонимные, базовая, или проверку подлинности NT запрос и ответ (называемая встроенная проверка подлинности Windows в Windows 2000). Эти параметры определяют, как веб-сервер управляет доступом через него, например запрос, что на клиентский компьютер привилегии явный доступ на веб-сервере NT.
>>>>>>> master

