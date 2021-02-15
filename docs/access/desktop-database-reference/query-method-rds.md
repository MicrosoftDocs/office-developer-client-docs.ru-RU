---
title: Метод запроса (RDS — справочник по базе данных Access для настольных ПК)
TOCTitle: Query method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92c72bf78f8f01a675038f63b065aceb6869fcd0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301115"
---
# <a name="query-method-rds"></a>Метод запроса (RDS)

**Область применения**: Access 2013, Office 2013

Возвращает набор записей с помощью SQL строки [запроса.](recordset-object-ado.md)

## <a name="syntax"></a>Синтаксис

Set *Recordset*  =  *DataFactory*. Query(*Connection*, *Query*)

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Recordset* |Объектная переменная, представляюная объект **Recordset.**|
|*DataFactory* |Объектная переменная, представляюная [объект RDSServer.DataFactory.](datafactory-object-rdsserver.md)|
|*Connection* |**Строка,** содержаная сведения о под подключением к серверу. Это свойство аналогично свойству [Connect.](connect-property-rds.md)|
|*Query* |**Строка,** содержаная SQL запроса.|

## <a name="remarks"></a>Заметки

В запросе должен SQL диалект сервера базы данных. Если при выполнении запроса произошла ошибка, возвращается состояние результата. Метод **Query** не выполняет проверку синтаксиса в **строке запроса.**

