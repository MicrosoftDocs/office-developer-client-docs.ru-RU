---
title: Свойство SQLState (ADO)
TOCTitle: SQLState property (ADO)
ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15)
ms:contentKeyID: 48547806
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f6fb45342a56a003856192a353270778b44654de
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872181"
---
# <a name="sqlstate-property-ado"></a>Свойство SQLState (ADO)


**Применимо к**: Access 2013, Office 2013

Указывает состояние SQL для того или иного объекта [ошибки](error-object-ado.md) .

## <a name="return-value"></a>Возвращаемое значение

Возвращает **строковое** значение пяти символов, которая стандарту ANSI SQL и указывает код ошибки.

## <a name="remarks"></a>Замечания

Используйте свойство **SQLState** читать код ошибки пяти знаков, поставщик возвращает при возникновении ошибки во время обработки инструкции SQL. Например при использовании поставщик Microsoft OLE DB для ODBC с базой данных Microsoft SQL Server, коды ошибок состояний SQL берутся из ODBC, основанные на ошибки, относящиеся к ODBC или на ошибки, которые создаются из Microsoft SQL Server, а затем сопоставляются с ODBC ошибки. Эти коды ошибок описаны в стандарте ANSI SQL, но может быть по-разному реализован различных источников данных.

