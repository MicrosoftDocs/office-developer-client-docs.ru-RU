---
title: Minimizing Log File Space Usage
TOCTitle: Minimizing Log File Space Usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2ac2bee2bf3f1036583bd195edc0c3da9e052f3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483090"
---
# <a name="minimizing-log-file-space-usage"></a>Minimizing Log File Space Usage


**Применимо к**: Access 2013 | Office 2013

Файл журнала можно указать быстро (таким образом, остановка работы сервера) при наличии больших объемов активности в базе данных SQL Server. Файл журнала можно включить **Truncate на контрольной точки** для значительного увеличения работы файла журнала для базы данных.

**Чтобы включить Truncate на контрольной точки в Microsoft SQL Server 6.5**

1.  Запустите Microsoft SQL Server Enterprise Manager, откройте дерево для сервера и откройте дерево устройств базы данных.

2.  Дважды щелкните имя базы данных, на котором эта возможность включена.

3.  Вкладка " **базы данных** " выберите **Truncate**.

4.  На вкладке **Параметры** выберите **Усечение журнала на контрольной точки**и нажмите кнопку **ОК**.

**Чтобы включить Truncate на контрольной точки в Microsoft SQL Server 7.0**

1.  Запустите Microsoft SQL Server Enterprise Manager, откройте дерево для сервера и откройте дерево базы данных.

2.  Щелкните правой кнопкой мыши имя базы данных, на котором этот компонент будет установлен и выберите команду **Свойства**.

3.  На вкладке **Параметры** выберите **Усечение журнала на контрольной точки**и нажмите кнопку **ОК**.

Дополнительные сведения о функции **Truncate на контрольной точки** документации Microsoft SQL Server.

