---
title: Модель программирования RDS с объектами
TOCTitle: RDS programming model with objects
ms:assetid: 207150ec-8eb5-bec5-3059-db37a0e28c19
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248987(v=office.15)
ms:contentKeyID: 48543663
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9743fb1e7329457abb60ed8ed41bc39067f3551d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301052"
---
# <a name="rds-programming-model-with-objects"></a>Модель программирования RDS с объектами

**Область применения**: Access 2013, Office 2013

Целью RDS является получение доступа к источникам данных и их обновление через посредника, такого как IIS. Модель программирования определяет последовательность действий, необходимых для достижения этой цели. Объектная модель определяет объекты, методы и свойства которых влияют на модель программирования.

RDS предоставляет средства для выполнения следующей последовательности действий:

- Укажите вызываемую на сервере программу и получите способ (прокси-сервер) ссылаться на нее от клиента ([RDS). DataSpace](dataspace-object-rds.md)).

- Вызов серверной программы. Передав параметры серверной программе, которая определяет источник данных и команду для выдачи (прокси-сервер [или RDS). DataControl](datacontrol-object-rds.md)).

- Серверная программа получает объект [Recordset](recordset-object-ado.md) из источника данных, обычно с помощью ADO. При желании объект **Recordset** обрабатывается на сервере ([RDSServer.DataFactory).](datafactory-object-rdsserver.md)

- Серверная программа возвращает конечный **объект Recordset** в клиентском приложении (прокси-сервере).

- На клиенте объект **Recordset** передается в форму, которая может быть легко использована визуальными элементами управления (визуальным элементом управления и **RDS). DataControl**).

- Изменения объекта **Recordset** отправляются обратно на сервер и используются для обновления источника данных **(RDS). DataControl** или **RDSServer.DataFactory**).

