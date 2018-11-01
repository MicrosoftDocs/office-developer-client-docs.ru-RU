---
title: Recordset2.Close Method (DAO)
TOCTitle: Close Method
ms:assetid: ef816969-9857-37cf-9562-d5c80d2815ea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836412(v=office.15)
ms:contentKeyID: 48548584
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 62bd5f60ed48e863a5190a19e546d292156f8dac
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888337"
---
# <a name="recordset2close-method-dao"></a>Recordset2.Close Method (DAO)


**Применимо к**: Access 2013, Office 2013

Закрытие открытых **набора записей**.

## <a name="syntax"></a>Синтаксис

*выражение* . Закрыть

*выражение* Переменная, которая представляет собой объект- **Recordset2** .

## <a name="remarks"></a>Замечания

Если при использовании **Close**объекта **набора записей** закрыт, возникает ошибка времени выполнения.

При попытке закрыть объект **подключения** имеет все открытые объекты **набора записей** объекты **набора записей** будут закрыты, а все ожидающие обновления или изменения будут отменены. Аналогично при попытке закрыть объект **рабочей области** , имеет все открытые объекты **подключения** , эти объекты **подключения** будут закрыты, которой закрывается их объекты **набора записей** .

Альтернативой метод **Close** — это значение переменной объекта значение **Nothing** (задать dbsTemp = ничего).

