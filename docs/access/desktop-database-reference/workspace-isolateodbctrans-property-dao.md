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

Задает или возвращает значение, которое указывает, изолированы ли несколько транзакций, связанных с тем же источником данных базы данных Microsoft Access, подключенным к базе данных ODBC (только в рабочей области Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражения* . IsolateODBCTrans

*expression*: переменная, представляющая объект **Workspace**.

## <a name="remarks"></a>Примечания

В некоторых ситуациях необходимо иметь несколько одновременных транзакций, ожидающих одно и то же подключение ODBC. Для этого необходимо открыть отдельное рабочее пространство **для** каждой транзакции. Хотя **каждое рабочее** пространство может иметь собственное подключение ODBC к базе данных, это замедляет производительность системы. Так как обычно не требуется изоляция транзакций, подключения ODBC из нескольких объектов **Workspace,** открытых тем же пользователем, делятся по умолчанию.

Некоторые серверы ODBC, например Microsoft SQL Server, не позволяют одновременные транзакции на одном подключении. Если требуется одновременно иметь несколько транзакций, ожидающих от такой базы данных, установите  свойство **IsolateODBCTrans** true на каждом рабочем пространстве, как только вы откроете его.  Это заставляет отдельное подключение ODBC для каждого **рабочего пространства.**

