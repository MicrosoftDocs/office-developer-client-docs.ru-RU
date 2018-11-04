---
title: Метод Query (RDS - ссылки для настольных баз данных Access)
TOCTitle: Query method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1e7f9dfc3ce5cb0d757951f13c1078ab44d04760
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949427"
---
# <a name="query-method-rds"></a>Метод Query (RDS)

**Применимо к**: Access 2013, Office 2013

Допустимая строка запроса SQL используется для возврата [набора записей](recordset-object-ado.md).

## <a name="syntax"></a>Синтаксис

Установка*набора записей* = *DataFactory*. Запрос (*подключения*, *запросов*)

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Набор записей* |Объектная переменная, представляющий объект **набора записей** .|
|*DataFactory* |Объектная переменная, которая представляет объект [RDSServer.DataFactory](datafactory-object-rdsserver.md) .|
|*Подключение* |**Строковое** значение, содержащее сведения о подключении сервера. Это свойства [подключения](connect-property-rds.md) .|
|*Query* |**Строка** , содержащая запрос SQL.|

## <a name="remarks"></a>Примечания

Запрос следует использовать диалект SQL сервера базы данных. Если возникает ошибка при выполнении запроса, был выполнен возвращается состояние результатов. Метод **Query** не выполняет проверку строки **запроса** синтаксис.

