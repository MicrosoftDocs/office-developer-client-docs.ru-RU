---
title: RDS Programming Model with Objects
TOCTitle: RDS Programming Model with Objects
ms:assetid: 207150ec-8eb5-bec5-3059-db37a0e28c19
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248987(v=office.15)
ms:contentKeyID: 48543663
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 833d3676c8fa3fac1e5cb8e16477073cde611199
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480733"
---
# <a name="rds-programming-model-with-objects"></a>RDS Programming Model with Objects


**Применимо к**: Access 2013 | Office 2013

Цель служб удаленных рабочих СТОЛОВ — получить доступ к и обновлять источники данных через промежуточное, таких как службы IIS. Модель программирования определяет последовательность действий, необходимых для этой цели. Объектная модель определяет объекты, методы и свойства влияют на модели программирования.

Служб удаленных рабочих СТОЛОВ позволяет выполнять следующие действия:

  - Укажите программу для вызова на сервере и получить способом (прокси-сервер), обратитесь к нему из клиента ([RDS. Пространства данных](dataspace-object-rds.md)).

  - Вызов программы сервера. Передает параметры программе сервера, которое идентифицирует источник данных и команды для устранения проблемы (прокси-сервер или [RDS. DataControl](datacontrol-object-rds.md)).

  - Программы сервера получает объект [набора записей](recordset-object-ado.md) из источника данных, обычно с помощью ADO. Кроме того в объект **набора записей** обрабатывается на сервере ([RDSServer.DataFactory](datafactory-object-rdsserver.md)).

  - Программы сервера возвращает окончательный объекта **набора записей** в клиентском приложении (прокси-сервер).

  - На стороне клиента, находится в состоянии объекта **набора записей** в форму, можно легко использовать visual элементы управления (элемент управления visual и **RDS. DataControl**).

  - Изменения в объект **набора записей** отправляются на сервер и используется для обновления источника данных (**RDS. DataControl** или **RDSServer.DataFactory**).

