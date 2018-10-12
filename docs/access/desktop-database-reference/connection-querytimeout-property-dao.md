---
title: Connection.QueryTimeout Property (DAO)
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
ms.openlocfilehash: 51f2f51743a8f92b77fafacebbc18e11eb77fe8a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480470"
---
# <a name="connectionquerytimeout-property-dao"></a>Connection.QueryTimeout Property (DAO)


**Применимо к**: Access 2013 | Office 2013

Задает или возвращает значение, указывающее количество секунд ожидания до возникновения ошибки времени ожидания при выполнении запроса на источник данных ODBC.

## <a name="syntax"></a>Синтаксис

*выражение* . QueryTimeout

*выражение* Переменная, которая содержит объект **подключения** .

## <a name="remarks"></a>Замечания

Значение по умолчанию — 60.

При использовании базы данных ODBC, например Microsoft SQL Server, могут возникнуть задержки из-за сетевой трафик или высокая интенсивность операций использования ODBC сервера. Вместо ожидания, можно указать время ожидания.

При использовании **QueryTimeout** с объектом **[подключения](connection-object-dao.md)** или **[базы данных](database-object-dao.md)** , задает глобальное значение для всех запросов, связанной с базой данных. Можно переопределить это значение для конкретного запроса, задав свойство **время ожидания ODBC** определенного объекта **[QueryDef](querydef-object-dao.md)** .
