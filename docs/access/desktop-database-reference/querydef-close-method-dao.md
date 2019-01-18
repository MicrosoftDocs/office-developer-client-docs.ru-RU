---
title: Метод QueryDef.Close (DAO)
TOCTitle: Close Method
ms:assetid: b2b63462-453d-9e2b-0bb3-69a4a7a6ecef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822031(v=office.15)
ms:contentKeyID: 48547179
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052976
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4d50fa52ff4f5d669b062a052bf3e59a28a9e732
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720004"
---
# <a name="querydefclose-method-dao"></a>Метод QueryDef.Close (DAO)


**Применимо к**: Access 2013, Office 2013

Закрытие открытых **QueryDef**.

## <a name="syntax"></a>Синтаксис

*выражение* . Закрыть

*выражение* Переменная, которая представляет собой объект- **QueryDef** .

## <a name="remarks"></a>Замечания

Если при использовании **Close**объекта **QueryDef** закрыт, возникает ошибка времени выполнения.

Альтернативой метод **Close** — это значение переменной объекта значение **Nothing** (задать dbsTemp = ничего).

