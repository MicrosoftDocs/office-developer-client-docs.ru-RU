---
title: Метод Connection.Close (DAO)
TOCTitle: Close Method
ms:assetid: 9b1a77cb-da12-24d6-892f-a56be103d51d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198015(v=office.15)
ms:contentKeyID: 48546559
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bf99abf97a2eb1b88e7056a36c160eb774959719
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295963"
---
# <a name="connectionclose-method-dao"></a>Метод Connection.Close (DAO)


**Область применения**: Access 2013, Office 2013

Закрывает **открытое** подключение.

## <a name="syntax"></a>Синтаксис

*выражение*.Close

*выражение*: переменная, представляющая объект **Connection**.

## <a name="remarks"></a>Примечания

Если на момент использования метода **Close** объект **Recordset** уже закрыт, возникнет ошибка во время выполнения.

Если вы попытаетесь закрыть объект **Connection**, у которого имеются какие-либо открытые объекты **Recordset**, объекты **Recordset** будут закрыты, и все ожидающие операции обновления или изменения будут отменены. Аналогично, если вы попытаетесь закрыть объект **Workspace**, у которого имеются какие-либо открытые объекты **Connection**, эти объекты **Connection** будут закрыты, что приведет к закрытию их объектов **Recordset**.

Альтернатива методу **Close** заключается в присвоении объектной переменной значения **Nothing** (Set dbsTemp = Nothing).

