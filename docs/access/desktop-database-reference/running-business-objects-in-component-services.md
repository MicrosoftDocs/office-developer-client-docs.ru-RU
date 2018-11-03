---
title: Выполнение бизнес-объекты в службы компонентов
TOCTitle: Running business objects in component services
ms:assetid: 12103458-b1dd-10fc-37e8-883fd6c6b9d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248893(v=office.15)
ms:contentKeyID: 48543328
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3dbf3c88f140210228a1bb3d6d0341d6bde42aa2
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944118"
---
# <a name="running-business-objects-in-component-services"></a>Выполнение бизнес-объекты в службы компонентов

**Применимо к**: Access 2013, Office 2013

Бизнес-объекты могут быть исполняемых файлов (.exe) или библиотеки динамической компоновки (DLL). Конфигурации, используемые для выполнения бизнес-объекта зависит от объекта .dll или .exe файла:

  - Бизнес-объекты, как файлы .exe можно вызвать через DCOM. Если эти бизнес-объекты используются через Internet Information Services (IIS), они могут быть marshalingof дополнительные данные, что приводит к снижению производительности клиента.

  - Бизнес-объекты, как DLL-файлы можно использовать с помощью служб IIS (и, следовательно, HTTP). Они могут также использоваться через DCOM только с помощью службы компонентов (или сервера транзакций, если вы используете Windows NT). Бизнес-объект библиотеки DLL, необходимо зарегистрировать на компьютере сервера IIS для предоставления специальных возможностей с помощью служб IIS. (Для действий по настройке DLL для запуска на DCOM, обратитесь к разделу «[Включение DLL выполнить на DCOM](enabling-a-dll-to-run-on-dcom.md).»)


> [!NOTE]
> При реализации бизнес-объекты на среднем уровне как компоненты службы компонентов (с помощью **GetObjectContext**, **SetComplete**и **SetAbort**), они могут использовать службы компонентов (или MTS, если вы используете Windows NT) контекст объектов сохранение их состояния между нескольких клиентских вызовов. Этот сценарий можно с помощью DCOM, который обычно реализуются между доверенных клиентов и серверов (интрасеть). 
>
> В данном случае [RDS. Пространства данных](dataspace-object-rds.md) объект и метод [CreateObject](createobject-method-rds.md) на стороне клиента, заменяются объект context транзакций и **CreateInstance** метод (интерфейс **ITransactionContext** ), реализованные с помощью службы компонентов.


## <a name="see-also"></a>См. также

- [Выполнение бизнес-объекты в службы компонентов (SQL Server)](https://docs.microsoft.com/sql/ado/guide/remote-data-service/running-business-objects-in-component-services?view=sql-server-2017)