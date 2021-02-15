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

Указывает состояние SQL для заданного объекта [Error.](error-object-ado.md)

## <a name="return-value"></a>Возвращаемое значение

Возвращает строковое значение  из пяти символов, которое следует стандарту ANSI SQL и указывает код ошибки.

## <a name="remarks"></a>Заметки

Используйте свойство **SQLState,** чтобы прочитать код ошибки из пяти символов, возвращаемой поставщиком при ошибке во время обработки SQL оператора. Например, при использовании поставщика Microsoft OLE DB для ODBC с базой данных Microsoft SQL Server коды ошибок состояния SQL исходят из ODBC на основе ошибок, характерных для ODBC, или на ошибках, которые происходят из Microsoft SQL Server, а затем соедиируются с ошибками ODBC. Эти коды ошибок задокументированы в стандарте anSI SQL, но могут быть реализованы по-разному различными источниками данных.

