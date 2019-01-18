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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716301"
---
# <a name="sqlstate-property-ado"></a>Свойство SQLState (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает состояние SQL для того или иного объекта [ошибки](error-object-ado.md) .

## <a name="return-value"></a>Возвращаемое значение

Возвращает **строковое** значение пяти символов, которая стандарту ANSI SQL и указывает код ошибки.

## <a name="remarks"></a>Замечания

Используйте свойство **SQLState** читать код ошибки пяти знаков, поставщик возвращает при возникновении ошибки во время обработки инструкции SQL. Например при использовании поставщик Microsoft OLE DB для ODBC с базой данных Microsoft SQL Server, коды ошибок состояний SQL берутся из ODBC, основанные на ошибки, относящиеся к ODBC или на ошибки, которые создаются из Microsoft SQL Server, а затем сопоставляются с ODBC ошибки. Эти коды ошибок описаны в стандарте ANSI SQL, но может быть по-разному реализован различных источников данных.

