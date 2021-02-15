---
title: Метод Recordset2.Close (DAO)
TOCTitle: Close Method
ms:assetid: ef816969-9857-37cf-9562-d5c80d2815ea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836412(v=office.15)
ms:contentKeyID: 48548584
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 178dec604a185da94493e6d586249bd2a633899c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307387"
---
# <a name="recordset2close-method-dao"></a>Метод Recordset2.Close (DAO)


**Область применения**: Access 2013, Office 2013

Закрывает открытый объект **Recordset**.

## <a name="syntax"></a>Синтаксис

*выражение*.Close

*выражение* Переменная, представляюная объект **Recordset2.**

## <a name="remarks"></a>Комментарии

Если на момент использования метода **Close** объект **Recordset** уже закрыт, возникнет ошибка во время выполнения.

Если вы попытаетесь закрыть объект **Connection**, у которого имеются какие-либо открытые объекты **Recordset**, объекты **Recordset** будут закрыты, и все ожидающие операции обновления или изменения будут отменены. Аналогично, если вы попытаетесь закрыть объект **Workspace**, у которого имеются какие-либо открытые объекты **Connection**, эти объекты **Connection** будут закрыты, что приведет к закрытию их объектов **Recordset**.

Альтернатива методу **Close** заключается в присвоении объектной переменной значения **Nothing** (Set dbsTemp = Nothing).

