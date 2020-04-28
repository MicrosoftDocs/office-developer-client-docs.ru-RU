---
title: Свойство Database. Connection (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77d9bfa30dbfab21fd75de36b336a25e6af3187e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294997"
---
# <a name="databaseconnection-property-dao"></a>Свойство Database. Connection (DAO)


**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*Expression* . Соединений

*выражение*: переменная, представляющая объект **Database**.

## <a name="remarks"></a>Примечания

Используйте свойство **Connection** для получения ссылки на объект **подключения** , соответствующий **базе данных**. В DAO объект **Connection** и соответствующий ему объект **Database** — это просто две разных ссылки на один и тот же объект. Свойство **[Database](connection-database-property-dao.md)** объекта **Connection** и свойство **Connection** объекта **Database** упрощают изменение подключений к источнику данных ODBC с помощью ядра СУБД Microsoft Access для использования ODBCDirect.

