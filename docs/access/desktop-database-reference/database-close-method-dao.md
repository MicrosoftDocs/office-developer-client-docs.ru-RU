---
title: Метод Database.Close (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 190b47b59bd9781553912f91156c74a3fd09c2d5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699979"
---
# <a name="databaseclose-method-dao"></a>Метод Database.Close (DAO)


**Применимо к**: Access 2013, Office 2013

Закрывает открыть **базу данных**.

## <a name="syntax"></a>Синтаксис

*выражение* . Закрыть

*выражение* Переменная, которая представляет собой объект **базы данных** .

## <a name="remarks"></a>Замечания

Если объект **базы данных** уже работает при использовании **Закрыть**, возникает ошибка времени выполнения.

Альтернативой метод **Close** — это значение переменной объекта значение **Nothing** (задать dbsTemp = ничего).

