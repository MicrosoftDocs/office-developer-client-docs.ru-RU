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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701559"
---
# <a name="workspaceisolateodbctrans-property-dao"></a>Свойство Workspace.IsolateODBCTrans (DAO)


**Применимо к**: Access 2013, Office 2013

Задает или возвращает значение, указывающее, включены ли несколько transactiond, связанных с одной Microsoft Access базы данных подключен модуль источник данных ODBC изолированный (Microsoft Access рабочие области только).

## <a name="syntax"></a>Синтаксис

*выражение* . IsolateODBCTrans

*выражение* Переменная, которая представляет собой объект- **рабочей области** .

## <a name="remarks"></a>Замечания

В некоторых случаях необходимо иметь несколько одновременных незавершенных транзакций для общего подключения ODBC. Для этого необходимо открыть отдельный **рабочей области** для каждой транзакции. Хотя для каждой **рабочей области** может иметь собственный подключения ODBC к базе данных, это снижает производительность системы. Так как изоляции транзакций не обычно не требуется, подключения ODBC от нескольких объектов **рабочей области** при открытии же являются общими по умолчанию.

На некоторых серверах ODBC, такие как Microsoft SQL Server не разрешать одновременных транзакций для одного подключения. Если необходимо иметь несколько транзакций во время ожидающие относительно такой базы данных, присвойте свойству **IsolateODBCTrans** значение **True,** на каждой **рабочей области** сразу после его открытия. Это заставляет отдельное подключение ODBC для каждой **рабочей области**.

