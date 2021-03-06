---
title: Базовая модель программирования RDS
TOCTitle: Basic RDS programming model
ms:assetid: a8dd22b0-ac9b-b5c3-4e31-d2990d36230a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249781(v=office.15)
ms:contentKeyID: 48546911
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 947a6355d07ba2e9fb9b2a9b76c4c1941d83e668
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296887"
---
# <a name="basic-rds-programming-model"></a>Базовая модель программирования RDS

**Область применения**: Access 2013, Office 2013

RDS обращается к приложениям, которые существуют в следующей среде: клиентская программа указывает программу, которая будет выполняться на сервере, и параметры, необходимые для возврата нужной информации. Программа, вызываемая на сервере, получает доступ к указанному источнику данных, извлекает информацию, необязательным образом обрабатывает данные, а затем возвращает полученные сведения в клиентские приложения в форме, которую можно легко использовать. RDS предоставляет средства для выполнения следующей последовательности действий:

- Укажите программу, вызываемую на сервере, и получите способ ссылаться на нее от клиента. (Эта ссылка иногда называется прокси. Представляет программу удаленного сервера. Клиентская программа будет "вызывать" прокси, как если бы это была локализованная программа, но на самом деле вызывает программу удаленного сервера.)

- Вызов серверной программы. Передай параметры серверной программе, которые определяют источник данных и команду для выпуска. (Программа сервера фактически использует ADO для получения доступа к источнику данных. ADO создает подключение к одному из указанных параметров, а затем выдает команду, указанную в другом параметре.)

- Серверная программа получает объект [Recordset](recordset-object-ado.md) из источника данных. Необязательный объект **Recordset** обрабатывается на сервере.

- Программа сервера возвращает конечный объект **Recordset** в клиентском приложении.

- На клиенте объект **Recordset** вложен в форму, которую можно легко использовать с помощью визуальных элементов управления.

- Любые изменения объекта **Recordset** отправляются обратно в серверную программу, которая использует их для обновления источника данных.

Эта модель программирования содержит определенные функции удобства. Если для доступа к источнику данных не требуется сложная серверная программа, а также необходимые параметры подключения и команд, RDS автоматически извлекает указанные данные с помощью простой серверной программы по умолчанию.

Если требуется более сложная обработка, можно указать собственную настраиваемую серверную программу. Например, так как настраиваемая серверная программа обладает полными полномочиями ADO в своем распоряжении, она может подключаться к нескольким различным источникам данных, комбинировать их данные каким-то сложным способом, а затем возвращать простой, обработанный результат в клиентском приложении.

Наконец, если ваши потребности находятся где-то между ними, ADO теперь поддерживает настройку поведения программы сервера по умолчанию.

