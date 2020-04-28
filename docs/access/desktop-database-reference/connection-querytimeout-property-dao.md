---
title: Свойство Connection. QueryTimeout (DAO)
TOCTitle: QueryTimeout Property
ms:assetid: 97853412-d5ae-7a71-ccaa-595c68919654
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197804(v=office.15)
ms:contentKeyID: 48546471
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052905
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a2a03b97fc69d6d770a5d7a1d149f6518933002b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295823"
---
# <a name="connectionquerytimeout-property-dao"></a>Свойство Connection. QueryTimeout (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, задающее время ожидания в секундах до возникновения ошибки времени ожидания при выполнении запроса к источнику данных ODBC.

## <a name="syntax"></a>Синтаксис

*Expression* . QueryTimeout

*выражение*: переменная, представляющая объект **Connection**.

## <a name="remarks"></a>Примечания

Значение по умолчанию  60.

При использовании базы данных ODBC, такой как Microsoft SQL Server, могут возникать задержки из-за сетевого трафика или интенсивного использования сервера ODBC. Вместо неопределенного периода ожидания можно указать время ожидания.

При использовании **QueryTimeOut** с **[подключением](connection-object-dao.md)** или объектом **[базы данных](database-object-dao.md)** он задает глобальное значение для всех запросов, связанных с базой данных. Вы можете переопределить это значение для определенного запроса, задав свойство **ODBCTimeout** для определенного объекта **[QueryDef](querydef-object-dao.md)** .

