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

Бизнес-объекты могут быть исполняемыми файлами (.exe) или динамическими библиотеками ссылок (.dll). Конфигурация, используемая для запуска бизнес-объекта, зависит от того, является ли объект .dll или .exe файлом:

- Бизнес-объекты, созданные .exe файлы, могут быть вызваны через DCOM. Если эти бизнес-объекты используются через службы IIS IIS, они могут быть подвергнуты дополнительной маршалинговке данных, что замедляет производительность клиента.

- Бизнес-объекты, созданные .dll файлов, можно использовать с помощью IIS (и, следовательно, HTTP). Они также могут использоваться в DCOM только через компонентные службы (или Microsoft Transaction Server, если вы используете Windows NT). DLLs бизнес-объекта необходимо зарегистрировать на серверном компьютере IIS, чтобы предоставить вам доступ через IIS. (Действия по настройке DLL для запуска DCOM см. в разделе "Включение DLL для запуска[на DCOM.")](enabling-a-dll-to-run-on-dcom.md)


> [!NOTE]
> Когда бизнес-объекты среднего уровня реализуются в качестве компонентов component Services (с помощью **GetObjectContext,** **SetComplete** и **SetAbort),** они могут использовать компонентные службы (или МТС, если вы используете Windows NT) контекстные объекты для поддержания своего состояния при нескольких клиентских вызовах. Этот сценарий возможен с помощью DCOM, который обычно реализуется между доверенными клиентами и серверами (интрасети). 
>
> В этом случае [RDS. Объект DataSpace](dataspace-object-rds.md) и [метод CreateObject](createobject-method-rds.md) на стороне клиента заменены объектом контекста транзакций и **методом CreateInstance** (обеспечивается **интерфейсом ITransactionContext),** реализованным компонентными службами.


## <a name="see-also"></a>См. также

- [Запуск бизнес-объектов в компонентных службах (SQL Server)](https://docs.microsoft.com/sql/ado/guide/remote-data-service/running-business-objects-in-component-services?view=sql-server-2017)
