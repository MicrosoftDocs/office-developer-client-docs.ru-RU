---
title: Свойство SQLState (ADO)
TOCTitle: SQLState property (ADO)
ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15)
ms:contentKeyID: 48547806
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eb4a9adbc6060b7c33e128a0a3fca8c1eb7bc10d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308555"
---
# <a name="sqlstate-property-ado"></a>Свойство SQLState (ADO)


**Область применения**: Access 2013, Office 2013

Указывает состояние SQL для данного объекта [Error.](error-object-ado.md)

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение String  с пятью символами, которое следует стандарту SQL ANSI, и указывает код ошибки.

## <a name="remarks"></a>Примечания

Используйте **свойство SQLState** для чтения кода ошибки с пятью символами, возвращаемого поставщиком при ошибке при обработке SQL оператора. Например, при использовании поставщика DB Microsoft OLE для ODBC с базой данных Microsoft SQL Server, коды ошибок SQL состояния происходят из ODBC, основанные на ошибках, определенных ODBC, или на ошибках, которые происходят из Microsoft SQL Server, а затем относясь к ошибкам ODBC. Эти коды ошибок задокументированы в стандарте SQL anSI, но могут быть реализованы по-разному из различных источников данных.

