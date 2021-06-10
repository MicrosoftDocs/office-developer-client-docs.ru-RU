---
title: Минимизация места, занимаемого файлом журнала
TOCTitle: Minimizing log file space usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: da4bf7c9c30d3b9b37e2835ddeeeab2b2ed8a2c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288878"
---
# <a name="minimizing-log-file-space-usage"></a>Минимизация места, занимаемого файлом журнала

**Область применения**: Access 2013, Office 2013

Файл журнала может быстро заполняться (таким образом останавливая сервер), если в базе данных SQL Server большой объем активности. Вы можете настроить файл журнала на **Усечение** на контрольной точке, чтобы значительно продлить срок службы файла журнала для базы данных.

**Включить усечение на контрольной точке Microsoft SQL Server 6.5**

1.  Запустите Microsoft SQL Server Enterprise manager, откройте дерево для сервера и откройте дерево устройств базы данных.

2.  Дважды щелкните имя базы данных, в которой будет включена эта функция.

3.  На **вкладке База данных** выберите **Усечение.**

4.  На **вкладке Параметры** выберите пункт Пункт пропуска **Truncate Log** и нажмите **кнопку ОК.**

**Включить усечение на контрольной точке Microsoft SQL Server 7.0**

1.  Запустите Microsoft SQL Server Enterprise manager, откройте дерево для сервера и откройте дерево Баз данных.

2.  Щелкните правой кнопкой мыши имя базы данных, в которой будет включена эта функция, и выберите **Свойства.**

3.  На **вкладке Параметры** выберите пункт Пункт пропуска **Truncate Log** и нажмите **кнопку ОК.**

Дополнительные сведения о функции **Truncate on Checkpoint** см. в Microsoft SQL Server документации.

