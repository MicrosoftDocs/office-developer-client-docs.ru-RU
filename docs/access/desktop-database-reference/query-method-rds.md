---
title: Метод query (Справочник по базам данных для рабочих столов RDS)
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
# <a name="query-method-rds"></a>Метод query (RDS)

**Область применения**: Access 2013, Office 2013

Для возврата объекта [Recordset](recordset-object-ado.md)используется допустимая строка запроса SQL.

## <a name="syntax"></a>Синтаксис

Задание объекта Recordset для объекта*Recordset* = *.* Запрос (*Подключение*, *запрос*)

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Recordset* |Объектная переменная, представляющая объект **Recordset** .|
|*DataFactory* |Объектная переменная, представляющая объект [фактов рдссервер.](datafactory-object-rdsserver.md) DataObject.|
|*Connection* |**Строковое** значение, содержащее сведения о подключении к серверу. Оно аналогично свойству [Connect](connect-property-rds.md) .|
|*Query* |**Строка** , содержащая запрос SQL.|

## <a name="remarks"></a>Примечания

В запросе должен использоваться диалект SQL сервера базы данных. Состояние результата возвращается при наличии ошибки в выполненном запросе. Метод **Query** не выполняет проверку синтаксиса в строке **запроса** .

