---
title: Database.Connection Property (DAO)
TOCTitle: Connection Property
ms:assetid: 8b900ea4-9179-9ed1-bc0b-0576939bb2bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197325(v=office.15)
ms:contentKeyID: 48546221
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7f0974051b1f10fa73caad6d9feafb2e2b769579
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882842"
---
# <a name="databaseconnection-property-dao"></a>Database.Connection Property (DAO)


**Применимо к**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение* . Подключение

*выражение* Переменная, которая представляет собой объект **базы данных** .

## <a name="remarks"></a>Замечания

Используйте свойство **подключение** для получения ссылки на объект **подключения** , соответствующее **базы данных**. В DAO, объект **подключения** и его соответствующего объекта **базы данных** — это просто два разных объектных переменных ссылки на тот же объект. **[База данных](connection-database-property-dao.md)** свойств объекта **подключения** и свойство **Connection** объекта **базы данных** облегчают изменять подключения к источнику данных ODBC с помощью ядро базы данных Microsoft Access, чтобы использовать технология ODBCDirect.

