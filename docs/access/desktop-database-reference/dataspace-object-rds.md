---
title: DataSpace Object (RDS)
TOCTitle: DataSpace Object (RDS)
ms:assetid: 7db181d5-422b-49fe-b6af-a20f5da520ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249527(v=office.15)
ms:contentKeyID: 48545862
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2466727f52a37d396e7478fa54d27a68158855a4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480175"
---
# <a name="dataspace-object-rds"></a>DataSpace Object (RDS)

**Применимо к**: Access 2013 | Office 2013

Создает прокси-серверы со стороны клиента и настраиваемых бизнес-объектов, расположенной на среднем уровне.

## <a name="remarks"></a>Замечания

Удаленной службы данных должна business объекта прокси-серверы, соответствующего компонента со стороны клиента может устанавливать связь с бизнес-объекты, расположенные на среднем уровне. Прокси-серверы упрощают создание пакета, содержащего, распаковке и транспорта (маршалинга) приложения [записей](recordset-object-ado.md) данных через границы процесса или компьютера.

Служба удаленного данных использует **RDS. Пространства данных** метод [CreateObject](createobject-method-rds.md) объекта для создания объекта business прокси-серверы. Прокси-сервера business object динамически создается при создании экземпляра от своего аналога среднего уровня бизнес-объектов. Служба удаленных данных поддерживает следующие протоколы: HTTP, HTTPS (Secure HTTP Sockets), DCOM и внутрипроцессный (клиентские компоненты и бизнес-объекты хранятся на том же компьютере).

> [!NOTE]
> Ведет себя служб удаленных рабочих СТОЛОВ в виде «без сведений о состоянии» при **RDS. Пространства данных** объект использует протоколов HTTP или HTTPS. То есть все внутренние сведения о запрос клиента удаляется после сервер возвращает ответ.

Хотя существует в течение времени жизни прокси-сервера business object бизнес-объект, бизнес-объект действительно существует только в том случае, пока ответ на запрос. Если выдается запрос (то есть, вызывается метод на бизнес-объект), прокси-сервер открывается новое подключение к серверу и сервер создает новый экземпляр объекта бизнеса. После бизнес-объект отвечает на запрос, сервер уничтожает бизнес-объекта и закрывает подключение.

Это означает, что нельзя передачи данных от одного запроса на другую с помощью переменной или свойству объекта business. Необходимо использовать другой механизм, например файла или аргумента метода, чтобы сохранить данные состояния.

КОД класса для **RDS. Пространства данных** объект является BD96C556-65A3 - 11D 0-983A-00C04FC29E36.
