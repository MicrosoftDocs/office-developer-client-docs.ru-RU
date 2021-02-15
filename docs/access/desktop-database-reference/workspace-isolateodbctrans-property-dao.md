---
title: Свойство Workspace.IsolateODBCTrans (DAO)
TOCTitle: IsolateODBCTrans Property
ms:assetid: f7a48358-870b-cad3-d4ef-e46b50428e12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836924(v=office.15)
ms:contentKeyID: 48548770
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053083
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 781679dfbd4050cfde219802db4cd9e1544d83ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302515"
---
# <a name="workspaceisolateodbctrans-property-dao"></a>Свойство Workspace.IsolateODBCTrans (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, которое указывает, изолированы ли несколько транзакций, в которые включается один и тот же источник данных ODBC, подключенный к яду баз данных Microsoft Access (только для рабочей области Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение .* IsolateODBCTrans

*expression*: переменная, представляющая объект **Workspace**.

## <a name="remarks"></a>Заметки

В некоторых случаях требуется несколько одновременных транзакций, ожидающих одного подключения ODBC. Для этого необходимо открыть отдельное рабочее **пространство** для каждой транзакции. Хотя каждая **workspace** может иметь собственное подключение ODBC к базе данных, это замедляет производительность системы. Поскольку изоляция транзакций обычно не требуется, подключения ODBC из нескольких объектов **Workspace,** открытых тем же пользователем, по умолчанию совместно.

Некоторые серверы ODBC, например Microsoft SQL Server, не позволяют одновременные транзакции при одном подмыве. Если требуется одновременное ожидание более одной транзакции для такой базы данных, установите  для свойства  **IsolateODBCTrans** true в каждой рабочей области, как только откроете ее. Это привнося отдельное подключение ODBC для каждой **рабочей области.**

