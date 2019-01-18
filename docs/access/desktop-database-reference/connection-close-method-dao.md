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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717218"
---
# <a name="connectionclose-method-dao"></a>Метод Connection.Close (DAO)


**Применимо к**: Access 2013, Office 2013

Закрывает открытое **подключение**.

## <a name="syntax"></a>Синтаксис

*выражение* . Закрыть

*выражение* Переменная, которая содержит объект **подключения** .

## <a name="remarks"></a>Замечания

Если при использовании **Close**объекта **набора записей** закрыт, возникает ошибка времени выполнения.

При попытке закрыть объект **подключения** имеет все открытые объекты **набора записей** объекты **набора записей** будут закрыты, а все ожидающие обновления или изменения будут отменены. Аналогично при попытке закрыть объект **рабочей области** , имеет все открытые объекты **подключения** , эти объекты **подключения** будут закрыты, которой закрывается их объекты **набора записей** .

Альтернативой метод **Close** — это значение переменной объекта значение **Nothing** (задать dbsTemp = ничего).

