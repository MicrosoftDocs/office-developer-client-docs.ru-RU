---
title: Выполнение бизнес-объектов в службах компонентов
TOCTitle: Running business objects in component services
ms:assetid: 12103458-b1dd-10fc-37e8-883fd6c6b9d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248893(v=office.15)
ms:contentKeyID: 48543328
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 23cb90161e5e0728aa652ae5d496216676f781a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309208"
---
# <a name="running-business-objects-in-component-services"></a>Выполнение бизнес-объектов в службах компонентов

**Область применения**: Access 2013, Office 2013

Бизнес-объектами могут быть исполняемые файлы (EXE) или библиотеки динамической ссылки (DLL). Конфигурация, используемая для запуска бизнес-объекта, зависит от того, является ли объект DLL-файлом или EXE-файлом:

- Бизнес-объекты, созданные как EXE-файлы, могут быть вызваны с помощью DCOM. Если эти бизнес-объекты используются через службы IIS, на них применяются дополнительные маршалинговые данные, что приводит к замедлению производительности клиента.

- Бизнес-объекты, созданные в качестве DLL-файлов, можно использовать с помощью IIS (и, следовательно, HTTP). Их также можно использовать через DCOM только через службы компонентов (или Microsoft Transaction Server, если вы используете Windows NT). DLL бизнес-объектов необходимо зарегистрировать на сервере IIS, чтобы предоставить вам доступ через IIS. (Действия по настройке DLL для запуска в DCOM см. в разделе["Включение DLL](enabling-a-dll-to-run-on-dcom.md)для запуска в DCOM.")


> [!NOTE]
> Когда бизнес-объекты на среднем уровне реализуются как компоненты служб компонентов (с помощью **GetObjectContext,** **SetComplete** и **SetAbort),** они могут использовать службы компонентов (или MTS, если вы используете Windows NT) для поддержания их состояния в нескольких клиентских вызовах. Этот сценарий возможен с помощью DCOM, который обычно реализуется между доверенными клиентами и серверами (интрасеть). 
>
> В этом случае [RDS. Объект DataSpace](dataspace-object-rds.md) и метод [CreateObject](createobject-method-rds.md) на стороне клиента заменены объектом контекста транзакции и **методом CreateInstance** (предоставляемым интерфейсом **ITransactionContext),** реализованным службами компонентов.


## <a name="see-also"></a>См. также

- [Запуск бизнес-объектов в службах компонентов (SQL Server)](https://docs.microsoft.com/sql/ado/guide/remote-data-service/running-business-objects-in-component-services?view=sql-server-2017)
